==================== Question ====================  

### What is the output of below code

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">main</span>(<span class="hljs-params"></span>) {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'A'</span>);
  <span class="hljs-built_in">setTimeout</span>(<span class="hljs-keyword">function</span> <span class="hljs-title function_">print</span>(<span class="hljs-params"></span>) {
     <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'B'</span>);
  }, <span class="hljs-number">0</span>);
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'C'</span>);
}
<span class="hljs-title function_">main</span>();
</code></pre>
<!-- codeblock-end -->

- 1: A, B and C

- 2: B, A and C

- 3: A and C

- 4: A, C and B  

==================== Answer ====================  

Answer: 4

The statements order is based on the event loop mechanism. The order of statements follows the below order,

1. At first, the main function is pushed to the stack.

2. Then the browser pushes the first statement of the main function( i.e, A's console.log) to the stack, executing and popping out immediately.

3. But `setTimeout` statement moved to Browser API to apply the delay for callback.

4. In the meantime, C's console.log added to stack, executed and popped out.

5. The callback of `setTimeout` moved from Browser API to message queue.

6. The `main` function popped out from stack because there are no statements to execute

7. The callback moved from message queue to the stack since the stack is empty.

8. The console.log for B is added to the stack and display on the console.

==================== Id ====================  
452

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#452-What-is-the-output-of-below-code-javasc

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
