==================== Question ====================  

### How to convert string to title case with javascript  

==================== Answer ====================  

Title case means that the first letter of each word is capitalized. You can convert a string to title case using the below function,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">toTitleCase</span>(<span class="hljs-params">str</span>) {
  <span class="hljs-keyword">return</span> str.<span class="hljs-title function_">replace</span>(<span class="hljs-regexp">/\w\S*/g</span>, <span class="hljs-keyword">function</span> (<span class="hljs-params">txt</span>) {
     <span class="hljs-keyword">return</span> txt.<span class="hljs-title function_">charAt</span>(<span class="hljs-number">0</span>).<span class="hljs-title function_">toUpperCase</span>() + txt.<span class="hljs-title function_">substring</span>(<span class="hljs-number">1</span>).<span class="hljs-title function_">toLowerCase</span>();
  });
}
<span class="hljs-title function_">toTitleCase</span>(<span class="hljs-string">'good morning john'</span>); <span class="hljs-comment">// Good Morning John</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
182

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#182-How-to-convert-string-to-title-case-with-j

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
