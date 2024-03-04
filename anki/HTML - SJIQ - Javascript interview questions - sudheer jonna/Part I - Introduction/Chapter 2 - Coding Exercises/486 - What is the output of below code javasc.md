==================== Question ====================  

### What is the output of below code

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> props = [
  { <span class="hljs-attr">id</span>: <span class="hljs-number">1</span>, <span class="hljs-attr">name</span>: <span class="hljs-string">'John'</span> },
  { <span class="hljs-attr">id</span>: <span class="hljs-number">2</span>, <span class="hljs-attr">name</span>: <span class="hljs-string">'Jack'</span> },
  { <span class="hljs-attr">id</span>: <span class="hljs-number">3</span>, <span class="hljs-attr">name</span>: <span class="hljs-string">'Tom'</span> },
];
<span class="hljs-keyword">const</span> [, , { name }] = props;
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(name);
</code></pre>
<!-- codeblock-end -->

- 1: Tom

- 2: Error

- 3: undefined

- 4: John  

==================== Answer ====================  

Answer: 1

It is possible to combine Array and Object destructuring. In this case, the third element in the array props accessed first followed by name property in the object.

==================== Id ====================  
486

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#486-What-is-the-output-of-below-code-javasc

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
