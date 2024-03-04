==================== Question ====================  

### What is a spread operator  

==================== Answer ====================  

Spread operator allows iterables( arrays / objects / strings ) to be expanded into single arguments/elements. Let's take an example to see this behavior,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">calculateSum</span>(<span class="hljs-params">x, y, z</span>) {
  <span class="hljs-keyword">return</span> x + y + z;
}
<span class="hljs-keyword">const</span> numbers = [<span class="hljs-number">1</span>, <span class="hljs-number">2</span>, <span class="hljs-number">3</span>];
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-title function_">calculateSum</span>(...numbers)); <span class="hljs-comment">// 6</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
188

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#188-What-is-a-spread-operator

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
