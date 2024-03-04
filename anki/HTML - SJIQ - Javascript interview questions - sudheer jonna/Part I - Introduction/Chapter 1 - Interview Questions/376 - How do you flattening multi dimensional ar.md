==================== Question ====================  

### How do you flattening multi dimensional arrays  

==================== Answer ====================  

Flattening bi-dimensional arrays is trivial with Spread operator.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> biDimensionalArr = [<span class="hljs-number">11</span>, [<span class="hljs-number">22</span>, <span class="hljs-number">33</span>], [<span class="hljs-number">44</span>, <span class="hljs-number">55</span>], [<span class="hljs-number">66</span>, <span class="hljs-number">77</span>], <span class="hljs-number">88</span>, <span class="hljs-number">99</span>];
<span class="hljs-keyword">const</span> flattenArr = [].<span class="hljs-title function_">concat</span>(...biDimensionalArr); <span class="hljs-comment">// [11, 22, 33, 44, 55, 66, 77, 88, 99]</span>
</code></pre>
<!-- codeblock-end -->

But you can make it work with multi-dimensional arrays by recursive calls,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">flattenMultiArray</span>(<span class="hljs-params">arr</span>) {
  <span class="hljs-keyword">const</span> flattened = [].<span class="hljs-title function_">concat</span>(...arr);
  <span class="hljs-keyword">return</span> flattened.<span class="hljs-title function_">some</span>(<span class="hljs-function">(<span class="hljs-params">item</span>) =></span> <span class="hljs-title class_">Array</span>.<span class="hljs-title function_">isArray</span>(item)) ? <span class="hljs-title function_">flattenMultiArray</span>(flattened) : flattened;
}
<span class="hljs-keyword">const</span> multiDimensionalArr = [<span class="hljs-number">11</span>, [<span class="hljs-number">22</span>, <span class="hljs-number">33</span>], [<span class="hljs-number">44</span>, [<span class="hljs-number">55</span>, <span class="hljs-number">66</span>, [<span class="hljs-number">77</span>, [<span class="hljs-number">88</span>]], <span class="hljs-number">99</span>]]];
<span class="hljs-keyword">const</span> flatArr = <span class="hljs-title function_">flattenMultiArray</span>(multiDimensionalArr); <span class="hljs-comment">// [11, 22, 33, 44, 55, 66, 77, 88, 99]</span>
</code></pre>
<!-- codeblock-end -->

Also you can use the `flat` method of Array.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> arr = [<span class="hljs-number">1</span>, [<span class="hljs-number">2</span>, <span class="hljs-number">3</span>], <span class="hljs-number">4</span>, <span class="hljs-number">5</span>, [<span class="hljs-number">6</span>, <span class="hljs-number">7</span>]];
<span class="hljs-keyword">const</span> fllattenArr = arr.<span class="hljs-title function_">flat</span>(); <span class="hljs-comment">// [1, 2, 3, 4, 5, 6, 7]</span>
<span class="hljs-comment">// And for multiDemensional arrays</span>
<span class="hljs-keyword">const</span> multiDimensionalArr = [<span class="hljs-number">11</span>, [<span class="hljs-number">22</span>, <span class="hljs-number">33</span>], [<span class="hljs-number">44</span>, [<span class="hljs-number">55</span>, <span class="hljs-number">66</span>, [<span class="hljs-number">77</span>, [<span class="hljs-number">88</span>]], <span class="hljs-number">99</span>]]];
<span class="hljs-keyword">const</span> oneStepFlat = multiDimensionalArr.<span class="hljs-title function_">flat</span>(<span class="hljs-number">1</span>); <span class="hljs-comment">// [11, 22, 33, 44, [55, 66, [77, [88]], 99]]</span>
<span class="hljs-keyword">const</span> towStep = multiDimensionalArr.<span class="hljs-title function_">flat</span>(<span class="hljs-number">2</span>); <span class="hljs-comment">// [11, 22, 33, 44, 55, 66, [77, [88]], 99]</span>
<span class="hljs-keyword">const</span> fullyFlatArray = multiDimensionalArr.<span class="hljs-title function_">flat</span>(<span class="hljs-title class_">Infinity</span>); <span class="hljs-comment">// [11, 22, 33, 44, 55, 66, 77, 88, 99]</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
376

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#376-How-do-you-flattening-multi-dimensional-ar

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
