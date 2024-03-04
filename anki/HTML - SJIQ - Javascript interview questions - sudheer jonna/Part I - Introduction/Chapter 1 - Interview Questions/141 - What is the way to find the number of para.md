==================== Question ====================  

### What is the way to find the number of parameters expected by a function  

==================== Answer ====================  

You can use `function.length` syntax to find the number of parameters expected by a function. Let's take an example of `sum` function to calculate the sum of numbers,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">sum</span>(<span class="hljs-params">num1, num2, num3, num4</span>) {
  <span class="hljs-keyword">return</span> num1 + num2 + num3 + num4;
}
sum.<span class="hljs-property">length</span>; <span class="hljs-comment">// 4 is the number of parameters expected.</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
141

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#141-What-is-the-way-to-find-the-number-of-para

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
