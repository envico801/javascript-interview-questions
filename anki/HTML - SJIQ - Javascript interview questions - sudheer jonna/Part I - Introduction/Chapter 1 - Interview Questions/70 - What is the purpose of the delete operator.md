==================== Question ====================  

### What is the purpose of the delete operator  

==================== Answer ====================  

The delete operator is used to delete the property as well as its value.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> user = { <span class="hljs-attr">firstName</span>: <span class="hljs-string">'John'</span>, <span class="hljs-attr">lastName</span>: <span class="hljs-string">'Doe'</span>, <span class="hljs-attr">age</span>: <span class="hljs-number">20</span> };
<span class="hljs-keyword">delete</span> user.<span class="hljs-property">age</span>;
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(user); <span class="hljs-comment">// {firstName: "John", lastName:"Doe"}</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
70

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#70-What-is-the-purpose-of-the-delete-operator

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
