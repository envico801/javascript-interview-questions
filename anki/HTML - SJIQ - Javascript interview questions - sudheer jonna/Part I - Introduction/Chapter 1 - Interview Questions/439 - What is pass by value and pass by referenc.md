==================== Question ====================  

### What is pass by value and pass by reference?  

==================== Answer ====================  

Pass-by-value creates a new space in memory and makes a copy of a value. Primitives such as string, number, boolean etc will actually create a new copy. Hence, updating one value doesn't impact the other value. i.e, The values are independent of each other.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">let</span> a = <span class="hljs-number">5</span>;
<span class="hljs-keyword">let</span> b = a;
b++;
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(a, b); <span class="hljs-comment">//5, 6</span>
</code></pre>
<!-- codeblock-end -->

In the above code snippet, the value of `a` is assigned to `b` and the variable `b` has been incremented. Since there is a new space created for variable `b`, any update on this variable doesn't impact the variable `a`.

Pass by reference doesn't create a new space in memory but the new variable adopts a memory address of an initial variable. Non-primitives such as objects, arrays and functions gets the reference of the initiable variable. i.e, updating one value will impact the other variable.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">let</span> user1 = {
  <span class="hljs-attr">name</span>: <span class="hljs-string">'John'</span>,
  <span class="hljs-attr">age</span>: <span class="hljs-number">27</span>,
};
<span class="hljs-keyword">let</span> user2 = user1;
user2.<span class="hljs-property">age</span> = <span class="hljs-number">30</span>;
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(user1.<span class="hljs-property">age</span>, user2.<span class="hljs-property">age</span>); <span class="hljs-comment">// 30, 30</span>
</code></pre>
<!-- codeblock-end -->

In the above code snippet, updating the `age` property of one object will impact the other property due to the same reference.

==================== Id ====================  
439

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#439-What-is-pass-by-value-and-pass-by-referenc

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
