==================== Question ====================  

### What is the output of below code

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> squareObj = <span class="hljs-keyword">new</span> <span class="hljs-title class_">Square</span>(<span class="hljs-number">10</span>);
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(squareObj.<span class="hljs-property">area</span>);
<span class="hljs-keyword">class</span> <span class="hljs-title class_">Square</span> {
  <span class="hljs-title function_">constructor</span>(<span class="hljs-params">length</span>) {
     <span class="hljs-variable language_">this</span>.<span class="hljs-property">length</span> = length;
  }
  <span class="hljs-keyword">get</span> <span class="hljs-title function_">area</span>() {
     <span class="hljs-keyword">return</span> <span class="hljs-variable language_">this</span>.<span class="hljs-property">length</span> * <span class="hljs-variable language_">this</span>.<span class="hljs-property">length</span>;
  }
  <span class="hljs-keyword">set</span> <span class="hljs-title function_">area</span>(<span class="hljs-params">value</span>) {
     <span class="hljs-variable language_">this</span>.<span class="hljs-property">area</span> = value;
  }
}
</code></pre>
<!-- codeblock-end -->

- 1: 100

- 2: ReferenceError  

==================== Answer ====================  

Answer: 2

Unlike function declarations, class declarations are not hoisted. i.e, First You need to declare your class and then access it, otherwise it will throw a ReferenceError "Uncaught ReferenceError: Square is not defined".

**Note:** Class expressions also applies to the same hoisting restrictions of class declarations.

==================== Id ====================  
497

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#497-What-is-the-output-of-below-code-javasc

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
