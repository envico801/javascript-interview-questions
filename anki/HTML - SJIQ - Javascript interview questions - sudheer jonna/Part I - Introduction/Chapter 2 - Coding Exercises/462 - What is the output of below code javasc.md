==================== Question ====================  

### What is the output of below code

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> <span class="hljs-title function_">arrowFunc</span> = (<span class="hljs-params"></span>) => <span class="hljs-variable language_">arguments</span>.<span class="hljs-property">length</span>;
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-title function_">arrowFunc</span>(<span class="hljs-number">1</span>, <span class="hljs-number">2</span>, <span class="hljs-number">3</span>));
</code></pre>
<!-- codeblock-end -->

- 1: ReferenceError: arguments is not defined

- 2: 3

- 3: undefined

- 4: null  

==================== Answer ====================  

Answer: 1

Arrow functions do not have an `arguments, super, this, or new.target` bindings. So any reference to `arguments` variable tries to resolve to a binding in a lexically enclosing environment. In this case, the arguments variable is not defined outside of the arrow function. Hence, you will receive a reference error.

Where as the normal function provides the number of arguments passed to the function

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> func = <span class="hljs-keyword">function</span> (<span class="hljs-params"></span>) {
  <span class="hljs-keyword">return</span> <span class="hljs-variable language_">arguments</span>.<span class="hljs-property">length</span>;
};
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-title function_">func</span>(<span class="hljs-number">1</span>, <span class="hljs-number">2</span>, <span class="hljs-number">3</span>));
</code></pre>
<!-- codeblock-end -->

But If you still want to use an arrow function then rest operator on arguments provides the expected arguments

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> <span class="hljs-title function_">arrowFunc</span> = (<span class="hljs-params">...args</span>) => args.<span class="hljs-property">length</span>;
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-title function_">arrowFunc</span>(<span class="hljs-number">1</span>, <span class="hljs-number">2</span>, <span class="hljs-number">3</span>));
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
462

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#462-What-is-the-output-of-below-code-javasc

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
