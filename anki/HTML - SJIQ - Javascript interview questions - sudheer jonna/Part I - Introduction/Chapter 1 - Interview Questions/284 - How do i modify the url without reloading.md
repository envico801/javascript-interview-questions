==================== Question ====================  

### How do I modify the url without reloading the page  

==================== Answer ====================  

The `window.location.href` property will be helpful to modify the url but it reloads the page. HTML5 introduced the `history.pushState()` and `history.replaceState()` methods, which allow you to add and modify history entries, respectively. For example, you can use pushState as below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-variable language_">window</span>.<span class="hljs-property">history</span>.<span class="hljs-title function_">pushState</span>(<span class="hljs-string">'page2'</span>, <span class="hljs-string">'Title'</span>, <span class="hljs-string">'/page2.html'</span>);
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
284

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#284-How-do-i-modify-the-url-without-reloading

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
