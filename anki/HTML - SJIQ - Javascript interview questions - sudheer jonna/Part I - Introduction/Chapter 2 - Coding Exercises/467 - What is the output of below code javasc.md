==================== Question ====================  

### What is the output of below code

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>([<span class="hljs-number">0</span>] == <span class="hljs-literal">false</span>);
<span class="hljs-keyword">if</span> ([<span class="hljs-number">0</span>]) {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">"I'm True"</span>);
} <span class="hljs-keyword">else</span> {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">"I'm False"</span>);
}
</code></pre>
<!-- codeblock-end -->

- 1: True, I'm True

- 2: True, I'm False

- 3: False, I'm True

- 4: False, I'm False  

==================== Answer ====================  

Answer: 1

In comparison operators, the expression `[0]` converted to Number([0].valueOf().toString()) which is resolved to false. Whereas `[0]` just becomes a truthy value without any conversion because there is no comparison operator.

==================== Id ====================  
467

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#467-What-is-the-output-of-below-code-javasc

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
