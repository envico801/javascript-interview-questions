==================== Question ====================  

### What is throttling?  

==================== Answer ====================  

Throttling is a technique used to limit the execution of an event handler function, even when this event triggers continuously due to user actions. The common use cases are browser resizing, window scrolling etc.

The below example creates a throttle function to reduce the number of events for each pixel change and trigger scroll event for each 100ms except for the first event.

<!-- codeblock-start -->
<pre><code class="hljs language-js"><span class="hljs-keyword">const</span> <span class="hljs-title function_">throttle</span> = (<span class="hljs-params">func, limit</span>) => {
  <span class="hljs-keyword">let</span> inThrottle;
  <span class="hljs-keyword">return</span> <span class="hljs-function">(<span class="hljs-params">...args</span>) =></span> {
     <span class="hljs-keyword">if</span> (!inThrottle) {
       func.<span class="hljs-title function_">apply</span>(<span class="hljs-variable language_">this</span>, args);
       inThrottle = <span class="hljs-literal">true</span>;
       <span class="hljs-built_in">setTimeout</span>(<span class="hljs-function">() =></span> (inThrottle = <span class="hljs-literal">false</span>), limit);
     }
  };
};
<span class="hljs-variable language_">window</span>.<span class="hljs-title function_">addEventListener</span>(<span class="hljs-string">'scroll'</span>, <span class="hljs-function">() =></span> {
  <span class="hljs-title function_">throttle</span>(handleScrollAnimation, <span class="hljs-number">100</span>);
});
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
435

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#435-What-is-throttling

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
