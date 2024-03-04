==================== Question ====================  

### How do you find min and max values without Math functions  

==================== Answer ====================  

You can write functions which loop through an array comparing each value with the lowest value or highest value to find the min and max values. Let's create those functions to find min and max values,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> marks = [<span class="hljs-number">50</span>, <span class="hljs-number">20</span>, <span class="hljs-number">70</span>, <span class="hljs-number">60</span>, <span class="hljs-number">45</span>, <span class="hljs-number">30</span>];
<span class="hljs-keyword">function</span> <span class="hljs-title function_">findMin</span>(<span class="hljs-params">arr</span>) {
  <span class="hljs-keyword">var</span> length = arr.<span class="hljs-property">length</span>;
  <span class="hljs-keyword">var</span> min = <span class="hljs-title class_">Infinity</span>;
  <span class="hljs-keyword">while</span> (length--) {
     <span class="hljs-keyword">if</span> (arr[length] &#x3C; min) {
       min = arr[length];
     }
  }
  <span class="hljs-keyword">return</span> min;
}
<span class="hljs-keyword">function</span> <span class="hljs-title function_">findMax</span>(<span class="hljs-params">arr</span>) {
  <span class="hljs-keyword">var</span> length = arr.<span class="hljs-property">length</span>;
  <span class="hljs-keyword">var</span> max = -<span class="hljs-title class_">Infinity</span>;
  <span class="hljs-keyword">while</span> (length--) {
     <span class="hljs-keyword">if</span> (arr[length] > max) {
       max = arr[length];
     }
  }
  <span class="hljs-keyword">return</span> max;
}
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-title function_">findMin</span>(marks));
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-title function_">findMax</span>(marks));
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
246

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#246-How-do-you-find-min-and-max-values-without

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
