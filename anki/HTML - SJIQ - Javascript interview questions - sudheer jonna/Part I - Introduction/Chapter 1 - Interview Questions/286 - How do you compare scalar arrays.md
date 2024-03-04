==================== Question ====================  

### How do you compare scalar arrays  

==================== Answer ====================  

You can use length and every method of arrays to compare two scalar(compared directly using ===) arrays. The combination of these expressions can give the expected result,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> arrayFirst = [<span class="hljs-number">1</span>, <span class="hljs-number">2</span>, <span class="hljs-number">3</span>, <span class="hljs-number">4</span>, <span class="hljs-number">5</span>];
<span class="hljs-keyword">const</span> arraySecond = [<span class="hljs-number">1</span>, <span class="hljs-number">2</span>, <span class="hljs-number">3</span>, <span class="hljs-number">4</span>, <span class="hljs-number">5</span>];
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(arrayFirst.<span class="hljs-property">length</span> === arraySecond.<span class="hljs-property">length</span> &#x26;&#x26; arrayFirst.<span class="hljs-title function_">every</span>(<span class="hljs-function">(<span class="hljs-params">value, index</span>) =></span> value === arraySecond[index])); <span class="hljs-comment">// true</span>
</code></pre>
<!-- codeblock-end -->

If you would like to compare arrays irrespective of order then you should sort them before,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> arrayFirst = [<span class="hljs-number">2</span>, <span class="hljs-number">3</span>, <span class="hljs-number">1</span>, <span class="hljs-number">4</span>, <span class="hljs-number">5</span>];
<span class="hljs-keyword">const</span> arraySecond = [<span class="hljs-number">1</span>, <span class="hljs-number">2</span>, <span class="hljs-number">3</span>, <span class="hljs-number">4</span>, <span class="hljs-number">5</span>];
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(arrayFirst.<span class="hljs-property">length</span> === arraySecond.<span class="hljs-property">length</span> &#x26;&#x26; arrayFirst.<span class="hljs-title function_">sort</span>().<span class="hljs-title function_">every</span>(<span class="hljs-function">(<span class="hljs-params">value, index</span>) =></span> value === arraySecond[index])); <span class="hljs-comment">//true</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
286

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#286-How-do-you-compare-scalar-arrays

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
