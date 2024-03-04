==================== Question ====================  

### What are raw strings  

==================== Answer ====================  

ES6 provides a raw strings feature using the `String.raw()` method which is used to get the raw string form of template strings. This feature allows you to access the raw strings as they were entered, without processing escape sequences. For example, the usage would be as below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> calculationString = <span class="hljs-title class_">String</span>.<span class="hljs-property">raw</span><span class="hljs-string">`The sum of numbers is \n<span class="hljs-subst">${<span class="hljs-number">1</span> + <span class="hljs-number">2</span> + <span class="hljs-number">3</span> + <span class="hljs-number">4</span>}</span>!`</span>;
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(calculationString); <span class="hljs-comment">// The sum of numbers is \n10!</span>
</code></pre>
<!-- codeblock-end -->

If you don't use raw strings, the newline character sequence will be processed by displaying the output in multiple lines

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> calculationString = <span class="hljs-string">`The sum of numbers is \n<span class="hljs-subst">${<span class="hljs-number">1</span> + <span class="hljs-number">2</span> + <span class="hljs-number">3</span> + <span class="hljs-number">4</span>}</span>!`</span>;
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(calculationString);
<span class="hljs-comment">// The sum of numbers is</span>
<span class="hljs-comment">// 10!</span>
</code></pre>
<!-- codeblock-end -->

Also, the raw property is available on the first argument to the tag function

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">tag</span>(<span class="hljs-params">strings</span>) {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(strings.<span class="hljs-property">raw</span>[<span class="hljs-number">0</span>]);
}
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
313

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#313-What-are-raw-strings

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
