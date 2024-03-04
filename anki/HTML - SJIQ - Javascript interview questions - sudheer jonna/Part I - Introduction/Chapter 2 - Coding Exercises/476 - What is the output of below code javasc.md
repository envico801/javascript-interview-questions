==================== Question ====================  

### What is the output of below code

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">delay</span>(<span class="hljs-params"></span>) {
  <span class="hljs-keyword">return</span> <span class="hljs-keyword">new</span> <span class="hljs-title class_">Promise</span>(<span class="hljs-function">(<span class="hljs-params">resolve</span>) =></span> <span class="hljs-built_in">setTimeout</span>(resolve, <span class="hljs-number">2000</span>));
}
<span class="hljs-keyword">async</span> <span class="hljs-keyword">function</span> <span class="hljs-title function_">delayedLog</span>(<span class="hljs-params">item</span>) {
  <span class="hljs-keyword">await</span> <span class="hljs-title function_">delay</span>();
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(item);
}
<span class="hljs-keyword">async</span> <span class="hljs-keyword">function</span> <span class="hljs-title function_">process</span>(<span class="hljs-params">array</span>) {
  array.<span class="hljs-title function_">forEach</span>(<span class="hljs-keyword">async</span> (item) => {
     <span class="hljs-keyword">await</span> <span class="hljs-title function_">delayedLog</span>(item);
  });
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'Process completed!'</span>);
}
<span class="hljs-title function_">process</span>([<span class="hljs-number">1</span>, <span class="hljs-number">2</span>, <span class="hljs-number">3</span>, <span class="hljs-number">5</span>]);
</code></pre>
<!-- codeblock-end -->

- 1: 1 2 3 5 and Process completed!

- 2: 5 5 5 5 and Process completed!

- 3: Process completed! and 5 5 5 5

- 4: Process completed! and 1 2 3 5  

==================== Answer ====================  

Answer: 4

The forEach method will not wait until all items are finished but it just runs the tasks and goes next. Hence, the last statement is displayed first followed by a sequence of promise resolutions.

But you control the array sequence using for..of loop,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">async</span> <span class="hljs-keyword">function</span> <span class="hljs-title function_">processArray</span>(<span class="hljs-params">array</span>) {
  <span class="hljs-keyword">for</span> (<span class="hljs-keyword">const</span> item <span class="hljs-keyword">of</span> array) {
     <span class="hljs-keyword">await</span> <span class="hljs-title function_">delayedLog</span>(item);
  }
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'Process completed!'</span>);
}
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
476

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#476-What-is-the-output-of-below-code-javasc

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
