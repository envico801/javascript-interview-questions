==================== Question ====================  

### What is an error object  

==================== Answer ====================  

An error object is a built in error object that provides error information when an error occurs. It has two properties: name and message. For example, the below function logs error details,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">try</span> {
  <span class="hljs-title function_">greeting</span>(<span class="hljs-string">'Welcome'</span>);
} <span class="hljs-keyword">catch</span> (err) {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(err.<span class="hljs-property">name</span> + <span class="hljs-string">'&#x3C;br>'</span> + err.<span class="hljs-property">message</span>);
}
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
226

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#226-What-is-an-error-object

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
