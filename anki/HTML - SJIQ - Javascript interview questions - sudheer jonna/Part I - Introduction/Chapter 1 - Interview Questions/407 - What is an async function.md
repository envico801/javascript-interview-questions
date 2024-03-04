==================== Question ====================  

### What is an async function  

==================== Answer ====================  

An async function is a function declared with the `async` keyword which enables asynchronous, promise-based behavior to be written in a cleaner style by avoiding promise chains. These functions can contain zero or more `await` expressions.

Let's take a below async function example,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">async</span> <span class="hljs-keyword">function</span> <span class="hljs-title function_">logger</span>(<span class="hljs-params"></span>) {
  <span class="hljs-keyword">let</span> data = <span class="hljs-keyword">await</span> <span class="hljs-title function_">fetch</span>(<span class="hljs-string">'http://someapi.com/users'</span>); <span class="hljs-comment">// pause until fetch returns</span>
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(data);
}
<span class="hljs-title function_">logger</span>();
</code></pre>
<!-- codeblock-end -->

It is basically syntax sugar over ES2015 promises and generators.

==================== Id ====================  
407

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#407-What-is-an-async-function

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
