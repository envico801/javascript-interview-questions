==================== Question ====================  

### What is the output of below code

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">class</span> <span class="hljs-title class_">A</span> {
  <span class="hljs-title function_">constructor</span>(<span class="hljs-params"></span>) {
     <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-keyword">new</span>.<span class="hljs-property">target</span>.<span class="hljs-property">name</span>);
  }
}
<span class="hljs-keyword">class</span> <span class="hljs-title class_">B</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">A</span> {
  <span class="hljs-title function_">constructor</span>(<span class="hljs-params"></span>) {
     <span class="hljs-variable language_">super</span>();
  }
}
<span class="hljs-keyword">new</span> <span class="hljs-title function_">A</span>();
<span class="hljs-keyword">new</span> <span class="hljs-title function_">B</span>();
</code></pre>
<!-- codeblock-end -->

- 1: A, A

- 2: A, B  

==================== Answer ====================  

Answer: 2

Using constructors, `new.target` refers to the constructor (points to the class definition of class which is initialized) that was directly invoked by new. This also applies to the case if the constructor is in a parent class and was delegated from a child constructor.

==================== Id ====================  
482

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#482-What-is-the-output-of-below-code-javasc

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
