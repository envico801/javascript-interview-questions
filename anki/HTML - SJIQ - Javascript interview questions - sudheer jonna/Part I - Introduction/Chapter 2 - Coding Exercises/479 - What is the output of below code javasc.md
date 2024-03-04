==================== Question ====================  

### What is the output of below code

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> sym1 = <span class="hljs-keyword">new</span> <span class="hljs-title class_">Symbol</span>(<span class="hljs-string">'one'</span>);
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(sym1);
</code></pre>
<!-- codeblock-end -->

- 1: SyntaxError

- 2: one

- 3: Symbol('one')

- 4: Symbol  

==================== Answer ====================  

Answer: 1

`Symbol` is a just a standard function and not an object constructor(unlike other primitives new Boolean, new String and new Number). So if you try to call it with the new operator will result in a TypeError

==================== Id ====================  
479

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#479-What-is-the-output-of-below-code-javasc

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
