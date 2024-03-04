==================== Question ====================  

### What is the purpose of the this keyword in JavaScript?  

==================== Answer ====================  

- The `this` keyword in JavaScript is a special variable that is used within a function to refer to the object on which the function is invoked. The value of this depends on how the function is called. It allows functions to access and interact with the object they are bound to.

- The this keyword in JavaScript is a reference to the object that owns or invokes the current function. Its value is determined by the calling context.

  **Example 1: this in a Global Context**

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-variable language_">this</span>);
</code></pre>
<!-- codeblock-end -->

- In a global context, this refers to the global object (e.g., window in a browser).

**Example 2: this in a Function**

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">displayThis</span>(<span class="hljs-params"></span>) {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-variable language_">this</span>);
}
<span class="hljs-title function_">displayThis</span>();
</code></pre>
<!-- codeblock-end -->

- In a regular function, this refers to the global object.

**Example 3: this in a Method**

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> person = {
  <span class="hljs-attr">name</span>: <span class="hljs-string">'John'</span>,
  <span class="hljs-attr">greet</span>: <span class="hljs-keyword">function</span> (<span class="hljs-params"></span>) {
     <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'Hello, '</span> + <span class="hljs-variable language_">this</span>.<span class="hljs-property">name</span>);
  },
};
person.<span class="hljs-title function_">greet</span>();
</code></pre>
<!-- codeblock-end -->

- In a method, this refers to the object that owns the method (person in the case).

**Example 4: this in an Event Handler**

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-variable language_">document</span>.<span class="hljs-title function_">getElementById</span>(<span class="hljs-string">'myButton'</span>).<span class="hljs-title function_">addEventListener</span>(<span class="hljs-string">'click'</span>, <span class="hljs-keyword">function</span> (<span class="hljs-params"></span>) {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-variable language_">this</span>);
});
</code></pre>
<!-- codeblock-end -->

- In an event handler, this refers to the element that triggered the event (the button in this case).

==================== Id ====================  
449

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#449-What-is-the-purpose-of-the-this-keyword-in

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
