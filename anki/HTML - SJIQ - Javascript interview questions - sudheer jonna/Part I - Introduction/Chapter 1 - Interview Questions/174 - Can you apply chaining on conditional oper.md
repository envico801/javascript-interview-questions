==================== Question ====================  

### Can you apply chaining on conditional operator  

==================== Answer ====================  

Yes, you can apply chaining on conditional operators similar to if … else if … else if … else chain. The syntax is going to be as below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">traceValue</span>(<span class="hljs-params">someParam</span>) {
  <span class="hljs-keyword">return</span> (
     condition1 ? value1
     : condition2 ? value2
     : condition3 ? value3
     : value4
  );
}
<span class="hljs-comment">// The above conditional operator is equivalent to:</span>
<span class="hljs-keyword">function</span> <span class="hljs-title function_">traceValue</span>(<span class="hljs-params">someParam</span>) {
  <span class="hljs-keyword">if</span> (condition1) {
     <span class="hljs-keyword">return</span> value1;
  } <span class="hljs-keyword">else</span> <span class="hljs-keyword">if</span> (condition2) {
     <span class="hljs-keyword">return</span> value2;
  } <span class="hljs-keyword">else</span> <span class="hljs-keyword">if</span> (condition3) {
     <span class="hljs-keyword">return</span> value3;
  } <span class="hljs-keyword">else</span> {
     <span class="hljs-keyword">return</span> value4;
  }
}
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
174

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#174-Can-you-apply-chaining-on-conditional-oper

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
