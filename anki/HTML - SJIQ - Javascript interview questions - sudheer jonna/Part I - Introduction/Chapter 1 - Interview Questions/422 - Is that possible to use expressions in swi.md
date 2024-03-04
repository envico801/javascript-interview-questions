==================== Question ====================  

### Is that possible to use expressions in switch cases?  

==================== Answer ====================  

You might have seen expressions used in switch condition but it is also possible to use for switch cases by assigning true value for the switch condition. Let's see the weather condition based on temparature as an example,

<!-- codeblock-start -->
<pre><code class="hljs language-js"><span class="hljs-keyword">const</span> weather = (<span class="hljs-keyword">function</span> <span class="hljs-title function_">getWeather</span>(<span class="hljs-params">temp</span>) {
  <span class="hljs-keyword">switch</span> (<span class="hljs-literal">true</span>) {
     <span class="hljs-keyword">case</span> temp &#x3C; <span class="hljs-number">0</span>:
       <span class="hljs-keyword">return</span> <span class="hljs-string">'freezing'</span>;
     <span class="hljs-keyword">case</span> temp &#x3C; <span class="hljs-number">10</span>:
       <span class="hljs-keyword">return</span> <span class="hljs-string">'cold'</span>;
     <span class="hljs-keyword">case</span> temp &#x3C; <span class="hljs-number">24</span>:
       <span class="hljs-keyword">return</span> <span class="hljs-string">'cool'</span>;
     <span class="hljs-attr">default</span>:
       <span class="hljs-keyword">return</span> <span class="hljs-string">'unknown'</span>;
  }
})(<span class="hljs-number">10</span>);
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
422

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#422-Is-that-possible-to-use-expressions-in-swi

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
