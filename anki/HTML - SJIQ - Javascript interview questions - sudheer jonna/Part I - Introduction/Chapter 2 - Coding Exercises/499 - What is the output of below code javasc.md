==================== Question ====================  

### What is the output of below code

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">class</span> <span class="hljs-title class_">Vehicle</span> {
  <span class="hljs-title function_">constructor</span>(<span class="hljs-params">name</span>) {
     <span class="hljs-variable language_">this</span>.<span class="hljs-property">name</span> = name;
  }
  <span class="hljs-title function_">start</span>(<span class="hljs-params"></span>) {
     <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">`<span class="hljs-subst">${<span class="hljs-variable language_">this</span>.name}</span> vehicle started`</span>);
  }
}
<span class="hljs-keyword">class</span> <span class="hljs-title class_">Car</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">Vehicle</span> {
  <span class="hljs-title function_">start</span>(<span class="hljs-params"></span>) {
     <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">`<span class="hljs-subst">${<span class="hljs-variable language_">this</span>.name}</span> car started`</span>);
     <span class="hljs-variable language_">super</span>.<span class="hljs-title function_">start</span>();
  }
}
<span class="hljs-keyword">const</span> car = <span class="hljs-keyword">new</span> <span class="hljs-title class_">Car</span>(<span class="hljs-string">'BMW'</span>);
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(car.<span class="hljs-title function_">start</span>());
</code></pre>
<!-- codeblock-end -->

- 1: SyntaxError

- 2: BMW vehicle started, BMW car started

- 3: BMW car started, BMW vehicle started

- 4: BMW car started, BMW car started  

==================== Answer ====================  

Answer: 3

The super keyword is used to call methods of a superclass. Unlike other languages the super invocation doesn't need to be a first statement. i.e, The statements will be executed in the same order of code.

==================== Id ====================  
499

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#499-What-is-the-output-of-below-code-javasc

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
