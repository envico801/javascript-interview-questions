==================== Question ====================  

### What is the difference between uneval and eval  

==================== Answer ====================  

The `uneval` function returns the source of a given object; whereas the `eval` function does the opposite, by evaluating that source code in a different memory area. Let's see an example to clarify the difference,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> msg = <span class="hljs-title function_">uneval</span>(<span class="hljs-keyword">function</span> <span class="hljs-title function_">greeting</span>(<span class="hljs-params"></span>) {
  <span class="hljs-keyword">return</span> <span class="hljs-string">'Hello, Good morning'</span>;
});
<span class="hljs-keyword">var</span> greeting = <span class="hljs-built_in">eval</span>(msg);
<span class="hljs-title function_">greeting</span>(); <span class="hljs-comment">// returns "Hello, Good morning"</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
213

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#213-What-is-the-difference-between-uneval-and

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
