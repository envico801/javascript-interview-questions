==================== Question ====================  

### What is the output of below code?

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">let</span> a = <span class="hljs-number">10</span>;
<span class="hljs-keyword">if</span> (<span class="hljs-literal">true</span>) {
  <span class="hljs-keyword">let</span> a = <span class="hljs-number">20</span>;
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(a, <span class="hljs-string">'inside'</span>);
}
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(a, <span class="hljs-string">'outside'</span>);
</code></pre>
<!-- codeblock-end -->

- 1: 20, "inside" and 20, "outside"

- 2: 20, "inside" and 10, "outside"

- 3: 10, "inside" and 10, "outside"

- 4: 10, "inside" and 20, "outside"  

==================== Answer ====================  

Answer: 2

The variable "a" declared inside "if" has block scope and does not affect the value of the outer "a" variable.

==================== Id ====================  
528

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#528-What-is-the-output-of-below-code-javas

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
