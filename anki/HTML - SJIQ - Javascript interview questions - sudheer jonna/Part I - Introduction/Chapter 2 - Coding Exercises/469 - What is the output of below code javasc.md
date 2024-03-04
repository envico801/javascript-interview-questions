==================== Question ====================  

### What is the output of below code

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> numbers = <span class="hljs-keyword">new</span> <span class="hljs-title class_">Set</span>([<span class="hljs-number">1</span>, <span class="hljs-number">1</span>, <span class="hljs-number">2</span>, <span class="hljs-number">3</span>, <span class="hljs-number">4</span>]);
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(numbers);
<span class="hljs-keyword">const</span> browser = <span class="hljs-keyword">new</span> <span class="hljs-title class_">Set</span>(<span class="hljs-string">'Firefox'</span>);
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(browser);
</code></pre>
<!-- codeblock-end -->

- 1: {1, 2, 3, 4}, {"F", "i", "r", "e", "f", "o", "x"}

- 2: {1, 2, 3, 4}, {"F", "i", "r", "e", "o", "x"}

- 3: [1, 2, 3, 4], ["F", "i", "r", "e", "o", "x"]

- 4: {1, 1, 2, 3, 4}, {"F", "i", "r", "e", "f", "o", "x"}  

==================== Answer ====================  

Answer: 1

Since `Set` object is a collection of unique values, it won't allow duplicate values in the collection. At the same time, it is case sensitive data structure.

==================== Id ====================  
469

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#469-What-is-the-output-of-below-code-javasc

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
