==================== Question ====================  

### What is the difference between dense and sparse arrays?  

==================== Answer ====================  

An array contains items at each index starting from first(0) to last(array.length - 1) is called as Dense array. Whereas if at least one item is missing at any index, the array is called as sparse.

Let's see the below two kind of arrays,

<!-- codeblock-start -->
<pre><code class="hljs language-js"><span class="hljs-keyword">const</span> avengers = [<span class="hljs-string">'Ironman'</span>, <span class="hljs-string">'Hulk'</span>, <span class="hljs-string">'CaptainAmerica'</span>];
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(avengers[<span class="hljs-number">0</span>]); <span class="hljs-comment">// 'Ironman'</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(avengers[<span class="hljs-number">1</span>]); <span class="hljs-comment">// 'Hulk'</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(avengers[<span class="hljs-number">2</span>]); <span class="hljs-comment">// 'CaptainAmerica'</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(avengers.<span class="hljs-property">length</span>); <span class="hljs-comment">// 3</span>
<span class="hljs-keyword">const</span> justiceLeague = [<span class="hljs-string">'Superman'</span>, <span class="hljs-string">'Aquaman'</span>, , <span class="hljs-string">'Batman'</span>];
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(justiceLeague[<span class="hljs-number">0</span>]); <span class="hljs-comment">// 'Superman'</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(justiceLeague[<span class="hljs-number">1</span>]); <span class="hljs-comment">// 'Aquaman'</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(justiceLeague[<span class="hljs-number">2</span>]); <span class="hljs-comment">// undefined</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(justiceLeague[<span class="hljs-number">3</span>]); <span class="hljs-comment">// 'Batman'</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(justiceLeague.<span class="hljs-property">length</span>); <span class="hljs-comment">// 4</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
427

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#427-What-is-the-difference-between-dense-and-s

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
