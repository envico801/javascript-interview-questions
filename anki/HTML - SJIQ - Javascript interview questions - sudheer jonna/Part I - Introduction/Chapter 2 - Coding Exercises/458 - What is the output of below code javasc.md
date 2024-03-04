==================== Question ====================  

### What is the output of below code

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> obj = {
  <span class="hljs-attr">prop1</span>: <span class="hljs-keyword">function</span> (<span class="hljs-params"></span>) {
     <span class="hljs-keyword">return</span> <span class="hljs-number">0</span>;
  },
  <span class="hljs-title function_">prop2</span>(<span class="hljs-params"></span>) {
     <span class="hljs-keyword">return</span> <span class="hljs-number">1</span>;
  },
  [<span class="hljs-string">'prop'</span> + <span class="hljs-number">3</span>]() {
     <span class="hljs-keyword">return</span> <span class="hljs-number">2</span>;
  },
};
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(obj.<span class="hljs-title function_">prop1</span>());
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(obj.<span class="hljs-title function_">prop2</span>());
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(obj.<span class="hljs-title function_">prop3</span>());
</code></pre>
<!-- codeblock-end -->

- 1: 0, 1, 2

- 2: 0, { return 1 }, 2

- 3: 0, { return 1 }, { return 2 }

- 4: 0, 1, undefined  

==================== Answer ====================  

Answer: 1

ES6 provides method definitions and property shorthands for objects. So both prop2 and prop3 are treated as regular function values.

==================== Id ====================  
458

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#458-What-is-the-output-of-below-code-javasc

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
