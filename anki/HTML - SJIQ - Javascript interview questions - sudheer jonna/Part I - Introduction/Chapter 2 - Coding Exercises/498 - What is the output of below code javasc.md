==================== Question ====================  

### What is the output of below code

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">Person</span>(<span class="hljs-params"></span>) {}
<span class="hljs-title class_">Person</span>.<span class="hljs-property"><span class="hljs-keyword">prototype</span></span>.<span class="hljs-property">walk</span> = <span class="hljs-keyword">function</span> (<span class="hljs-params"></span>) {
  <span class="hljs-keyword">return</span> <span class="hljs-variable language_">this</span>;
};
<span class="hljs-title class_">Person</span>.<span class="hljs-property">run</span> = <span class="hljs-keyword">function</span> (<span class="hljs-params"></span>) {
  <span class="hljs-keyword">return</span> <span class="hljs-variable language_">this</span>;
};
<span class="hljs-keyword">let</span> user = <span class="hljs-keyword">new</span> <span class="hljs-title class_">Person</span>();
<span class="hljs-keyword">let</span> walk = user.<span class="hljs-property">walk</span>;
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-title function_">walk</span>());
<span class="hljs-keyword">let</span> run = <span class="hljs-title class_">Person</span>.<span class="hljs-property">run</span>;
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-title function_">run</span>());
</code></pre>
<!-- codeblock-end -->

- 1: undefined, undefined

- 2: Person, Person

- 3: SyntaxError

- 4: Window, Window  

==================== Answer ====================  

Answer: 4

When a regular or prototype method is called without a value for **this**, the methods return an initial this value if the value is not undefined. Otherwise global window object will be returned. In our case, the initial `this` value is undefined so both methods return window objects.

==================== Id ====================  
498

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#498-What-is-the-output-of-below-code-javasc

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
