==================== Question ====================  

### How do you detect a mobile browser without regexp  

==================== Answer ====================  

You can detect mobile browsers by simply running through a list of devices and checking if the useragent matches anything. This is an alternative solution for RegExp usage,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">detectmob</span>(<span class="hljs-params"></span>) {
  <span class="hljs-keyword">if</span> (
     navigator.<span class="hljs-property">userAgent</span>.<span class="hljs-title function_">match</span>(<span class="hljs-regexp">/Android/i</span>) ||
     navigator.<span class="hljs-property">userAgent</span>.<span class="hljs-title function_">match</span>(<span class="hljs-regexp">/webOS/i</span>) ||
     navigator.<span class="hljs-property">userAgent</span>.<span class="hljs-title function_">match</span>(<span class="hljs-regexp">/iPhone/i</span>) ||
     navigator.<span class="hljs-property">userAgent</span>.<span class="hljs-title function_">match</span>(<span class="hljs-regexp">/iPad/i</span>) ||
     navigator.<span class="hljs-property">userAgent</span>.<span class="hljs-title function_">match</span>(<span class="hljs-regexp">/iPod/i</span>) ||
     navigator.<span class="hljs-property">userAgent</span>.<span class="hljs-title function_">match</span>(<span class="hljs-regexp">/BlackBerry/i</span>) ||
     navigator.<span class="hljs-property">userAgent</span>.<span class="hljs-title function_">match</span>(<span class="hljs-regexp">/Windows Phone/i</span>)
  ) {
     <span class="hljs-keyword">return</span> <span class="hljs-literal">true</span>;
  } <span class="hljs-keyword">else</span> {
     <span class="hljs-keyword">return</span> <span class="hljs-literal">false</span>;
  }
}
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
167

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#167-How-do-you-detect-a-mobile-browser-without

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
