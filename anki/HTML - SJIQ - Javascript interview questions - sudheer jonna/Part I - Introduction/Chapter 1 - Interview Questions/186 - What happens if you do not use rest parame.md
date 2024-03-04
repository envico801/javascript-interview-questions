==================== Question ====================  

### What happens if you do not use rest parameter as a last argument  

==================== Answer ====================  

The rest parameter should be the last argument, as its job is to collect all the remaining arguments into an array. For example, if you define a function like below it doesn’t make any sense and will throw an error.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">someFunc</span>(<span class="hljs-params">a,…b,c</span>){
<span class="hljs-comment">//You code goes here</span>
<span class="hljs-keyword">return</span>;
}
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
186

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#186-What-happens-if-you-do-not-use-rest-parame

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
