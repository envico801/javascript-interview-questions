==================== Question ====================  

### What is an Unary operator  

==================== Answer ====================  

The unary(+) operator is used to convert a variable to a number.If the variable cannot be converted, it will still become a number but with the value NaN. Let's see this behavior in an action.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> x = <span class="hljs-string">'100'</span>;
<span class="hljs-keyword">var</span> y = +x;
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-keyword">typeof</span> x, <span class="hljs-keyword">typeof</span> y); <span class="hljs-comment">// string, number</span>
<span class="hljs-keyword">var</span> a = <span class="hljs-string">'Hello'</span>;
<span class="hljs-keyword">var</span> b = +a;
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-keyword">typeof</span> a, <span class="hljs-keyword">typeof</span> b, b); <span class="hljs-comment">// string, number, NaN</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
241

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#241-What-is-an-unary-operator

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
