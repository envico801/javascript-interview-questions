==================== Question ====================  

### What are the function parameter rules  

==================== Answer ====================  

JavaScript functions follow below rules for parameters,

1. The function definitions do not specify data types for parameters.

2. Do not perform type checking on the passed arguments.

3. Do not check the number of arguments received.

    i.e, The below function follows the above rules,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">functionName</span>(<span class="hljs-params">parameter1, parameter2, parameter3</span>) {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(parameter1); <span class="hljs-comment">// 1</span>
}
<span class="hljs-title function_">functionName</span>(<span class="hljs-number">1</span>);
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
225

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#225-What-are-the-function-parameter-rules

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
