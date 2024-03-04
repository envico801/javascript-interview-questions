==================== Question ====================  

### What is the output of below code

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>([<span class="hljs-number">1</span>, <span class="hljs-number">2</span>] + [<span class="hljs-number">3</span>, <span class="hljs-number">4</span>]);
</code></pre>
<!-- codeblock-end -->

- 1: [1,2,3,4]

- 2: [1,2][3,4]

- 3: SyntaxError

- 4: 1,23,4  

==================== Answer ====================  

Answer: 4

The + operator is not meant or defined for arrays. So it converts arrays into strings and concatenates them.

==================== Id ====================  
468

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#468-What-is-the-output-of-below-code-javasc

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
