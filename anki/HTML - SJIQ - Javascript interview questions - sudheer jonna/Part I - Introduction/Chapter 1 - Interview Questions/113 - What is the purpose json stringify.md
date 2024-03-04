==================== Question ====================  

### What is the purpose JSON stringify  

==================== Answer ====================  

When sending data to a web server, the data has to be in a string format. You can achieve this by converting JSON object into a string using stringify() method.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> userJSON = { <span class="hljs-attr">name</span>: <span class="hljs-string">'John'</span>, <span class="hljs-attr">age</span>: <span class="hljs-number">31</span> };
<span class="hljs-keyword">var</span> userString = <span class="hljs-title class_">JSON</span>.<span class="hljs-title function_">stringify</span>(userJSON);
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(userString); <span class="hljs-comment">//"{"name":"John","age":31}"</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
113

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#113-What-is-the-purpose-json-stringify

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
