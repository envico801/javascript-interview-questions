==================== Question ====================  

### What is referential transparency?  

==================== Answer ====================  

An expression in javascript that can be replaced by its value without affecting the behaviour of the program is called referential transparency. Pure functions are referentially transparent.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> <span class="hljs-title function_">add</span> = (<span class="hljs-params">x, y</span>) => x + y;
<span class="hljs-keyword">const</span> <span class="hljs-title function_">multiplyBy2</span> = (<span class="hljs-params">x</span>) => x * <span class="hljs-number">2</span>;
<span class="hljs-comment">//Now add (2, 3) can be replaced by 5.</span>
<span class="hljs-title function_">multiplyBy2</span>(<span class="hljs-title function_">add</span>(<span class="hljs-number">2</span>, <span class="hljs-number">3</span>));
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
443

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#443-What-is-referential-transparency

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
