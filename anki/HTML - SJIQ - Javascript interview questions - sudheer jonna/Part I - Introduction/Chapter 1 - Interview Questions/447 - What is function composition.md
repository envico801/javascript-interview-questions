==================== Question ====================  

### What is Function Composition?  

==================== Answer ====================  

It is an approach where the result of one function is passed on to the next function, which is passed to another until the final function is executed for the final result.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-comment">//example</span>
<span class="hljs-keyword">const</span> <span class="hljs-title function_">double</span> = (<span class="hljs-params">x</span>) => x * <span class="hljs-number">2</span>;
<span class="hljs-keyword">const</span> <span class="hljs-title function_">square</span> = (<span class="hljs-params">x</span>) => x * x;
<span class="hljs-keyword">var</span> output1 = <span class="hljs-title function_">double</span>(<span class="hljs-number">2</span>);
<span class="hljs-keyword">var</span> output2 = <span class="hljs-title function_">square</span>(output1);
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(output2);
<span class="hljs-keyword">var</span> output_final = <span class="hljs-title function_">square</span>(<span class="hljs-title function_">double</span>(<span class="hljs-number">2</span>));
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(output_final);
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
447

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#447-What-is-function-composition

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
