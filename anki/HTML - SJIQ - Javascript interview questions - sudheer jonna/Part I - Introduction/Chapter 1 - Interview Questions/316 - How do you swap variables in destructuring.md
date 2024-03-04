==================== Question ====================  

### How do you swap variables in destructuring assignment  

==================== Answer ====================  

If you don't use destructuring assignment, swapping two values requires a temporary variable. Whereas using a destructuring feature, two variable values can be swapped in one destructuring expression. Let's swap two number variables in array destructuring assignment,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> x = <span class="hljs-number">10</span>,
  y = <span class="hljs-number">20</span>;
[x, y] = [y, x];
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(x); <span class="hljs-comment">// 20</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(y); <span class="hljs-comment">// 10</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
316

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#316-How-do-you-swap-variables-in-destructuring

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
