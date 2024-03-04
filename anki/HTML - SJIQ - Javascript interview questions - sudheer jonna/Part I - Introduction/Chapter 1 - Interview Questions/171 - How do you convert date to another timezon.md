==================== Question ====================  

### How do you convert date to another timezone in javascript  

==================== Answer ====================  

You can use the toLocaleString() method to convert dates in one timezone to another. For example, let's convert current date to British English timezone as below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(event.<span class="hljs-title function_">toLocaleString</span>(<span class="hljs-string">'en-GB'</span>, { <span class="hljs-attr">timeZone</span>: <span class="hljs-string">'UTC'</span> })); <span class="hljs-comment">//29/06/2019, 09:56:00</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
171

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#171-How-do-you-convert-date-to-another-timezon

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
