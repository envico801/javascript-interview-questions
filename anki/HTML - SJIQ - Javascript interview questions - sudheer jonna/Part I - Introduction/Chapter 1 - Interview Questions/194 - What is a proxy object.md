==================== Question ====================  

### What is a proxy object  

==================== Answer ====================  

The Proxy object is used to define custom behavior for fundamental operations such as property lookup, assignment, enumeration, function invocation, etc. The syntax would be as follows,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> p = <span class="hljs-keyword">new</span> <span class="hljs-title class_">Proxy</span>(target, handler);
</code></pre>
<!-- codeblock-end -->

Let's take an example of proxy object,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> handler = {
  <span class="hljs-attr">get</span>: <span class="hljs-keyword">function</span> (<span class="hljs-params">obj, prop</span>) {
     <span class="hljs-keyword">return</span> prop <span class="hljs-keyword">in</span> obj ? obj[prop] : <span class="hljs-number">100</span>;
  },
};
<span class="hljs-keyword">var</span> p = <span class="hljs-keyword">new</span> <span class="hljs-title class_">Proxy</span>({}, handler);
p.<span class="hljs-property">a</span> = <span class="hljs-number">10</span>;
p.<span class="hljs-property">b</span> = <span class="hljs-literal">null</span>;
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(p.<span class="hljs-property">a</span>, p.<span class="hljs-property">b</span>); <span class="hljs-comment">// 10, null</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'c'</span> <span class="hljs-keyword">in</span> p, p.<span class="hljs-property">c</span>); <span class="hljs-comment">// false, 100</span>
</code></pre>
<!-- codeblock-end -->

In the above code, it uses `get` handler which define the behavior of the proxy when an operation is performed on it

==================== Id ====================  
194

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#194-What-is-a-proxy-object

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
