==================== Question ====================  

### How do get the timezone offset from date  

==================== Answer ====================  

You can use the `getTimezoneOffset` method of the date object. This method returns the time zone difference, in minutes, from current locale (host system settings) to UTC

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> offset = <span class="hljs-keyword">new</span> <span class="hljs-title class_">Date</span>().<span class="hljs-title function_">getTimezoneOffset</span>();
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(offset); <span class="hljs-comment">// -480</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
293

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#293-How-do-get-the-timezone-offset-from-date

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
