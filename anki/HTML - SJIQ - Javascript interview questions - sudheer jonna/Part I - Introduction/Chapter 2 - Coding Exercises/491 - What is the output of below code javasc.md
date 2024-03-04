==================== Question ====================  

### What is the output of below code

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">myFun</span>(<span class="hljs-params">x, y, ...manyMoreArgs</span>) {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(manyMoreArgs);
}
<span class="hljs-title function_">myFun</span>(<span class="hljs-number">1</span>, <span class="hljs-number">2</span>, <span class="hljs-number">3</span>, <span class="hljs-number">4</span>, <span class="hljs-number">5</span>);
<span class="hljs-title function_">myFun</span>(<span class="hljs-number">1</span>, <span class="hljs-number">2</span>);
</code></pre>
<!-- codeblock-end -->

- 1: [3, 4, 5], undefined

- 2: SyntaxError

- 3: [3, 4, 5], []

- 4: [3, 4, 5], [undefined]  

==================== Answer ====================  

Answer: 3

The rest parameter is used to hold the remaining parameters of a function and it becomes an empty array if the argument is not provided.

==================== Id ====================  
491

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#491-What-is-the-output-of-below-code-javasc

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
