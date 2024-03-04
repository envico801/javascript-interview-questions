==================== Question ====================  

### How to get the value from get parameters  

==================== Answer ====================  

The `new URL()` object accepts the url string and `searchParams` property of this object can be used to access the get parameters. Remember that you may need to use polyfill or `window.location` to access the URL in older browsers(including IE).

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">let</span> urlString = <span class="hljs-string">'http://www.some-domain.com/about.html?x=1&#x26;y=2&#x26;z=3'</span>; <span class="hljs-comment">//window.location.href</span>
<span class="hljs-keyword">let</span> url = <span class="hljs-keyword">new</span> <span class="hljs-title function_">URL</span>(urlString);
<span class="hljs-keyword">let</span> parameterZ = url.<span class="hljs-property">searchParams</span>.<span class="hljs-title function_">get</span>(<span class="hljs-string">'z'</span>);
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(parameterZ); <span class="hljs-comment">// 3</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
287

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#287-How-to-get-the-value-from-get-parameters

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
