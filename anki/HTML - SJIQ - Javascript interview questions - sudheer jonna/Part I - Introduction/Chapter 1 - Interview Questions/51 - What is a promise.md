==================== Question ====================  

### What is a promise  

==================== Answer ====================  

A promise is an object that may produce a single value some time in the future with either a resolved value or a reason that it’s not resolved(for example, network error). It will be in one of the 3 possible states: fulfilled, rejected, or pending.

The syntax of Promise creation looks like below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> promise = <span class="hljs-keyword">new</span> <span class="hljs-title class_">Promise</span>(<span class="hljs-keyword">function</span> (<span class="hljs-params">resolve, reject</span>) {
  <span class="hljs-comment">// promise description</span>
});
</code></pre>
<!-- codeblock-end -->

The usage of a promise would be as below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> promise = <span class="hljs-keyword">new</span> <span class="hljs-title class_">Promise</span>(
  <span class="hljs-function">(<span class="hljs-params">resolve</span>) =></span> {
     <span class="hljs-built_in">setTimeout</span>(<span class="hljs-function">() =></span> {
       <span class="hljs-title function_">resolve</span>(<span class="hljs-string">"I'm a Promise!"</span>);
     }, <span class="hljs-number">5000</span>);
  },
  <span class="hljs-function">(<span class="hljs-params">reject</span>) =></span> {},
);
promise.<span class="hljs-title function_">then</span>(<span class="hljs-function">(<span class="hljs-params">value</span>) =></span> <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(value));
</code></pre>
<!-- codeblock-end -->

The action flow of a promise will be as below,

![promises](../../../../images/promises.png)

==================== Id ====================  
51

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#51-What-is-a-promise

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
