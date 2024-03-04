==================== Question ====================  

### What is the output of below code in non strict mode?

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">let</span> msg = <span class="hljs-string">'Good morning!!'</span>;
msg.<span class="hljs-property">name</span> = <span class="hljs-string">'John'</span>;
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(msg.<span class="hljs-property">name</span>);
</code></pre>
<!-- codeblock-end -->

- 1: ""

- 2: Error

- 3: John

- 4: Undefined  

==================== Answer ====================  

Answer: 4

It returns undefined for non-strict mode and returns Error for strict mode. In non-strict mode, the wrapper object is going to be created and get the mentioned property. But the object get disappeared after accessing the property in next line.

==================== Id ====================  
504

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#504-What-is-the-output-of-below-code-in-non-st

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
