==================== Question ====================  

### What is a thunk function  

==================== Answer ====================  

A thunk is just a function which delays the evaluation of the value. It doesn’t take any arguments but gives the value whenever you invoke the thunk. i.e, It is used not to execute now but it will be sometime in the future. Let's take a synchronous example,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> <span class="hljs-title function_">add</span> = (<span class="hljs-params">x, y</span>) => x + y;
<span class="hljs-keyword">const</span> <span class="hljs-title function_">thunk</span> = (<span class="hljs-params"></span>) => <span class="hljs-title function_">add</span>(<span class="hljs-number">2</span>, <span class="hljs-number">3</span>);
<span class="hljs-title function_">thunk</span>(); <span class="hljs-comment">// 5</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
351

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#351-What-is-a-thunk-function

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
