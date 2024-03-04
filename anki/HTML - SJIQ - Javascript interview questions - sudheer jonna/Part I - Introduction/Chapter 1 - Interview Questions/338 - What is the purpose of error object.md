==================== Question ====================  

### What is the purpose of Error object  

==================== Answer ====================  

The Error constructor creates an error object and the instances of error objects are thrown when runtime errors occur. The Error object can also be used as a base object for user-defined exceptions. The syntax of error object would be as below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">new</span> <span class="hljs-title class_">Error</span>([message[, fileName[, lineNumber]]])
</code></pre>
<!-- codeblock-end -->

You can throw user defined exceptions or errors using Error object in try...catch block as below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">try</span> {
  <span class="hljs-keyword">if</span> (withdraw > balance) <span class="hljs-keyword">throw</span> <span class="hljs-keyword">new</span> <span class="hljs-title class_">Error</span>(<span class="hljs-string">"Oops! You don't have enough balance"</span>);
} <span class="hljs-keyword">catch</span> (e) {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(e.<span class="hljs-property">name</span> + <span class="hljs-string">': '</span> + e.<span class="hljs-property">message</span>);
}
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
338

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#338-What-is-the-purpose-of-error-object

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
