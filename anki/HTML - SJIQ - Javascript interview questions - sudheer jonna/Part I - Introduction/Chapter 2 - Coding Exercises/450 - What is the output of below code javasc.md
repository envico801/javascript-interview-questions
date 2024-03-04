==================== Question ====================  

### What is the output of below code

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> car = <span class="hljs-keyword">new</span> <span class="hljs-title class_">Vehicle</span>(<span class="hljs-string">'Honda'</span>, <span class="hljs-string">'white'</span>, <span class="hljs-string">'2010'</span>, <span class="hljs-string">'UK'</span>);
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(car);
<span class="hljs-keyword">function</span> <span class="hljs-title function_">Vehicle</span>(<span class="hljs-params">model, color, year, country</span>) {
  <span class="hljs-variable language_">this</span>.<span class="hljs-property">model</span> = model;
  <span class="hljs-variable language_">this</span>.<span class="hljs-property">color</span> = color;
  <span class="hljs-variable language_">this</span>.<span class="hljs-property">year</span> = year;
  <span class="hljs-variable language_">this</span>.<span class="hljs-property">country</span> = country;
}
</code></pre>
<!-- codeblock-end -->

- 1: Undefined

- 2: ReferenceError

- 3: null

- 4: {model: "Honda", color: "white", year: "2010", country: "UK"}  

==================== Answer ====================  

Answer: 4

The function declarations are hoisted similar to any variables. So the placement for `Vehicle` function declaration doesn't make any difference.

==================== Id ====================  
450

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#450-What-is-the-output-of-below-code-javasc

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
