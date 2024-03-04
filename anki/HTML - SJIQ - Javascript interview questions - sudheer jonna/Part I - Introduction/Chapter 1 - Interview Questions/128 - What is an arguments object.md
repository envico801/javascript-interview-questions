==================== Question ====================  

### What is an arguments object  

==================== Answer ====================  

The arguments object is an Array-like object accessible inside functions that contains the values of the arguments passed to that function. For example, let's see how to use arguments object inside sum function,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">sum</span>(<span class="hljs-params"></span>) {
  <span class="hljs-keyword">var</span> total = <span class="hljs-number">0</span>;
  <span class="hljs-keyword">for</span> (<span class="hljs-keyword">var</span> i = <span class="hljs-number">0</span>, len = <span class="hljs-variable language_">arguments</span>.<span class="hljs-property">length</span>; i &#x3C; len; ++i) {
     total += <span class="hljs-variable language_">arguments</span>[i];
  }
  <span class="hljs-keyword">return</span> total;
}
<span class="hljs-title function_">sum</span>(<span class="hljs-number">1</span>, <span class="hljs-number">2</span>, <span class="hljs-number">3</span>); <span class="hljs-comment">// returns 6</span>
</code></pre>
<!-- codeblock-end -->

**Note:** You can't apply array methods on arguments object. But you can convert into a regular array as below.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> argsArray = <span class="hljs-title class_">Array</span>.<span class="hljs-property"><span class="hljs-keyword">prototype</span></span>.<span class="hljs-property">slice</span>.<span class="hljs-title function_">call</span>(<span class="hljs-variable language_">arguments</span>);
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
128

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#128-What-is-an-arguments-object

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
