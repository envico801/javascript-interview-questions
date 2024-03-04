==================== Question ====================  

### What is the output of below code

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">add</span>(<span class="hljs-params">item, items = []</span>) {
  items.<span class="hljs-title function_">push</span>(item);
  <span class="hljs-keyword">return</span> items;
}
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-title function_">add</span>(<span class="hljs-string">'Orange'</span>));
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-title function_">add</span>(<span class="hljs-string">'Apple'</span>));
</code></pre>
<!-- codeblock-end -->

- 1: ['Orange'], ['Orange', 'Apple']

- 2: ['Orange'], ['Apple']  

==================== Answer ====================  

Answer: 2

Since the default argument is evaluated at call time, a new object is created each time the function is called. So in this case, the new array is created and an element pushed to the default empty array.

==================== Id ====================  
488

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#488-What-is-the-output-of-below-code-javasc

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
