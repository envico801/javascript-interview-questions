==================== Question ====================  

### What are default values in destructuring assignment  

==================== Answer ====================  

A variable can be assigned a default value when the value unpacked from the array or object is undefined during destructuring assignment. It helps to avoid setting default values separately for each assignment. Let's take an example for both arrays and object use cases,

**Arrays destructuring:**

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> x, y, z;
[x = <span class="hljs-number">2</span>, y = <span class="hljs-number">4</span>, z = <span class="hljs-number">6</span>] = [<span class="hljs-number">10</span>];
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(x); <span class="hljs-comment">// 10</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(y); <span class="hljs-comment">// 4</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(z); <span class="hljs-comment">// 6</span>
</code></pre>
<!-- codeblock-end -->

**Objects destructuring:**

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> { x = <span class="hljs-number">2</span>, y = <span class="hljs-number">4</span>, z = <span class="hljs-number">6</span> } = { <span class="hljs-attr">x</span>: <span class="hljs-number">10</span> };
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(x); <span class="hljs-comment">// 10</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(y); <span class="hljs-comment">// 4</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(z); <span class="hljs-comment">// 6</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
315

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#315-What-are-default-values-in-destructuring-a

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
