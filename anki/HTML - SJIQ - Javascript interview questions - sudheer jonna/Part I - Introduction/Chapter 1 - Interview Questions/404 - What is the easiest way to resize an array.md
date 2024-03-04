==================== Question ====================  

### What is the easiest way to resize an array  

==================== Answer ====================  

The length property of an array is useful to resize or empty an array quickly. Let's apply length property on number array to resize the number of elements from 5 to 2,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> array = [<span class="hljs-number">1</span>, <span class="hljs-number">2</span>, <span class="hljs-number">3</span>, <span class="hljs-number">4</span>, <span class="hljs-number">5</span>];
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(array.<span class="hljs-property">length</span>); <span class="hljs-comment">// 5</span>
array.<span class="hljs-property">length</span> = <span class="hljs-number">2</span>;
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(array.<span class="hljs-property">length</span>); <span class="hljs-comment">// 2</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(array); <span class="hljs-comment">// [1,2]</span>
</code></pre>
<!-- codeblock-end -->

and the array can be emptied too

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> array = [<span class="hljs-number">1</span>, <span class="hljs-number">2</span>, <span class="hljs-number">3</span>, <span class="hljs-number">4</span>, <span class="hljs-number">5</span>];
array.<span class="hljs-property">length</span> = <span class="hljs-number">0</span>;
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(array.<span class="hljs-property">length</span>); <span class="hljs-comment">// 0</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(array); <span class="hljs-comment">// []</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
404

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#404-What-is-the-easiest-way-to-resize-an-array

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
