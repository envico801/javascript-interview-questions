==================== Question ====================  

### How do you search a string for a pattern  

==================== Answer ====================  

You can use the test() method of regular expression in order to search a string for a pattern, and return true or false depending on the result.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> pattern = <span class="hljs-regexp">/you/</span>;
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(pattern.<span class="hljs-title function_">test</span>(<span class="hljs-string">'How are you?'</span>)); <span class="hljs-comment">//true</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
159

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#159-How-do-you-search-a-string-for-a-pattern

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
