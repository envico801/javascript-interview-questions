==================== Question ====================  

### What is the output of below code

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> y = <span class="hljs-number">1</span>;
<span class="hljs-keyword">if</span> (<span class="hljs-keyword">function</span> <span class="hljs-title function_">f</span>(<span class="hljs-params"></span>) {}) {
  y += <span class="hljs-keyword">typeof</span> f;
}
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(y);
</code></pre>
<!-- codeblock-end -->

- 1: 1function

- 2: 1object

- 3: ReferenceError

- 4: 1undefined  

==================== Answer ====================  

Answer: 4

The main points in the above code snippets are,

1. You can see function expression instead function declaration inside if statement. So it always returns true.

2. Since it is not declared(or assigned) anywhere, f is undefined and typeof f is undefined too.

In other words, it is same as

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> y = <span class="hljs-number">1</span>;
<span class="hljs-keyword">if</span> (<span class="hljs-string">'foo'</span>) {
  y += <span class="hljs-keyword">typeof</span> f;
}
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(y);
</code></pre>
<!-- codeblock-end -->

**Note:** It returns 1object for MS Edge browser

==================== Id ====================  
454

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#454-What-is-the-output-of-below-code-javasc

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
