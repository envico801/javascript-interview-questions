==================== Question ====================  

### How do you get enumerable key and value pairs  

==================== Answer ====================  

The Object.entries() method is used to return an array of a given object's own enumerable string-keyed property [key, value] pairs, in the same order as that provided by a for...in loop. Let's see the functionality of object.entries() method in an example,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> object = {
  <span class="hljs-attr">a</span>: <span class="hljs-string">'Good morning'</span>,
  <span class="hljs-attr">b</span>: <span class="hljs-number">100</span>,
};
<span class="hljs-keyword">for</span> (<span class="hljs-keyword">let</span> [key, value] <span class="hljs-keyword">of</span> <span class="hljs-title class_">Object</span>.<span class="hljs-title function_">entries</span>(object)) {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">`<span class="hljs-subst">${key}</span>: <span class="hljs-subst">${value}</span>`</span>); <span class="hljs-comment">// a: 'Good morning'</span>
  <span class="hljs-comment">// b: 100</span>
}
</code></pre>
<!-- codeblock-end -->

**Note:** The order is not guaranteed as object defined.

==================== Id ====================  
199

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#199-How-do-you-get-enumerable-key-and-value-pa

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
