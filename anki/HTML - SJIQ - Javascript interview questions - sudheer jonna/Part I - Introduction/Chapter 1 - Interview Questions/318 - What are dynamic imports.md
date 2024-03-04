==================== Question ====================  

### What are dynamic imports  

==================== Answer ====================  

The dynamic imports using `import()` function syntax allows us to load modules on demand by using promises or the async/await syntax. Currently this feature is in [stage4 proposal](https://github.com/tc39/proposal-dynamic-import). The main advantage of dynamic imports is reduction of our bundle's sizes, the size/payload response of our requests and overall improvements in the user experience.

The syntax of dynamic imports would be as below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">import</span>(<span class="hljs-string">'./Module'</span>).<span class="hljs-title function_">then</span>(<span class="hljs-function">(<span class="hljs-params">Module</span>) =></span> <span class="hljs-title class_">Module</span>.<span class="hljs-title function_">method</span>());
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
318

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#318-What-are-dynamic-imports

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
