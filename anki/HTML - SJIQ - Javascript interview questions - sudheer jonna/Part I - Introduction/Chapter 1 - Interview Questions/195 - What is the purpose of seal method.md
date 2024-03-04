==================== Question ====================  

### What is the purpose of seal method  

==================== Answer ====================  

The **Object.seal()** method is used to seal an object, by preventing new properties from being added to it and marking all existing properties as non-configurable. But values of present properties can still be changed as long as they are writable. Let's see the below example to understand more about seal() method

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> object = {
  <span class="hljs-attr">property</span>: <span class="hljs-string">'Welcome JS world'</span>,
};
<span class="hljs-title class_">Object</span>.<span class="hljs-title function_">seal</span>(object);
object.<span class="hljs-property">property</span> = <span class="hljs-string">'Welcome to object world'</span>;
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-title class_">Object</span>.<span class="hljs-title function_">isSealed</span>(object)); <span class="hljs-comment">// true</span>
<span class="hljs-keyword">delete</span> object.<span class="hljs-property">property</span>; <span class="hljs-comment">// You cannot delete when sealed</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(object.<span class="hljs-property">property</span>); <span class="hljs-comment">//Welcome to object world</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
195

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#195-What-is-the-purpose-of-seal-method

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
