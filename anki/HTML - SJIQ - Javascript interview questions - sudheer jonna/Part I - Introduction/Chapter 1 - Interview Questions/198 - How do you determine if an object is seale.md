==================== Question ====================  

### How do you determine if an object is sealed or not  

==================== Answer ====================  

The Object.isSealed() method is used to determine if an object is sealed or not. An object is sealed if all of the below conditions hold true

1. If it is not extensible.

2. If all of its properties are non-configurable.

3. If it is not removable (but not necessarily non-writable).

    Let's see it in the action

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> object = {
  <span class="hljs-attr">property</span>: <span class="hljs-string">'Hello, Good morning'</span>,
};
<span class="hljs-title class_">Object</span>.<span class="hljs-title function_">seal</span>(object); <span class="hljs-comment">// Using seal() method to seal the object</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-title class_">Object</span>.<span class="hljs-title function_">isSealed</span>(object)); <span class="hljs-comment">// checking whether the object is sealed or not</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
198

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#198-How-do-you-determine-if-an-object-is-seale

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
