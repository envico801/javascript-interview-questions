==================== Question ====================  

### How do you check web storage browser support  

==================== Answer ====================  

You need to check browser support for localStorage and sessionStorage before using web storage,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">if</span> (<span class="hljs-keyword">typeof</span> <span class="hljs-title class_">Storage</span> !== <span class="hljs-string">'undefined'</span>) {
  <span class="hljs-comment">// Code for localStorage/sessionStorage.</span>
} <span class="hljs-keyword">else</span> {
  <span class="hljs-comment">// Sorry! No Web Storage support..</span>
}
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
47

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#47-How-do-you-check-web-storage-browser-suppo

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
