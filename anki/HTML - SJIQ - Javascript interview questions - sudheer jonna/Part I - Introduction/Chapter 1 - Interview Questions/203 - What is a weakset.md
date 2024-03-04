==================== Question ====================  

### What is a WeakSet  

==================== Answer ====================  

WeakSet is used to store a collection of weakly(weak references) held objects. The syntax would be as follows,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">new</span> <span class="hljs-title class_">WeakSet</span>([iterable]);
</code></pre>
<!-- codeblock-end -->

Let's see the below example to explain it's behavior,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> ws = <span class="hljs-keyword">new</span> <span class="hljs-title class_">WeakSet</span>();
<span class="hljs-keyword">var</span> user = {};
ws.<span class="hljs-title function_">add</span>(user);
ws.<span class="hljs-title function_">has</span>(user); <span class="hljs-comment">// true</span>
ws.<span class="hljs-title function_">delete</span>(user); <span class="hljs-comment">// removes user from the set</span>
ws.<span class="hljs-title function_">has</span>(user); <span class="hljs-comment">// false, user has been removed</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
203

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#203-What-is-a-weakset

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
