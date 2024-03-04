==================== Question ====================  

### When you get a syntax error  

==================== Answer ====================  

A SyntaxError is thrown if you try to evaluate code with a syntax error. For example, the below missing quote for the function parameter throws a syntax error

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">try</span> {
  <span class="hljs-built_in">eval</span>(<span class="hljs-string">"greeting('welcome)"</span>); <span class="hljs-comment">// Missing ' will produce an error</span>
} <span class="hljs-keyword">catch</span> (err) {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(err.<span class="hljs-property">name</span>);
}
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
227

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#227-When-you-get-a-syntax-error

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
