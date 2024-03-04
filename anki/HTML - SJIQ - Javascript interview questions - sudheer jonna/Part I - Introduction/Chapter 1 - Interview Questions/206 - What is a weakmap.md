==================== Question ====================  

### What is a WeakMap  

==================== Answer ====================  

The WeakMap object is a collection of key/value pairs in which the keys are weakly referenced. In this case, keys must be objects and the values can be arbitrary values. The syntax is looking like as below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">new</span> <span class="hljs-title class_">WeakMap</span>([iterable]);
</code></pre>
<!-- codeblock-end -->

Let's see the below example to explain it's behavior,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> ws = <span class="hljs-keyword">new</span> <span class="hljs-title class_">WeakMap</span>();
<span class="hljs-keyword">var</span> user = {};
ws.<span class="hljs-title function_">set</span>(user);
ws.<span class="hljs-title function_">has</span>(user); <span class="hljs-comment">// true</span>
ws.<span class="hljs-title function_">delete</span>(user); <span class="hljs-comment">// removes user from the map</span>
ws.<span class="hljs-title function_">has</span>(user); <span class="hljs-comment">// false, user has been removed</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
206

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#206-What-is-a-weakmap

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
