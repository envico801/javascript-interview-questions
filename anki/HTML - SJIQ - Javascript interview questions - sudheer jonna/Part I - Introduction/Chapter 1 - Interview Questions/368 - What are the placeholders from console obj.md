==================== Question ====================  

### What are the placeholders from console object  

==================== Answer ====================  

Below are the list of placeholders available from console object,

1. %o — It takes an object,

2. %s — It takes a string,

3. %d — It is used for a decimal or integer

    These placeholders can be represented in the console.log as below

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> user = { <span class="hljs-attr">name</span>: <span class="hljs-string">'John'</span>, <span class="hljs-attr">id</span>: <span class="hljs-number">1</span>, <span class="hljs-attr">city</span>: <span class="hljs-string">'Delhi'</span> };
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'Hello %s, your details %o are available in the object form'</span>, <span class="hljs-string">'John'</span>, user); <span class="hljs-comment">// Hello John, your details {name: "John", id: 1, city: "Delhi"} are available in object</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
368

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#368-What-are-the-placeholders-from-console-obj

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
