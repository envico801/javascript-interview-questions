==================== Question ====================  

### How do you redirect new page in javascript  

==================== Answer ====================  

In vanilla javascript, you can redirect to a new page using the `location` property of window object. The syntax would be as follows,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">redirect</span>(<span class="hljs-params"></span>) {
  <span class="hljs-variable language_">window</span>.<span class="hljs-property">location</span>.<span class="hljs-property">href</span> = <span class="hljs-string">'newPage.html'</span>;
}
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
119

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#119-How-do-you-redirect-new-page-in-javascript

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
