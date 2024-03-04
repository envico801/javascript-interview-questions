==================== Question ====================  

### How do you get the current url with javascript  

==================== Answer ====================  

You can use `window.location.href` expression to get the current url path and you can use the same expression for updating the URL too. You can also use `document.URL` for read-only purposes but this solution has issues in FF.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'location.href'</span>, <span class="hljs-variable language_">window</span>.<span class="hljs-property">location</span>.<span class="hljs-property">href</span>); <span class="hljs-comment">// Returns full URL</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
122

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#122-How-do-you-get-the-current-url-with-javasc

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
