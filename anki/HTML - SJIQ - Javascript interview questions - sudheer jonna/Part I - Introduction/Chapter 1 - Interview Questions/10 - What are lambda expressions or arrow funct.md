==================== Question ====================  

### What are lambda expressions or arrow functions  

==================== Answer ====================  

An arrow function is a shorter/concise syntax for a function expression and does not have its own **this, arguments, super, or new.target**. These functions are best suited for non-method functions, and they cannot be used as constructors.

Some of the examples of arrow functions are listed as below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> <span class="hljs-title function_">arrowFunc1</span> = (<span class="hljs-params">a, b</span>) => a + b; <span class="hljs-comment">// Multiple parameters</span>
<span class="hljs-keyword">const</span> <span class="hljs-title function_">arrowFunc2</span> = (<span class="hljs-params">a</span>) => a * <span class="hljs-number">10</span>; <span class="hljs-comment">// Single parameter</span>
<span class="hljs-keyword">const</span> <span class="hljs-title function_">arrowFunc3</span> = (<span class="hljs-params"></span>) => {}; <span class="hljs-comment">// no parameters</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
10

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#10-What-are-lambda-expressions-or-arrow-funct

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
