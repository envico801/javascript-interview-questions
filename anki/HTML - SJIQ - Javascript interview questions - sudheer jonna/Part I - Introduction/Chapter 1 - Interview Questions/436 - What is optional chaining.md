==================== Question ====================  

### What is optional chaining?  

==================== Answer ====================  

According to MDN official docs, the optional chaining operator (?.) permits reading the value of a property located deep within a chain of connected objects without having to expressly validate that each reference in the chain is valid.

The ?. operator is like the . chaining operator, except that instead of causing an error if a reference is nullish (null or undefined), the expression short-circuits with a return value of undefined. When used with function calls, it returns undefined if the given function does not exist.

<!-- codeblock-start -->
<pre><code class="hljs language-js"><span class="hljs-keyword">const</span> adventurer = {
  <span class="hljs-attr">name</span>: <span class="hljs-string">'Alice'</span>,
  <span class="hljs-attr">cat</span>: {
     <span class="hljs-attr">name</span>: <span class="hljs-string">'Dinah'</span>,
  },
};
<span class="hljs-keyword">const</span> dogName = adventurer.<span class="hljs-property">dog</span>?.<span class="hljs-property">name</span>;
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(dogName);
<span class="hljs-comment">// expected output: undefined</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(adventurer.<span class="hljs-property">someNonExistentMethod</span>?.());
<span class="hljs-comment">// expected output: undefined</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
436

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#436-What-is-optional-chaining

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
