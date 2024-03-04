==================== Question ====================  

### How can you get the list of keys of any object  

==================== Answer ====================  

You can use the `Object.keys()` method which is used to return an array of a given object's own property names, in the same order as we get with a normal loop. For example, you can get the keys of a user object,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> user = {
  <span class="hljs-attr">name</span>: <span class="hljs-string">'John'</span>,
  <span class="hljs-attr">gender</span>: <span class="hljs-string">'male'</span>,
  <span class="hljs-attr">age</span>: <span class="hljs-number">40</span>,
};
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-title class_">Object</span>.<span class="hljs-title function_">keys</span>(user)); <span class="hljs-comment">//['name', 'gender', 'age']</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
201

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#201-How-can-you-get-the-list-of-keys-of-any-ob

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
