==================== Question ====================  

### How do you display the current date in javascript  

==================== Answer ====================  

You can use `new Date()` to generate a new Date object containing the current date and time. For example, let's display the current date in mm/dd/yyyy

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> today = <span class="hljs-keyword">new</span> <span class="hljs-title class_">Date</span>();
<span class="hljs-keyword">var</span> dd = <span class="hljs-title class_">String</span>(today.<span class="hljs-title function_">getDate</span>()).<span class="hljs-title function_">padStart</span>(<span class="hljs-number">2</span>, <span class="hljs-string">'0'</span>);
<span class="hljs-keyword">var</span> mm = <span class="hljs-title class_">String</span>(today.<span class="hljs-title function_">getMonth</span>() + <span class="hljs-number">1</span>).<span class="hljs-title function_">padStart</span>(<span class="hljs-number">2</span>, <span class="hljs-string">'0'</span>); <span class="hljs-comment">//January is 0!</span>
<span class="hljs-keyword">var</span> yyyy = today.<span class="hljs-title function_">getFullYear</span>();
today = mm + <span class="hljs-string">'/'</span> + dd + <span class="hljs-string">'/'</span> + yyyy;
<span class="hljs-variable language_">document</span>.<span class="hljs-title function_">write</span>(today);
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
131

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#131-How-do-you-display-the-current-date-in-jav

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
