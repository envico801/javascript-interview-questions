==================== Question ====================  

### What are the string methods available in Regular expression  

==================== Answer ====================  

Regular Expressions has two string methods: search() and replace().

The search() method uses an expression to search for a match, and returns the position of the match.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> msg = <span class="hljs-string">'Hello John'</span>;
<span class="hljs-keyword">var</span> n = msg.<span class="hljs-title function_">search</span>(<span class="hljs-regexp">/John/i</span>); <span class="hljs-comment">// 6</span>
</code></pre>
<!-- codeblock-end -->

The replace() method is used to return a modified string where the pattern is replaced.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> msg = <span class="hljs-string">'Hello John'</span>;
<span class="hljs-keyword">var</span> n = msg.<span class="hljs-title function_">replace</span>(<span class="hljs-regexp">/John/i</span>, <span class="hljs-string">'Buttler'</span>); <span class="hljs-comment">// Hello Buttler</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
155

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#155-What-are-the-string-methods-available-in-r

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
