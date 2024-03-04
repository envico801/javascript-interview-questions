==================== Question ====================  

### What is the main difference between Object.values and Object.entries method  

==================== Answer ====================  

The Object.values() method's behavior is similar to Object.entries() method but it returns an array of values instead [key,value] pairs.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> object = {
  <span class="hljs-attr">a</span>: <span class="hljs-string">'Good morning'</span>,
  <span class="hljs-attr">b</span>: <span class="hljs-number">100</span>,
};
<span class="hljs-keyword">for</span> (<span class="hljs-keyword">let</span> value <span class="hljs-keyword">of</span> <span class="hljs-title class_">Object</span>.<span class="hljs-title function_">values</span>(object)) {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">`<span class="hljs-subst">${value}</span>`</span>); <span class="hljs-comment">// 'Good morning'</span>
  <span class="hljs-number">100</span>;
}
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
200

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#200-What-is-the-main-difference-between-object

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
