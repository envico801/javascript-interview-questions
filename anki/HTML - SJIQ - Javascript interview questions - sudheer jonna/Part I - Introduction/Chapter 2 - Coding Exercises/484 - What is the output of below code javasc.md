==================== Question ====================  

### What is the output of below code

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> { <span class="hljs-attr">a</span>: x = <span class="hljs-number">10</span>, <span class="hljs-attr">b</span>: y = <span class="hljs-number">20</span> } = { <span class="hljs-attr">a</span>: <span class="hljs-number">30</span> };
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(x);
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(y);
</code></pre>
<!-- codeblock-end -->

- 1: 30, 20

- 2: 10, 20

- 3: 10, undefined

- 4: 30, undefined  

==================== Answer ====================  

Answer: 1

The object property follows below rules,

1. The object properties can be retrieved and assigned to a variable with a different name

2. The property assigned a default value when the retrieved value is `undefined`

==================== Id ====================  
484

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#484-What-is-the-output-of-below-code-javasc

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
