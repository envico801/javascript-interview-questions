==================== Question ====================  

### What is the output order of below code?

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-built_in">setTimeout</span>(<span class="hljs-function">() =></span> {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'1'</span>);
}, <span class="hljs-number">0</span>);
<span class="hljs-title class_">Promise</span>.<span class="hljs-title function_">resolve</span>(<span class="hljs-string">'hello'</span>).<span class="hljs-title function_">then</span>(<span class="hljs-function">() =></span> <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'2'</span>));
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'3'</span>);
</code></pre>
<!-- codeblock-end -->

- 1: 1, 2, 3

- 2: 1, 3, 2

- 3: 3, 1, 2

- 4: 3, 2, 1  

==================== Answer ====================  

Answer: 4

When the JavaScript engine parses the above code, the first two statements are asynchronous which will be executed later and third statement is synchronous statement which will be moved to callstack, executed and prints the number 3 in the console. Next, Promise is native in ES6 and it will be moved to Job queue which has high priority than callback queue in the execution order. At last, since setTimeout is part of WebAPI the callback function moved to callback queue and executed. Hence, you will see number 2 printed first followed by 1.

==================== Id ====================  
514

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#514-What-is-the-output-order-of-below-code

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
