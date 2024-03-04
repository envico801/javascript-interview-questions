==================== Question ====================  

### How do get query string values in javascript  

==================== Answer ====================  

You can use URLSearchParams to get query string values in javascript. Let's see an example to get the client code value from URL query string,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> urlParams = <span class="hljs-keyword">new</span> <span class="hljs-title class_">URLSearchParams</span>(<span class="hljs-variable language_">window</span>.<span class="hljs-property">location</span>.<span class="hljs-property">search</span>);
<span class="hljs-keyword">const</span> clientCode = urlParams.<span class="hljs-title function_">get</span>(<span class="hljs-string">'clientCode'</span>);
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
124

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#124-How-do-get-query-string-values-in-javascri

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
