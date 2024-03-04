==================== Question ====================  

### What is the difference between function and class declarations  

==================== Answer ====================  

The main difference between function declarations and class declarations is `hoisting`. The function declarations are hoisted but not class declarations.

**Classes:**

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> user = <span class="hljs-keyword">new</span> <span class="hljs-title class_">User</span>(); <span class="hljs-comment">// ReferenceError</span>
<span class="hljs-keyword">class</span> <span class="hljs-title class_">User</span> {}
</code></pre>
<!-- codeblock-end -->

**Constructor Function:**

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> user = <span class="hljs-keyword">new</span> <span class="hljs-title class_">User</span>(); <span class="hljs-comment">// No error</span>
<span class="hljs-keyword">function</span> <span class="hljs-title function_">User</span>(<span class="hljs-params"></span>) {}
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
406

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#406-What-is-the-difference-between-function-an

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
