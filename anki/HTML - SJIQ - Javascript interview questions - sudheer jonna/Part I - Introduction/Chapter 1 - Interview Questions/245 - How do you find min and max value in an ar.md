==================== Question ====================  

### How do you find min and max value in an array  

==================== Answer ====================  

You can use `Math.min` and `Math.max` methods on array variables to find the minimum and maximum elements within an array. Let's create two functions to find the min and max value with in an array,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> marks = [<span class="hljs-number">50</span>, <span class="hljs-number">20</span>, <span class="hljs-number">70</span>, <span class="hljs-number">60</span>, <span class="hljs-number">45</span>, <span class="hljs-number">30</span>];
<span class="hljs-keyword">function</span> <span class="hljs-title function_">findMin</span>(<span class="hljs-params">arr</span>) {
  <span class="hljs-keyword">return</span> <span class="hljs-title class_">Math</span>.<span class="hljs-property">min</span>.<span class="hljs-title function_">apply</span>(<span class="hljs-literal">null</span>, arr);
}
<span class="hljs-keyword">function</span> <span class="hljs-title function_">findMax</span>(<span class="hljs-params">arr</span>) {
  <span class="hljs-keyword">return</span> <span class="hljs-title class_">Math</span>.<span class="hljs-property">max</span>.<span class="hljs-title function_">apply</span>(<span class="hljs-literal">null</span>, arr);
}
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-title function_">findMin</span>(marks));
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-title function_">findMax</span>(marks));
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
245

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#245-How-do-you-find-min-and-max-value-in-an-ar

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
