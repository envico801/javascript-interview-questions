==================== Question ====================  

### What is the output of below function calls

**Code snippet:**

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> circle = {
  <span class="hljs-attr">radius</span>: <span class="hljs-number">20</span>,
  <span class="hljs-title function_">diameter</span>(<span class="hljs-params"></span>) {
     <span class="hljs-keyword">return</span> <span class="hljs-variable language_">this</span>.<span class="hljs-property">radius</span> * <span class="hljs-number">2</span>;
  },
  <span class="hljs-attr">perimeter</span>: <span class="hljs-function">() =></span> <span class="hljs-number">2</span> * <span class="hljs-title class_">Math</span>.<span class="hljs-property">PI</span> * <span class="hljs-variable language_">this</span>.<span class="hljs-property">radius</span>,
};
</code></pre>
<!-- codeblock-end -->

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(circle.<span class="hljs-title function_">diameter</span>());
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(circle.<span class="hljs-title function_">perimeter</span>());
</code></pre>
<!-- codeblock-end -->  

==================== Answer ====================  

**Output:**

The output is 40 and NaN. Remember that diameter is a regular function, whereas the value of perimeter is an arrow function. The `this` keyword of a regular function(i.e, diameter) refers to the surrounding scope which is a class(i.e, Shape object). Whereas this keyword of perimeter function refers to the surrounding scope which is a window object. Since there is no radius property on window objects it returns an undefined value and the multiple of number value returns NaN value.

==================== Id ====================  
353

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#353-What-is-the-output-of-below-function-calls

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
