==================== Question ====================  

### How do you redeclare variables in a switch block without an error  

==================== Answer ====================  

If you try to redeclare variables in a `switch block` then it will cause errors because there is only one block. For example, the below code block throws a syntax error as below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">let</span> counter = <span class="hljs-number">1</span>;
<span class="hljs-keyword">switch</span> (x) {
  <span class="hljs-keyword">case</span> <span class="hljs-number">0</span>:
     <span class="hljs-keyword">let</span> name;
     <span class="hljs-keyword">break</span>;
  <span class="hljs-keyword">case</span> <span class="hljs-number">1</span>:
     <span class="hljs-keyword">let</span> name; <span class="hljs-comment">// SyntaxError for redeclaration.</span>
     <span class="hljs-keyword">break</span>;
}
</code></pre>
<!-- codeblock-end -->

To avoid this error, you can create a nested block inside a case clause and create a new block scoped lexical environment.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">let</span> counter = <span class="hljs-number">1</span>;
<span class="hljs-keyword">switch</span> (x) {
  <span class="hljs-keyword">case</span> <span class="hljs-number">0</span>: {
     <span class="hljs-keyword">let</span> name;
     <span class="hljs-keyword">break</span>;
  }
  <span class="hljs-keyword">case</span> <span class="hljs-number">1</span>: {
     <span class="hljs-keyword">let</span> name; <span class="hljs-comment">// No SyntaxError for redeclaration.</span>
     <span class="hljs-keyword">break</span>;
  }
}
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
20

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#20-How-do-you-redeclare-variables-in-a-switch

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
