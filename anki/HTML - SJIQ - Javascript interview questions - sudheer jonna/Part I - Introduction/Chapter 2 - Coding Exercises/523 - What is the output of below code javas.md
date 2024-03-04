==================== Question ====================  

### What is the output of below code?

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">greeting</span>(<span class="hljs-params"></span>) {
  <span class="hljs-built_in">setTimeout</span>(<span class="hljs-keyword">function</span> (<span class="hljs-params"></span>) {
     <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(message);
  }, <span class="hljs-number">5000</span>);
  <span class="hljs-keyword">const</span> message = <span class="hljs-string">'Hello, Good morning'</span>;
}
<span class="hljs-title function_">greeting</span>();
</code></pre>
<!-- codeblock-end -->

- 1: Undefined

- 2: Reference error:

- 3: Hello, Good morning

- 4: null  

==================== Answer ====================  

Answer: 3

The variable `message` is still treated as closure(since it has been used in inner function) eventhough it has been declared after setTimeout function. The function with in setTimeout function will be sent to WebAPI and the variable declaration executed with in 5 seconds with the assigned value. Hence, the text declared for the variable will be displayed.

==================== Id ====================  
523

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#523-What-is-the-output-of-below-code-javas

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
