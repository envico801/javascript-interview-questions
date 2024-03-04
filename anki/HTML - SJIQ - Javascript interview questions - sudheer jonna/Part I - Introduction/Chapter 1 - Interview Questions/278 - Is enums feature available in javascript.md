==================== Question ====================  

### Is enums feature available in javascript  

==================== Answer ====================  

No, javascript does not natively support enums. But there are different kinds of solutions to simulate them even though they may not provide exact equivalents. For example, you can use freeze or seal on object,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> <span class="hljs-title class_">DaysEnum</span> = <span class="hljs-title class_">Object</span>.<span class="hljs-title function_">freeze</span>({<span class="hljs-string">"monday"</span>:<span class="hljs-number">1</span>, <span class="hljs-string">"tuesday"</span>:<span class="hljs-number">2</span>, <span class="hljs-string">"wednesday"</span>:<span class="hljs-number">3</span>, ...})
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
278

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#278-Is-enums-feature-available-in-javascript

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
