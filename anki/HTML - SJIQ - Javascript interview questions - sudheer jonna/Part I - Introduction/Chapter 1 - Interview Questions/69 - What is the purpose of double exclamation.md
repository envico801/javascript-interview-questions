==================== Question ====================  

### What is the purpose of double exclamation  

==================== Answer ====================  

The double exclamation or negation(!!) ensures the resulting type is a boolean. If it was falsey (e.g. 0, null, undefined, etc.), it will be false, otherwise, it will be true.

For example, you can test IE version using this expression as below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">let</span> isIE8 = <span class="hljs-literal">false</span>;
isIE8 = !!navigator.<span class="hljs-property">userAgent</span>.<span class="hljs-title function_">match</span>(<span class="hljs-regexp">/MSIE 8.0/</span>);
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(isIE8); <span class="hljs-comment">// returns true or false</span>
</code></pre>
<!-- codeblock-end -->

If you don't use this expression then it returns the original value.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(navigator.<span class="hljs-property">userAgent</span>.<span class="hljs-title function_">match</span>(<span class="hljs-regexp">/MSIE 8.0/</span>)); <span class="hljs-comment">// returns either an Array or null</span>
</code></pre>
<!-- codeblock-end -->

**Note:** The expression !! is not an operator, but it is just twice of ! operator.

==================== Id ====================  
69

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#69-What-is-the-purpose-of-double-exclamation

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
