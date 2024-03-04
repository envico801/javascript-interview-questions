==================== Question ====================  

### What is the output of below code

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">outer</span>(<span class="hljs-params">f = inner()</span>) {
  <span class="hljs-keyword">function</span> <span class="hljs-title function_">inner</span>(<span class="hljs-params"></span>) {
     <span class="hljs-keyword">return</span> <span class="hljs-string">'Inner'</span>;
  }
}
<span class="hljs-title function_">outer</span>();
</code></pre>
<!-- codeblock-end -->

- 1: ReferenceError

- 2: Inner  

==================== Answer ====================  

Answer: 1

The functions and variables declared in the function body cannot be referred from default value parameter initializers. If you still try to access, it throws a run-time ReferenceError(i.e, `inner` is not defined).

==================== Id ====================  
490

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#490-What-is-the-output-of-below-code-javasc

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
