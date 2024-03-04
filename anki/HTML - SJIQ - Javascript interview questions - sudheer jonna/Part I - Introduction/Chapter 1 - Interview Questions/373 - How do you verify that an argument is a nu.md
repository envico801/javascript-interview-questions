==================== Question ====================  

### How do you verify that an argument is a Number or not  

==================== Answer ====================  

The combination of IsNaN and isFinite methods are used to confirm whether an argument is a number or not.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">isNumber</span>(<span class="hljs-params">n</span>) {
  <span class="hljs-keyword">return</span> !<span class="hljs-built_in">isNaN</span>(<span class="hljs-built_in">parseFloat</span>(n)) &#x26;&#x26; <span class="hljs-built_in">isFinite</span>(n);
}
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
373

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#373-How-do-you-verify-that-an-argument-is-a-nu

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
