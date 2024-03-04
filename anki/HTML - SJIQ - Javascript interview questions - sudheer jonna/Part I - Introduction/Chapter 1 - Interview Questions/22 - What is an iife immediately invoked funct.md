==================== Question ====================  

### What is an IIFE (Immediately Invoked Function Expression)  

==================== Answer ====================  

IIFE (Immediately Invoked Function Expression) is a JavaScript function that runs as soon as it is defined. The signature of it would be as below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript">(<span class="hljs-keyword">function</span> (<span class="hljs-params"></span>) {
  <span class="hljs-comment">// logic here</span>
})();
</code></pre>
<!-- codeblock-end -->

The primary reason to use an IIFE is to obtain data privacy because any variables declared within the IIFE cannot be accessed by the outside world. i.e, If you try to access variables from the IIFE then it throws an error as below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript">(<span class="hljs-keyword">function</span> (<span class="hljs-params"></span>) {
  <span class="hljs-keyword">var</span> message = <span class="hljs-string">'IIFE'</span>;
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(message);
})();
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(message); <span class="hljs-comment">//Error: message is not defined</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
22

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#22-What-is-an-iife-immediately-invoked-funct

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
