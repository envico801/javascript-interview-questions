==================== Question ====================  

### What is the advantage of a comma operator  

==================== Answer ====================  

It is normally used to include multiple expressions in a location that requires a single expression. One of the common usages of this comma operator is to supply multiple parameters in a `for` loop. For example, the below for loop uses multiple expressions in a single location using comma operator,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">for</span> (<span class="hljs-keyword">var</span> a = <span class="hljs-number">0</span>, b =<span class="hljs-number">10</span>; a &#x3C;= <span class="hljs-number">10</span>; a++, b--)
</code></pre>
<!-- codeblock-end -->

You can also use the comma operator in a return statement where it processes before returning.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">myFunction</span>(<span class="hljs-params"></span>) {
  <span class="hljs-keyword">var</span> a = <span class="hljs-number">1</span>;
  <span class="hljs-keyword">return</span> (a += <span class="hljs-number">10</span>), a; <span class="hljs-comment">// 11</span>
}
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
250

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#250-What-is-the-advantage-of-a-comma-operator

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
