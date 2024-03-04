==================== Question ====================  

### How do you print numbers with commas as thousand separators  

==================== Answer ====================  

You can use the `Number.prototype.toLocaleString()` method which returns a string with a language-sensitive representation such as thousand separator,currency etc of this number.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">convertToThousandFormat</span>(<span class="hljs-params">x</span>) {
  <span class="hljs-keyword">return</span> x.<span class="hljs-title function_">toLocaleString</span>(); <span class="hljs-comment">// 12,345.679</span>
}
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-title function_">convertToThousandFormat</span>(<span class="hljs-number">12345.6789</span>));
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
288

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#288-How-do-you-print-numbers-with-commas-as-th

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
