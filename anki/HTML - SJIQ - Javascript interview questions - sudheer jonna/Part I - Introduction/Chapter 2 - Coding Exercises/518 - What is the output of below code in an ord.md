==================== Question ====================  

### What is the output of below code in an order?

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">second</span>(<span class="hljs-params"></span>) {
  <span class="hljs-keyword">var</span> message;
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(message);
}
<span class="hljs-keyword">function</span> <span class="hljs-title function_">first</span>(<span class="hljs-params"></span>) {
  <span class="hljs-keyword">var</span> message = <span class="hljs-string">'first'</span>;
  <span class="hljs-title function_">second</span>();
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(message);
}
<span class="hljs-keyword">var</span> message = <span class="hljs-string">'default'</span>;
<span class="hljs-title function_">first</span>();
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(message);
</code></pre>
<!-- codeblock-end -->

- 1: undefined, first, default

- 2: default, default, default

- 3: first, first, default

- 4: undefined, undefined, undefined  

==================== Answer ====================  

Answer: 1

Each context(global or functional) has it's own variable environment and the callstack of variables in a LIFO order. So you can see the message variable value from second, first functions in an order followed by global context message variable value at the end.

==================== Id ====================  
518

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#518-What-is-the-output-of-below-code-in-an-ord

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
