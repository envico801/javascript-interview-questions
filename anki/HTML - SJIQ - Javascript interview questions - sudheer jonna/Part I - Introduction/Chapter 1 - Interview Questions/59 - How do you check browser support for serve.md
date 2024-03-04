==================== Question ====================  

### How do you check browser support for server-sent events  

==================== Answer ====================  

You can perform browser support for server-sent events before using it as below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">if</span> (<span class="hljs-keyword">typeof</span> <span class="hljs-title class_">EventSource</span> !== <span class="hljs-string">'undefined'</span>) {
  <span class="hljs-comment">// Server-sent events supported. Let's have some code here!</span>
} <span class="hljs-keyword">else</span> {
  <span class="hljs-comment">// No server-sent events supported</span>
}
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
59

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#59-How-do-you-check-browser-support-for-serve

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
