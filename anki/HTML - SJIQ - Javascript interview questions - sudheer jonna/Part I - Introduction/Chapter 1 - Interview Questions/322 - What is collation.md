==================== Question ====================  

### What is collation  

==================== Answer ====================  

Collation is used for sorting a set of strings and searching within a set of strings. It is parameterized by locale and aware of Unicode. Let's take comparison and sorting features,

1. **Comparison:**

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> list = [<span class="hljs-string">'ä'</span>, <span class="hljs-string">'a'</span>, <span class="hljs-string">'z'</span>]; <span class="hljs-comment">// In German,  "ä" sorts with "a" Whereas in Swedish, "ä" sorts after "z"</span>
<span class="hljs-keyword">var</span> l10nDE = <span class="hljs-keyword">new</span> <span class="hljs-title class_">Intl</span>.<span class="hljs-title class_">Collator</span>(<span class="hljs-string">'de'</span>);
<span class="hljs-keyword">var</span> l10nSV = <span class="hljs-keyword">new</span> <span class="hljs-title class_">Intl</span>.<span class="hljs-title class_">Collator</span>(<span class="hljs-string">'sv'</span>);
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(l10nDE.<span class="hljs-title function_">compare</span>(<span class="hljs-string">'ä'</span>, <span class="hljs-string">'z'</span>) === -<span class="hljs-number">1</span>); <span class="hljs-comment">// true</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(l10nSV.<span class="hljs-title function_">compare</span>(<span class="hljs-string">'ä'</span>, <span class="hljs-string">'z'</span>) === +<span class="hljs-number">1</span>); <span class="hljs-comment">// true</span>
</code></pre>
<!-- codeblock-end -->

1. **Sorting:**

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> list = [<span class="hljs-string">'ä'</span>, <span class="hljs-string">'a'</span>, <span class="hljs-string">'z'</span>]; <span class="hljs-comment">// In German,  "ä" sorts with "a" Whereas in Swedish, "ä" sorts after "z"</span>
<span class="hljs-keyword">var</span> l10nDE = <span class="hljs-keyword">new</span> <span class="hljs-title class_">Intl</span>.<span class="hljs-title class_">Collator</span>(<span class="hljs-string">'de'</span>);
<span class="hljs-keyword">var</span> l10nSV = <span class="hljs-keyword">new</span> <span class="hljs-title class_">Intl</span>.<span class="hljs-title class_">Collator</span>(<span class="hljs-string">'sv'</span>);
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(list.<span class="hljs-title function_">sort</span>(l10nDE.<span class="hljs-property">compare</span>)); <span class="hljs-comment">// [ "a", "ä", "z" ]</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(list.<span class="hljs-title function_">sort</span>(l10nSV.<span class="hljs-property">compare</span>)); <span class="hljs-comment">// [ "a", "z", "ä" ]</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
322

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#322-What-is-collation

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
