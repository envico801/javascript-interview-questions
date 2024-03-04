==================== Question ====================  

### How do you check whether an array includes a particular value or not  

==================== Answer ====================  

The `Array#includes()` method is used to determine whether an array includes a particular value among its entries by returning either true or false. Let's see an example to find an element(numeric and string) within an array.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> numericArray = [<span class="hljs-number">1</span>, <span class="hljs-number">2</span>, <span class="hljs-number">3</span>, <span class="hljs-number">4</span>];
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(numericArray.<span class="hljs-title function_">includes</span>(<span class="hljs-number">3</span>)); <span class="hljs-comment">// true</span>
<span class="hljs-keyword">var</span> stringArray = [<span class="hljs-string">'green'</span>, <span class="hljs-string">'yellow'</span>, <span class="hljs-string">'blue'</span>];
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(stringArray.<span class="hljs-title function_">includes</span>(<span class="hljs-string">'blue'</span>)); <span class="hljs-comment">//true</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
285

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#285-How-do-you-check-whether-an-array-includes

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
