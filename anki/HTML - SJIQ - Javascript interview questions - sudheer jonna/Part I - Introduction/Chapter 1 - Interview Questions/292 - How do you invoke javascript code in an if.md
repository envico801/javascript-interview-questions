==================== Question ====================  

### How do you invoke javascript code in an iframe from parent page  

==================== Answer ====================  

Initially iFrame needs to be accessed using either `document.getElementBy` or `window.frames`. After that `contentWindow` property of iFrame gives the access for targetFunction

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-variable language_">document</span>.<span class="hljs-title function_">getElementById</span>(<span class="hljs-string">'targetFrame'</span>).<span class="hljs-property">contentWindow</span>.<span class="hljs-title function_">targetFunction</span>();
<span class="hljs-variable language_">window</span>.<span class="hljs-property">frames</span>[<span class="hljs-number">0</span>].<span class="hljs-property">frameElement</span>.<span class="hljs-property">contentWindow</span>.<span class="hljs-title function_">targetFunction</span>(); <span class="hljs-comment">// Accessing iframe this way may not work in latest versions chrome and firefox</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
292

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#292-How-do-you-invoke-javascript-code-in-an-if

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
