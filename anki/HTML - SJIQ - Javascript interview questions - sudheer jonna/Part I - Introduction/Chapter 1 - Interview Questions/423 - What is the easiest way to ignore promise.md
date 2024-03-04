==================== Question ====================  

### What is the easiest way to ignore promise errors?  

==================== Answer ====================  

The easiest and safest way to ignore promise errors is void that error. This approach is ESLint friendly too.

<!-- codeblock-start -->
<pre><code class="hljs language-js"><span class="hljs-keyword">await</span> promise.<span class="hljs-title function_">catch</span>(<span class="hljs-function">(<span class="hljs-params">e</span>) =></span> <span class="hljs-keyword">void</span> e);
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
423

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#423-What-is-the-easiest-way-to-ignore-promise

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
