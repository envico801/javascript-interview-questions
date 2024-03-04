==================== Question ====================  

### How do you determine whether object is frozen or not  

==================== Answer ====================  

Object.isFrozen() method is used to determine if an object is frozen or not.An object is frozen if all of the below conditions hold true,

1. If it is not extensible.

2. If all of its properties are non-configurable.

3. If all its data properties are non-writable.

    The usage is going to be as follows,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> object = {
  <span class="hljs-attr">property</span>: <span class="hljs-string">'Welcome JS world'</span>,
};
<span class="hljs-title class_">Object</span>.<span class="hljs-title function_">freeze</span>(object);
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-title class_">Object</span>.<span class="hljs-title function_">isFrozen</span>(object));
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
189

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#189-How-do-you-determine-whether-object-is-fro

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
