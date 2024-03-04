==================== Question ====================  

### What is promise.all  

==================== Answer ====================  

Promise.all is a promise that takes an array of promises as an input (an iterable), and it gets resolved when all the promises get resolved or any one of them gets rejected. For example, the syntax of promise.all method is below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-title class_">Promise</span>.<span class="hljs-title function_">all</span>([<span class="hljs-title class_">Promise1</span>, <span class="hljs-title class_">Promise2</span>, <span class="hljs-title class_">Promise3</span>]) .<span class="hljs-title function_">then</span>(result) => {   <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(result) }) .<span class="hljs-title function_">catch</span>(<span class="hljs-function"><span class="hljs-params">error</span> =></span> <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">`Error in promises <span class="hljs-subst">${error}</span>`</span>))
</code></pre>
<!-- codeblock-end -->

**Note:** Remember that the order of the promises(output the result) is maintained as per input order.

==================== Id ====================  
64

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#64-What-is-promise-all

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
