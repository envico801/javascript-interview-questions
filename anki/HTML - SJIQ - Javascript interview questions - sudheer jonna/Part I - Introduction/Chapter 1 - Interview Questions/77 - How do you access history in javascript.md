==================== Question ====================  

### How do you access history in javascript  

==================== Answer ====================  

The window.history object contains the browser's history. You can load previous and next URLs in the history using back() and next() methods.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">goBack</span>(<span class="hljs-params"></span>) {
  <span class="hljs-variable language_">window</span>.<span class="hljs-property">history</span>.<span class="hljs-title function_">back</span>();
}
<span class="hljs-keyword">function</span> <span class="hljs-title function_">goForward</span>(<span class="hljs-params"></span>) {
  <span class="hljs-variable language_">window</span>.<span class="hljs-property">history</span>.<span class="hljs-title function_">forward</span>();
}
</code></pre>
<!-- codeblock-end -->

**Note:** You can also access history without window prefix.

==================== Id ====================  
77

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#77-How-do-you-access-history-in-javascript

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
