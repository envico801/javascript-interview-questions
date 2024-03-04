==================== Question ====================  

### How do you check if a string starts with another string  

==================== Answer ====================  

You can use ECMAScript 6's `String.prototype.startsWith()` method to check if a string starts with another string or not. But it is not yet supported in all browsers. Let's see an example to see this usage,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-string">'Good morning'</span>.<span class="hljs-title function_">startsWith</span>(<span class="hljs-string">'Good'</span>); <span class="hljs-comment">// true</span>
<span class="hljs-string">'Good morning'</span>.<span class="hljs-title function_">startsWith</span>(<span class="hljs-string">'morning'</span>); <span class="hljs-comment">// false</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
133

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#133-How-do-you-check-if-a-string-starts-with-a

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
