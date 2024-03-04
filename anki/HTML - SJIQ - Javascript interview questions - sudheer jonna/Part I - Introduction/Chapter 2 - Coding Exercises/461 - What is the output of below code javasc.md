==================== Question ====================  

### What is the output of below code

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> <span class="hljs-title function_">printNumbersArrow</span> = (<span class="hljs-params">first, second, first</span>) => {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(first, second, first);
};
<span class="hljs-title function_">printNumbersArrow</span>(<span class="hljs-number">1</span>, <span class="hljs-number">2</span>, <span class="hljs-number">3</span>);
</code></pre>
<!-- codeblock-end -->

- 1: 1, 2, 3

- 2: 3, 2, 3

- 3: SyntaxError: Duplicate parameter name not allowed in this context

- 4: 1, 2, 1  

==================== Answer ====================  

Answer: 3

Unlike regular functions, the arrow functions doesn't not allow duplicate parameters in either strict or non-strict mode. So you can see `SyntaxError` in the console.

==================== Id ====================  
461

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#461-What-is-the-output-of-below-code-javasc

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
