==================== Question ====================  

### What are js labels  

==================== Answer ====================  

The label statement allows us to name loops and blocks in JavaScript. We can then use these labels to refer back to the code later. For example, the below code with labels avoids printing the numbers when they are same,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> i, j;
<span class="hljs-attr">loop1</span>: <span class="hljs-keyword">for</span> (i = <span class="hljs-number">0</span>; i &#x3C; <span class="hljs-number">3</span>; i++) {
  <span class="hljs-attr">loop2</span>: <span class="hljs-keyword">for</span> (j = <span class="hljs-number">0</span>; j &#x3C; <span class="hljs-number">3</span>; j++) {
     <span class="hljs-keyword">if</span> (i === j) {
       <span class="hljs-keyword">continue</span> loop1;
     }
     <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'i = '</span> + i + <span class="hljs-string">', j = '</span> + j);
  }
}
<span class="hljs-comment">// Output is:</span>
<span class="hljs-comment">//   "i = 1, j = 0"</span>
<span class="hljs-comment">//   "i = 2, j = 0"</span>
<span class="hljs-comment">//   "i = 2, j = 1"</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
144

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#144-What-are-js-labels

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
