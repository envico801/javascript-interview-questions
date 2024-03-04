==================== Question ====================  

### What is the purpose of isFinite function  

==================== Answer ====================  

The isFinite() function is used to determine whether a number is a finite, legal number. It returns false if the value is +infinity, -infinity, or NaN (Not-a-Number), otherwise it returns true.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-built_in">isFinite</span>(<span class="hljs-title class_">Infinity</span>); <span class="hljs-comment">// false</span>
<span class="hljs-built_in">isFinite</span>(<span class="hljs-title class_">NaN</span>); <span class="hljs-comment">// false</span>
<span class="hljs-built_in">isFinite</span>(-<span class="hljs-title class_">Infinity</span>); <span class="hljs-comment">// false</span>
<span class="hljs-built_in">isFinite</span>(<span class="hljs-number">100</span>); <span class="hljs-comment">// true</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
84

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#84-What-is-the-purpose-of-isfinite-function

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
