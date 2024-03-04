==================== Question ====================  

### What are classes in ES6  

==================== Answer ====================  

In ES6, Javascript classes are primarily syntactic sugar over JavaScript’s existing prototype-based inheritance.

For example, the prototype based inheritance written in function expression as below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">Bike</span>(<span class="hljs-params">model, color</span>) {
  <span class="hljs-variable language_">this</span>.<span class="hljs-property">model</span> = model;
  <span class="hljs-variable language_">this</span>.<span class="hljs-property">color</span> = color;
}
<span class="hljs-title class_">Bike</span>.<span class="hljs-property"><span class="hljs-keyword">prototype</span></span>.<span class="hljs-property">getDetails</span> = <span class="hljs-keyword">function</span> (<span class="hljs-params"></span>) {
  <span class="hljs-keyword">return</span> <span class="hljs-variable language_">this</span>.<span class="hljs-property">model</span> + <span class="hljs-string">' bike has'</span> + <span class="hljs-variable language_">this</span>.<span class="hljs-property">color</span> + <span class="hljs-string">' color'</span>;
};
</code></pre>
<!-- codeblock-end -->

Whereas ES6 classes can be defined as an alternative

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">class</span> <span class="hljs-title class_">Bike</span> {
  <span class="hljs-title function_">constructor</span>(<span class="hljs-params">color, model</span>) {
     <span class="hljs-variable language_">this</span>.<span class="hljs-property">color</span> = color;
     <span class="hljs-variable language_">this</span>.<span class="hljs-property">model</span> = model;
  }
  <span class="hljs-title function_">getDetails</span>(<span class="hljs-params"></span>) {
     <span class="hljs-keyword">return</span> <span class="hljs-variable language_">this</span>.<span class="hljs-property">model</span> + <span class="hljs-string">' bike has'</span> + <span class="hljs-variable language_">this</span>.<span class="hljs-property">color</span> + <span class="hljs-string">' color'</span>;
  }
}
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
26

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#26-What-are-classes-in-es6

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
