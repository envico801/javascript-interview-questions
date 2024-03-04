==================== Question ====================  

### How do you check web workers browser support  

==================== Answer ====================  

You need to check browser support for web workers before using it

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">if</span> (<span class="hljs-keyword">typeof</span> <span class="hljs-title class_">Worker</span> !== <span class="hljs-string">'undefined'</span>) {
  <span class="hljs-comment">// code for Web worker support.</span>
} <span class="hljs-keyword">else</span> {
  <span class="hljs-comment">// Sorry! No Web Worker support..</span>
}
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
48

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#48-How-do-you-check-web-workers-browser-suppo

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
