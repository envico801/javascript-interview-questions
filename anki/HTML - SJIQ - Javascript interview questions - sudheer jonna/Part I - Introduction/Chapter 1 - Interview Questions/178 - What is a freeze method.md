==================== Question ====================  

### What is a freeze method  

==================== Answer ====================  

The **freeze()** method is used to freeze an object. Freezing an object does not allow adding new properties to an object,prevents from removing and prevents changing the enumerability, configurability, or writability of existing properties. i.e, It returns the passed object and does not create a frozen copy.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> obj = {
  <span class="hljs-attr">prop</span>: <span class="hljs-number">100</span>,
};
<span class="hljs-title class_">Object</span>.<span class="hljs-title function_">freeze</span>(obj);
obj.<span class="hljs-property">prop</span> = <span class="hljs-number">200</span>; <span class="hljs-comment">// Throws an error in strict mode</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(obj.<span class="hljs-property">prop</span>); <span class="hljs-comment">//100</span>
</code></pre>
<!-- codeblock-end -->

Remember freezing is only applied to the top-level properties in objects but not for nested objects.

For example, let's try to freeze user object which has employment details as nested object and observe that details have been changed.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> user = {
  <span class="hljs-attr">name</span>: <span class="hljs-string">'John'</span>,
  <span class="hljs-attr">employment</span>: {
     <span class="hljs-attr">department</span>: <span class="hljs-string">'IT'</span>,
  },
};
<span class="hljs-title class_">Object</span>.<span class="hljs-title function_">freeze</span>(user);
user.<span class="hljs-property">employment</span>.<span class="hljs-property">department</span> = <span class="hljs-string">'HR'</span>;
</code></pre>
<!-- codeblock-end -->

**Note:** It causes a TypeError if the argument passed is not an object.

==================== Id ====================  
178

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#178-What-is-a-freeze-method

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
