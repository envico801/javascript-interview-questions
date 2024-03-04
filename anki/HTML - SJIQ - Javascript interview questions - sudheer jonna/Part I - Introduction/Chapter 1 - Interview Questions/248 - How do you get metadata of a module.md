==================== Question ====================  

### How do you get metadata of a module  

==================== Answer ====================  

You can use the `import.meta` object which is a meta-property exposing context-specific meta data to a JavaScript module. It contains information about the current module, such as the module's URL. In browsers, you might get different meta data than NodeJS.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript">&#x3C;script type=<span class="hljs-string">'module'</span> src=<span class="hljs-string">'welcome-module.js'</span>>&#x3C;/script>;
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-keyword">import</span>.<span class="hljs-property">meta</span>); <span class="hljs-comment">// { url: "file:///home/user/welcome-module.js" }</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
248

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#248-How-do-you-get-metadata-of-a-module

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
