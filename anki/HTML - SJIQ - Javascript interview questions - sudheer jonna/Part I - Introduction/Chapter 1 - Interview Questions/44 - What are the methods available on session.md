==================== Question ====================  

### What are the methods available on session storage  

==================== Answer ====================  

The session storage provided methods for reading, writing and clearing the session data

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-comment">// Save data to sessionStorage</span>
<span class="hljs-variable language_">sessionStorage</span>.<span class="hljs-title function_">setItem</span>(<span class="hljs-string">'key'</span>, <span class="hljs-string">'value'</span>);
<span class="hljs-comment">// Get saved data from sessionStorage</span>
<span class="hljs-keyword">let</span> data = <span class="hljs-variable language_">sessionStorage</span>.<span class="hljs-title function_">getItem</span>(<span class="hljs-string">'key'</span>);
<span class="hljs-comment">// Remove saved data from sessionStorage</span>
<span class="hljs-variable language_">sessionStorage</span>.<span class="hljs-title function_">removeItem</span>(<span class="hljs-string">'key'</span>);
<span class="hljs-comment">// Remove all saved data from sessionStorage</span>
<span class="hljs-variable language_">sessionStorage</span>.<span class="hljs-title function_">clear</span>();
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
44

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#44-What-are-the-methods-available-on-session

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
