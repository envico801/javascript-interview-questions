==================== Question ====================  

### What is an observable  

==================== Answer ====================  

An Observable is basically a function that can return a stream of values either synchronously or asynchronously to an observer over time. The consumer can get the value by calling `subscribe()` method.

Let's look at a simple example of an Observable

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">import</span> { <span class="hljs-title class_">Observable</span> } <span class="hljs-keyword">from</span> <span class="hljs-string">'rxjs'</span>;
<span class="hljs-keyword">const</span> observable = <span class="hljs-keyword">new</span> <span class="hljs-title class_">Observable</span>(<span class="hljs-function">(<span class="hljs-params">observer</span>) =></span> {
  <span class="hljs-built_in">setTimeout</span>(<span class="hljs-function">() =></span> {
     observer.<span class="hljs-title function_">next</span>(<span class="hljs-string">'Message from a Observable!'</span>);
  }, <span class="hljs-number">3000</span>);
});
observable.<span class="hljs-title function_">subscribe</span>(<span class="hljs-function">(<span class="hljs-params">value</span>) =></span> <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(value));
</code></pre>
<!-- codeblock-end -->

![observables](../../../../images/observables.png)

**Note:** Observables are not part of the JavaScript language yet but they are being proposed to be added to the language

==================== Id ====================  
405

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#405-What-is-an-observable

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
