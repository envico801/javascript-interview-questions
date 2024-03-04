==================== Question ====================  

### What is the output of below code?

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> promiseOne = <span class="hljs-keyword">new</span> <span class="hljs-title class_">Promise</span>(<span class="hljs-function">(<span class="hljs-params">resolve, reject</span>) =></span> <span class="hljs-built_in">setTimeout</span>(resolve, <span class="hljs-number">4000</span>));
<span class="hljs-keyword">const</span> promiseTwo = <span class="hljs-keyword">new</span> <span class="hljs-title class_">Promise</span>(<span class="hljs-function">(<span class="hljs-params">resolve, reject</span>) =></span> <span class="hljs-built_in">setTimeout</span>(reject, <span class="hljs-number">4000</span>));
<span class="hljs-title class_">Promise</span>.<span class="hljs-title function_">all</span>([promiseOne, promiseTwo]).<span class="hljs-title function_">then</span>(<span class="hljs-function">(<span class="hljs-params">data</span>) =></span> <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(data));
</code></pre>
<!-- codeblock-end -->

- 1: [{status: "fullfilled", value: undefined}, {status: "rejected", reason: undefined}]

- 2: [{status: "fullfilled", value: undefined}, Uncaught(in promise)]

- 3: Uncaught (in promise)

- 4: [Uncaught(in promise), Uncaught(in promise)]  

==================== Answer ====================  

Answer: 3

The above promises settled at the same time but one of them resolved and other one rejected. When you use `.all` method on these promises, the result will be short circuted by throwing an error due to rejection in second promise. But If you use `.allSettled` method then result of both the promises will be returned irrespective of resolved or rejected promise status without throwing any error.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-title class_">Promise</span>.<span class="hljs-title function_">allSettled</span>([promiseOne, promiseTwo]).<span class="hljs-title function_">then</span>(<span class="hljs-function">(<span class="hljs-params">data</span>) =></span> <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(data));
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
526

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#526-What-is-the-output-of-below-code-javas

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
