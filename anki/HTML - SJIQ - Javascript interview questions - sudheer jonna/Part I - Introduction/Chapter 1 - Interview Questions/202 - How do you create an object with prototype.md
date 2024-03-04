==================== Question ====================  

### How do you create an object with prototype  

==================== Answer ====================  

The Object.create() method is used to create a new object with the specified prototype object and properties. i.e, It uses an existing object as the prototype of the newly created object. It returns a new object with the specified prototype object and properties.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> user = {
  <span class="hljs-attr">name</span>: <span class="hljs-string">'John'</span>,
  <span class="hljs-attr">printInfo</span>: <span class="hljs-keyword">function</span> (<span class="hljs-params"></span>) {
     <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">`My name is <span class="hljs-subst">${<span class="hljs-variable language_">this</span>.name}</span>.`</span>);
  },
};
<span class="hljs-keyword">const</span> admin = <span class="hljs-title class_">Object</span>.<span class="hljs-title function_">create</span>(user);
admin.<span class="hljs-property">name</span> = <span class="hljs-string">'Nick'</span>; <span class="hljs-comment">// Remember that "name" is a property set on "admin" but not on "user" object</span>
admin.<span class="hljs-title function_">printInfo</span>(); <span class="hljs-comment">// My name is Nick</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
202

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#202-How-do-you-create-an-object-with-prototype

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
