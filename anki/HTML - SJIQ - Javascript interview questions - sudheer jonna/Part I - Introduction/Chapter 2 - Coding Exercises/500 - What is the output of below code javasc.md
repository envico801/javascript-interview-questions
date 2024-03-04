==================== Question ====================  

### What is the output of below code

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> <span class="hljs-variable constant_">USER</span> = { <span class="hljs-attr">age</span>: <span class="hljs-number">30</span> };
<span class="hljs-variable constant_">USER</span>.<span class="hljs-property">age</span> = <span class="hljs-number">25</span>;
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-variable constant_">USER</span>.<span class="hljs-property">age</span>);
</code></pre>
<!-- codeblock-end -->

- 1: 30

- 2: 25

- 3: Uncaught TypeError

- 4: SyntaxError  

==================== Answer ====================  

Answer: 2

Even though we used constant variables, the content of it is an object and the object's contents (e.g properties) can be altered. Hence, the change is going to be valid in this case.

==================== Id ====================  
500

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#500-What-is-the-output-of-below-code-javasc

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
