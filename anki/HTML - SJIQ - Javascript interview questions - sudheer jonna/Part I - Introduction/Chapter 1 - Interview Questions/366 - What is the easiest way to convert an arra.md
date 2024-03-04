==================== Question ====================  

### What is the easiest way to convert an array to an object  

==================== Answer ====================  

You can convert an array to an object with the same data using spread(...) operator.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> fruits = [<span class="hljs-string">'banana'</span>, <span class="hljs-string">'apple'</span>, <span class="hljs-string">'orange'</span>, <span class="hljs-string">'watermelon'</span>];
<span class="hljs-keyword">var</span> fruitsObject = { ...fruits };
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(fruitsObject); <span class="hljs-comment">// {0: "banana", 1: "apple", 2: "orange", 3: "watermelon"}</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
366

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#366-What-is-the-easiest-way-to-convert-an-arra

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
