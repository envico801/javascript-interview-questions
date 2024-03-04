==================== Question ====================  

### How do you parse JSON string  

==================== Answer ====================  

When receiving the data from a web server, the data is always in a string format. But you can convert this string value to a javascript object using parse() method.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> userString = <span class="hljs-string">'{"name":"John","age":31}'</span>;
<span class="hljs-keyword">var</span> userJSON = <span class="hljs-title class_">JSON</span>.<span class="hljs-title function_">parse</span>(userString);
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(userJSON); <span class="hljs-comment">// {name: "John", age: 31}</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
114

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#114-How-do-you-parse-json-string

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
