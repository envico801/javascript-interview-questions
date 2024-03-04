==================== Question ====================  

### How do you make asynchronous HTTP request  

==================== Answer ====================  

Browsers provide an XMLHttpRequest object which can be used to make asynchronous HTTP requests from JavaScript by passing the 3rd parameter as true.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">httpGetAsync</span>(<span class="hljs-params">theUrl, callback</span>) {
  <span class="hljs-keyword">var</span> xmlHttpReq = <span class="hljs-keyword">new</span> <span class="hljs-title class_">XMLHttpRequest</span>();
  xmlHttpReq.<span class="hljs-property">onreadystatechange</span> = <span class="hljs-keyword">function</span> (<span class="hljs-params"></span>) {
     <span class="hljs-keyword">if</span> (xmlHttpReq.<span class="hljs-property">readyState</span> == <span class="hljs-number">4</span> &#x26;&#x26; xmlHttpReq.<span class="hljs-property">status</span> == <span class="hljs-number">200</span>) <span class="hljs-title function_">callback</span>(xmlHttpReq.<span class="hljs-property">responseText</span>);
  };
  xmlHttp.<span class="hljs-title function_">open</span>(<span class="hljs-string">'GET'</span>, theUrl, <span class="hljs-literal">true</span>); <span class="hljs-comment">// true for asynchronous</span>
  xmlHttp.<span class="hljs-title function_">send</span>(<span class="hljs-literal">null</span>);
}
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
170

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#170-How-do-you-make-asynchronous-http-request

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
