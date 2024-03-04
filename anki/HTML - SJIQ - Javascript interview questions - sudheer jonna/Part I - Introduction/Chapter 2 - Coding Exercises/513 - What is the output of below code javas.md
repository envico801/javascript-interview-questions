==================== Question ====================  

### What is the output of below code?

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> numbers = [<span class="hljs-number">11</span>, <span class="hljs-number">25</span>, <span class="hljs-number">31</span>, <span class="hljs-number">23</span>, <span class="hljs-number">33</span>, <span class="hljs-number">18</span>, <span class="hljs-number">200</span>];
numbers.<span class="hljs-title function_">sort</span>();
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(numbers);
</code></pre>
<!-- codeblock-end -->

- 1: [11, 18, 23, 25, 31, 33, 200]

- 2: [11, 18, 200, 23, 25, 31, 33]

- 3: [11, 25, 31, 23, 33, 18, 200]

- 4: Cannot sort numbers  

==================== Answer ====================  

Answer: 2

By default, the sort method sorts elements alphabetically. This is because elemented converted to strings and strings compared in UTF-16 code units order. Hence, you will see the above numbers not sorted as expected. In order to sort numerically just supply a comparator function which handles numeric sorts.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> numbers = [<span class="hljs-number">11</span>, <span class="hljs-number">25</span>, <span class="hljs-number">31</span>, <span class="hljs-number">23</span>, <span class="hljs-number">33</span>, <span class="hljs-number">18</span>, <span class="hljs-number">200</span>];
numbers.<span class="hljs-title function_">sort</span>(<span class="hljs-function">(<span class="hljs-params">a, b</span>) =></span> a - b);
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(numbers);
</code></pre>
<!-- codeblock-end -->

**Note:** Sort() method changes the original array.

==================== Id ====================  
513

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#513-What-is-the-output-of-below-code-javas

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
