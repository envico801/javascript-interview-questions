==================== Question ====================  

### What is the output of below code

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">let</span> [a, ...b] = [<span class="hljs-number">1</span>, <span class="hljs-number">2</span>, <span class="hljs-number">3</span>, <span class="hljs-number">4</span>, <span class="hljs-number">5</span>];
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(a, b);
</code></pre>
<!-- codeblock-end -->

- 1: 1, [2, 3, 4, 5]

- 2: 1, {2, 3, 4, 5}

- 3: SyntaxError

- 4: 1, [2, 3, 4]  

==================== Answer ====================  

Answer: 3

When using rest parameters, trailing commas are not allowed and will throw a SyntaxError.

If you remove the trailing comma then it displays 1st answer

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">let</span> [a, ...b] = [<span class="hljs-number">1</span>, <span class="hljs-number">2</span>, <span class="hljs-number">3</span>, <span class="hljs-number">4</span>, <span class="hljs-number">5</span>];
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(a, b); <span class="hljs-comment">// 1, [2, 3, 4, 5]</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
472

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#472-What-is-the-output-of-below-code-javasc

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
