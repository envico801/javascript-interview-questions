==================== Question ====================  

### What is destructuring assignment  

==================== Answer ====================  

The destructuring assignment is a JavaScript expression that makes it possible to unpack values from arrays or properties from objects into distinct variables.

Let's get the month values from an array using destructuring assignment

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> [one, two, three] = [<span class="hljs-string">'JAN'</span>, <span class="hljs-string">'FEB'</span>, <span class="hljs-string">'MARCH'</span>];
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(one); <span class="hljs-comment">// "JAN"</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(two); <span class="hljs-comment">// "FEB"</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(three); <span class="hljs-comment">// "MARCH"</span>
</code></pre>
<!-- codeblock-end -->

and you can get user properties of an object using destructuring assignment,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> { name, age } = { <span class="hljs-attr">name</span>: <span class="hljs-string">'John'</span>, <span class="hljs-attr">age</span>: <span class="hljs-number">32</span> };
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(name); <span class="hljs-comment">// John</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(age); <span class="hljs-comment">// 32</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
314

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#314-What-is-destructuring-assignment

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
