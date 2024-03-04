==================== Question ====================  

### What is the output of below code?

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">let</span> quickPromise = <span class="hljs-title class_">Promise</span>.<span class="hljs-title function_">resolve</span>();
quickPromise.<span class="hljs-title function_">then</span>(<span class="hljs-function">() =></span> <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'promise finished'</span>));
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'program finished'</span>);
</code></pre>
<!-- codeblock-end -->

- 1: program finished

- 2: Cannot predict the order

- 3: program finished, promise finished

- 4: promise finished, program finished  

==================== Answer ====================  

Answer: 3

Even though a promise is resolved immediately, it won't be executed immediately because its **.then/catch/finally** handlers or callbacks(aka task) are pushed into the queue. Whenever the JavaScript engine becomes free from the current program, it pulls a task from the queue and executes it. This is the reason why last statement is printed first before the log of promise handler.

**Note:** We call the above queue as "MicroTask Queue"

==================== Id ====================  
509

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#509-What-is-the-output-of-below-code-javas

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
