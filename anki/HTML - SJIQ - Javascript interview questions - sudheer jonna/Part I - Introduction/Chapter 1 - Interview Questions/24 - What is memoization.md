==================== Question ====================  

### What is memoization  

==================== Answer ====================  

Memoization is a functional programming technique which attempts to increase a function’s performance by caching its previously computed results. Each time a memoized function is called, its parameters are used to index the cache. If the data is present, then it can be returned, without executing the entire function. Otherwise the function is executed and then the result is added to the cache.

Let's take an example of adding function with memoization,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> <span class="hljs-title function_">memoizAddition</span> = (<span class="hljs-params"></span>) => {
  <span class="hljs-keyword">let</span> cache = {};
  <span class="hljs-keyword">return</span> <span class="hljs-function">(<span class="hljs-params">value</span>) =></span> {
     <span class="hljs-keyword">if</span> (value <span class="hljs-keyword">in</span> cache) {
       <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'Fetching from cache'</span>);
       <span class="hljs-keyword">return</span> cache[value]; <span class="hljs-comment">// Here, cache.value cannot be used as property name starts with the number which is not a valid JavaScript  identifier. Hence, can only be accessed using the square bracket notation.</span>
     } <span class="hljs-keyword">else</span> {
       <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'Calculating result'</span>);
       <span class="hljs-keyword">let</span> result = value + <span class="hljs-number">20</span>;
       cache[value] = result;
       <span class="hljs-keyword">return</span> result;
     }
  };
};
<span class="hljs-comment">// returned function from memoizAddition</span>
<span class="hljs-keyword">const</span> addition = <span class="hljs-title function_">memoizAddition</span>();
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-title function_">addition</span>(<span class="hljs-number">20</span>)); <span class="hljs-comment">//output: 40 calculated</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-title function_">addition</span>(<span class="hljs-number">20</span>)); <span class="hljs-comment">//output: 40 cached</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
24

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#24-What-is-memoization

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
