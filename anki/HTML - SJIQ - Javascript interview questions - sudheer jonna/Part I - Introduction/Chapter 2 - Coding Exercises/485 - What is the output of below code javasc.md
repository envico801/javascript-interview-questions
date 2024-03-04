==================== Question ====================  

### What is the output of below code

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">area</span>(<span class="hljs-params">{ length = <span class="hljs-number">10</span>, width = <span class="hljs-number">20</span> }</span>) {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(length * width);
}
<span class="hljs-title function_">area</span>();
</code></pre>
<!-- codeblock-end -->

- 1: 200

- 2: Error

- 3: undefined

- 4: 0  

==================== Answer ====================  

Answer: 2

If you leave out the right-hand side assignment for the destructuring object, the function will look for at least one argument to be supplied when invoked. Otherwise you will receive an error `Error: Cannot read property 'length' of undefined` as mentioned above.

You can avoid the error with either of the below changes,

1. **Pass at least an empty object:**

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">area</span>(<span class="hljs-params">{ length = <span class="hljs-number">10</span>, width = <span class="hljs-number">20</span> }</span>) {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(length * width);
}
<span class="hljs-title function_">area</span>({});
</code></pre>
<!-- codeblock-end -->

2. **Assign default empty object:**

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">area</span>(<span class="hljs-params">{ length = <span class="hljs-number">10</span>, width = <span class="hljs-number">20</span> } = {}</span>) {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(length * width);
}
<span class="hljs-title function_">area</span>();
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
485

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#485-What-is-the-output-of-below-code-javasc

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
