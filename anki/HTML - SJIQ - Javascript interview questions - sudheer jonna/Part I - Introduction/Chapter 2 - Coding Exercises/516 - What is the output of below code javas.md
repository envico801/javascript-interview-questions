==================== Question ====================  

### What is the output of below code?

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-title function_">message</span>();
<span class="hljs-keyword">function</span> <span class="hljs-title function_">message</span>(<span class="hljs-params"></span>) {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'Hello'</span>);
}
<span class="hljs-keyword">function</span> <span class="hljs-title function_">message</span>(<span class="hljs-params"></span>) {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'Bye'</span>);
}
</code></pre>
<!-- codeblock-end -->

- 1: Reference error: message is not defined

- 2: Hello

- 3: Bye

- 4: Compile time error  

==================== Answer ====================  

Answer: 3

As part of hoisting, initially JavaScript Engine or compiler will store first function in heap memory but later rewrite or replaces with redefined function content.

==================== Id ====================  
516

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#516-What-is-the-output-of-below-code-javas

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
