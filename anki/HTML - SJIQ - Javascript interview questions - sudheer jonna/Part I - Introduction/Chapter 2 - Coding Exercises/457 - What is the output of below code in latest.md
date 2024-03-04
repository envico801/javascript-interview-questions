==================== Question ====================  

### What is the output of below code in latest Chrome

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> array1 = <span class="hljs-keyword">new</span> <span class="hljs-title class_">Array</span>(<span class="hljs-number">3</span>);
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(array1);
<span class="hljs-keyword">var</span> array2 = [];
array2[<span class="hljs-number">2</span>] = <span class="hljs-number">100</span>;
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(array2);
<span class="hljs-keyword">var</span> array3 = [, , ,];
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(array3);
</code></pre>
<!-- codeblock-end -->

- 1: [undefined × 3], [undefined × 2, 100], [undefined × 3]

- 2: [empty × 3], [empty × 2, 100], [empty × 3]

- 3: [null × 3], [null × 2, 100], [null × 3]

- 4: [], [100], []  

==================== Answer ====================  

Answer: 2

The latest chrome versions display `sparse array`(they are filled with holes) using this empty x n notation. Whereas the older versions have undefined x n notation.

**Note:** The latest version of FF displays `n empty slots` notation.

==================== Id ====================  
457

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#457-What-is-the-output-of-below-code-in-latest

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
