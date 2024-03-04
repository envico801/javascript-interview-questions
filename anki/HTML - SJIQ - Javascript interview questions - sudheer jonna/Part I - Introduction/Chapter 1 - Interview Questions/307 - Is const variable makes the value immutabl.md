==================== Question ====================  

### Is const variable makes the value immutable  

==================== Answer ====================  

No, the const variable doesn't make the value immutable. But it disallows subsequent assignments(i.e, You can declare with assignment but can't assign another value later)

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> userList = [];
userList.<span class="hljs-title function_">push</span>(<span class="hljs-string">'John'</span>); <span class="hljs-comment">// Can mutate even though it can't re-assign</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(userList); <span class="hljs-comment">// ['John']</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
307

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#307-Is-const-variable-makes-the-value-immutabl

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
