==================== Question ====================  

### How do you test for an empty object  

==================== Answer ====================  

There are different solutions based on ECMAScript versions

1. **Using Object entries(ECMA 7+):** You can use object entries length along with constructor type.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-title class_">Object</span>.<span class="hljs-title function_">entries</span>(obj).<span class="hljs-property">length</span> === <span class="hljs-number">0</span> &#x26;&#x26; obj.<span class="hljs-property">constructor</span> === <span class="hljs-title class_">Object</span>; <span class="hljs-comment">// Since date object length is 0, you need to check constructor check as well</span>
</code></pre>
<!-- codeblock-end -->

1. **Using Object keys(ECMA 5+):** You can use object keys length along with constructor type.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-title class_">Object</span>.<span class="hljs-title function_">keys</span>(obj).<span class="hljs-property">length</span> === <span class="hljs-number">0</span> &#x26;&#x26; obj.<span class="hljs-property">constructor</span> === <span class="hljs-title class_">Object</span>; <span class="hljs-comment">// Since date object length is 0, you need to check constructor check as well</span>
</code></pre>
<!-- codeblock-end -->

1. **Using for-in with hasOwnProperty(Pre-ECMA 5):** You can use a for-in loop along with hasOwnProperty.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">isEmpty</span>(<span class="hljs-params">obj</span>) {
  <span class="hljs-keyword">for</span> (<span class="hljs-keyword">var</span> prop <span class="hljs-keyword">in</span> obj) {
     <span class="hljs-keyword">if</span> (obj.<span class="hljs-title function_">hasOwnProperty</span>(prop)) {
       <span class="hljs-keyword">return</span> <span class="hljs-literal">false</span>;
     }
  }
  <span class="hljs-keyword">return</span> <span class="hljs-title class_">JSON</span>.<span class="hljs-title function_">stringify</span>(obj) === <span class="hljs-title class_">JSON</span>.<span class="hljs-title function_">stringify</span>({});
}
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
127

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#127-How-do-you-test-for-an-empty-object

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
