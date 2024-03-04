==================== Question ====================  

### What is the output of below code

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">delay</span>(<span class="hljs-params"></span>) {
<span class="hljs-keyword">return</span> <span class="hljs-keyword">new</span> <span class="hljs-title class_">Promise</span>(<span class="hljs-function"><span class="hljs-params">resolve</span> =></span> <span class="hljs-built_in">setTimeout</span>(resolve, <span class="hljs-number">2000</span>));
}
<span class="hljs-keyword">async</span> <span class="hljs-keyword">function</span> <span class="hljs-title function_">delayedLog</span>(<span class="hljs-params">item</span>) {
<span class="hljs-keyword">await</span> <span class="hljs-title function_">delay</span>();
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(item);
}
<span class="hljs-keyword">async</span> <span class="hljs-keyword">function</span> <span class="hljs-title function_">processArray</span>(<span class="hljs-params">array</span>) {
array.<span class="hljs-title function_">forEach</span>(<span class="hljs-function"><span class="hljs-params">item</span> =></span> {
 <span class="hljs-keyword">await</span> <span class="hljs-title function_">delayedLog</span>(item);
})
}
<span class="hljs-title function_">processArray</span>([<span class="hljs-number">1</span>, <span class="hljs-number">2</span>, <span class="hljs-number">3</span>, <span class="hljs-number">4</span>]);
</code></pre>
<!-- codeblock-end -->

- 1: SyntaxError

- 2: 1, 2, 3, 4

- 3: 4, 4, 4, 4

- 4: 4, 3, 2, 1  

==================== Answer ====================  

Answer: 1

Even though “processArray” is an async function, the anonymous function that we use for `forEach` is synchronous. If you use await inside a synchronous function then it throws a syntax error.

==================== Id ====================  
475

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#475-What-is-the-output-of-below-code-javasc

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
