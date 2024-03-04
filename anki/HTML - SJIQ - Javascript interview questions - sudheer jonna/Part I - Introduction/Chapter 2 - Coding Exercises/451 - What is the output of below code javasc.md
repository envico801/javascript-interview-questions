==================== Question ====================  

### What is the output of below code

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">foo</span>(<span class="hljs-params"></span>) {
  <span class="hljs-keyword">let</span> x = (y = <span class="hljs-number">0</span>);
  x++;
  y++;
  <span class="hljs-keyword">return</span> x;
}
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-title function_">foo</span>(), <span class="hljs-keyword">typeof</span> x, <span class="hljs-keyword">typeof</span> y);
</code></pre>
<!-- codeblock-end -->

- 1: 1, undefined and undefined

- 2: ReferenceError: X is not defined

- 3: 1, undefined and number

- 4: 1, number and number  

==================== Answer ====================  

Answer: 3

Of course the return value of `foo()` is 1 due to the increment operator. But the statement `let x = y = 0` declares a local variable x. Whereas y declared as a global variable accidentally. This statement is equivalent to,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">let</span> x;
<span class="hljs-variable language_">window</span>.<span class="hljs-property">y</span> = <span class="hljs-number">0</span>;
x = <span class="hljs-variable language_">window</span>.<span class="hljs-property">y</span>;
</code></pre>
<!-- codeblock-end -->

Since the block scoped variable x is undefined outside of the function, the type will be undefined too. Whereas the global variable `y` is available outside the function, the value is 0 and type is number.

==================== Id ====================  
451

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#451-What-is-the-output-of-below-code-javasc

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
