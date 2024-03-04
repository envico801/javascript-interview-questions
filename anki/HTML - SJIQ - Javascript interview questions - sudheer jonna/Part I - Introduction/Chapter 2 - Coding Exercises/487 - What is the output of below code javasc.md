==================== Question ====================  

### What is the output of below code

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">checkType</span>(<span class="hljs-params">num = <span class="hljs-number">1</span></span>) {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-keyword">typeof</span> num);
}
<span class="hljs-title function_">checkType</span>();
<span class="hljs-title function_">checkType</span>(<span class="hljs-literal">undefined</span>);
<span class="hljs-title function_">checkType</span>(<span class="hljs-string">''</span>);
<span class="hljs-title function_">checkType</span>(<span class="hljs-literal">null</span>);
</code></pre>
<!-- codeblock-end -->

- 1: number, undefined, string, object

- 2: undefined, undefined, string, object

- 3: number, number, string, object

- 4: number, number, number, number  

==================== Answer ====================  

Answer: 3

If the function argument is set implicitly(not passing argument) or explicitly to undefined, the value of the argument is the default parameter. Whereas for other falsy values('' or null), the value of the argument is passed as a parameter.

Hence, the result of function calls categorized as below,

1. The first two function calls logs number type since the type of default value is number

2. The type of '' and null values are string and object type respectively.

==================== Id ====================  
487

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#487-What-is-the-output-of-below-code-javasc

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
