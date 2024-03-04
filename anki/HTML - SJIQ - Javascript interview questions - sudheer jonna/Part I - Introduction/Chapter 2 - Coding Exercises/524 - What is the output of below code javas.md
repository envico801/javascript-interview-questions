==================== Question ====================  

### What is the output of below code?

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> a = <span class="hljs-keyword">new</span> <span class="hljs-title class_">Number</span>(<span class="hljs-number">10</span>);
<span class="hljs-keyword">const</span> b = <span class="hljs-number">10</span>;
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(a === b);
</code></pre>
<!-- codeblock-end -->

- 1: False

- 2: True  

==================== Answer ====================  

Answer: 1

Eventhough both variables `a` and `b` refer a number value, the first declaration is based on constructor function and the type of the variable is going to be `object` type. Whereas the second declaration is primitive assignment with a number and the type is `number` type. Hence, the equality operator `===` will output `false` value.

==================== Id ====================  
524

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#524-What-is-the-output-of-below-code-javas

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
