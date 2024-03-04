==================== Question ====================  

### What is the output of below code?

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'First line'</span>)[(<span class="hljs-string">'a'</span>, <span class="hljs-string">'b'</span>, <span class="hljs-string">'c'</span>)].<span class="hljs-title function_">forEach</span>(<span class="hljs-function">(<span class="hljs-params">element</span>) =></span> <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(element));
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'Third line'</span>);
</code></pre>
<!-- codeblock-end -->

- 1: `First line`, then print `a, b, c` in a new line, and finally print `Third line` as next line

- 2: `First line`, then print `a, b, c` in a first line, and print `Third line` as next line

- 3: Missing semi-colon error

- 4: Cannot read properties of undefined  

==================== Answer ====================  

Answer: 4

When JavaScript encounters a line break without a semicolon, the JavaScript parser will automatically add a semicolon based on a set of rules called `Automatic Semicolon Insertion` which determines whether line break as end of statement or not to insert semicolon. But it does not assume a semicolon before square brackets [...]. So the first two lines considered as a single statement as below.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'First line'</span>)[(<span class="hljs-string">'a'</span>, <span class="hljs-string">'b'</span>, <span class="hljs-string">'c'</span>)].<span class="hljs-title function_">forEach</span>(<span class="hljs-function">(<span class="hljs-params">element</span>) =></span> <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(element));
</code></pre>
<!-- codeblock-end -->

Hence, there will be **cannot read properties of undefined** error while applying the array square bracket on log function.

==================== Id ====================  
510

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#510-What-is-the-output-of-below-code-javas

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
