==================== Question ====================  

### What is a callback hell  

==================== Answer ====================  

Callback Hell is an anti-pattern with multiple nested callbacks which makes code hard to read and debug when dealing with asynchronous logic. The callback hell looks like below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-title function_">async1</span>(<span class="hljs-keyword">function</span>(<span class="hljs-params"></span>){
     <span class="hljs-title function_">async2</span>(<span class="hljs-keyword">function</span>(<span class="hljs-params"></span>){
         <span class="hljs-title function_">async3</span>(<span class="hljs-keyword">function</span>(<span class="hljs-params"></span>){
             <span class="hljs-title function_">async4</span>(<span class="hljs-keyword">function</span>(<span class="hljs-params"></span>){
                 ....
             });
         });
     });
});
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
56

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#56-What-is-a-callback-hell

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
