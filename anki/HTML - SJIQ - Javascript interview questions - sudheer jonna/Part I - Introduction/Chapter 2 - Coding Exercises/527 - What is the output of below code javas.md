==================== Question ====================  

### What is the output of below code?

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">try</span> {
  <span class="hljs-built_in">setTimeout</span>(<span class="hljs-function">() =></span> {
     <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'try block'</span>);
     <span class="hljs-keyword">throw</span> <span class="hljs-keyword">new</span> <span class="hljs-title class_">Error</span>(<span class="hljs-string">`An exception is thrown`</span>);
  }, <span class="hljs-number">1000</span>);
} <span class="hljs-keyword">catch</span> (err) {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'Error: '</span>, err);
}
</code></pre>
<!-- codeblock-end -->

- 1: try block, Error: An exception is thrown

- 2: Error: An exception is thrown

- 3: try block, Uncaught Error: Exception is thrown

- 4: Uncaught Error: Exception is thrown  

==================== Answer ====================  

Answer: 3

If you put `setTimeout` and `setInterval` methods inside the try clause and an exception is thrown, the catch clause will not catch any of them. This is because the try...catch statement works synchronously, and the function in the above code is executed asynchronously after a certain period of time. Hence, you will see runtime exception without catching the error. To resolve this issue, you have to put the try...catch block inside the function as below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-built_in">setTimeout</span>(<span class="hljs-function">() =></span> {
  <span class="hljs-keyword">try</span> {
     <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'try block'</span>);
     <span class="hljs-keyword">throw</span> <span class="hljs-keyword">new</span> <span class="hljs-title class_">Error</span>(<span class="hljs-string">`An exception is thrown`</span>);
  } <span class="hljs-keyword">catch</span> (err) {
     <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'Error: '</span>, err);
  }
}, <span class="hljs-number">1000</span>);
</code></pre>
<!-- codeblock-end -->

You can use `.catch()` function in promises to avoid these issues with asynchronous code.

==================== Id ====================  
527

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#527-What-is-the-output-of-below-code-javas

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
