==================== Question ====================  

### How do you make synchronous HTTP request  

==================== Answer ====================  

Browsers provide an XMLHttpRequest object which can be used to make synchronous HTTP requests from JavaScript

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">httpGet</span>(<span class="hljs-params">theUrl</span>) {
  <span class="hljs-keyword">var</span> xmlHttpReq = <span class="hljs-keyword">new</span> <span class="hljs-title class_">XMLHttpRequest</span>();
  xmlHttpReq.<span class="hljs-title function_">open</span>(<span class="hljs-string">'GET'</span>, theUrl, <span class="hljs-literal">false</span>); <span class="hljs-comment">// false for synchronous request</span>
  xmlHttpReq.<span class="hljs-title function_">send</span>(<span class="hljs-literal">null</span>);
  <span class="hljs-keyword">return</span> xmlHttpReq.<span class="hljs-property">responseText</span>;
}
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
169

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#169-How-do-you-make-synchronous-http-request

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
