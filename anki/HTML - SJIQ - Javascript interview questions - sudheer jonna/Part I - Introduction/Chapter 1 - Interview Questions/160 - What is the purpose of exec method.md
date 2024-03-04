==================== Question ====================  

### What is the purpose of exec method  

==================== Answer ====================  

The purpose of exec method is similar to test method but it executes a search for a match in a specified string and returns a result array, or null instead of returning true/false.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> pattern = <span class="hljs-regexp">/you/</span>;
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(pattern.<span class="hljs-title function_">exec</span>(<span class="hljs-string">'How are you?'</span>)); <span class="hljs-comment">//["you", index: 8, input: "How are you?", groups: undefined]</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
160

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#160-What-is-the-purpose-of-exec-method

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
