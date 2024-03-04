==================== Question ====================  

### What is destructuring aliases  

==================== Answer ====================  

Sometimes you would like to have a destructured variable with a different name than the property name. In that case, you'll use a `: newName` to specify a name for the variable. This process is called destructuring aliases.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> obj = { <span class="hljs-attr">x</span>: <span class="hljs-number">1</span> };
<span class="hljs-comment">// Grabs obj.x as as { otherName }</span>
<span class="hljs-keyword">const</span> { <span class="hljs-attr">x</span>: otherName } = obj;
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
362

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#362-What-is-destructuring-aliases

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
