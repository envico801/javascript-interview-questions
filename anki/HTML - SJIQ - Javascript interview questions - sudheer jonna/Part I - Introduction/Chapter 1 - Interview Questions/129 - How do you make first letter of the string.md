==================== Question ====================  

### How do you make first letter of the string in an uppercase  

==================== Answer ====================  

You can create a function which uses a chain of string methods such as charAt, toUpperCase and slice methods to generate a string with the first letter in uppercase.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">capitalizeFirstLetter</span>(<span class="hljs-params">string</span>) {
  <span class="hljs-keyword">return</span> string.<span class="hljs-title function_">charAt</span>(<span class="hljs-number">0</span>).<span class="hljs-title function_">toUpperCase</span>() + string.<span class="hljs-title function_">slice</span>(<span class="hljs-number">1</span>);
}
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
129

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#129-How-do-you-make-first-letter-of-the-string

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
