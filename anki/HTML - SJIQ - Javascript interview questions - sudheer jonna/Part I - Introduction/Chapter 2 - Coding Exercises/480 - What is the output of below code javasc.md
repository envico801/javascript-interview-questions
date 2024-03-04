==================== Question ====================  

### What is the output of below code

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">let</span> myNumber = <span class="hljs-number">100</span>;
<span class="hljs-keyword">let</span> myString = <span class="hljs-string">'100'</span>;
<span class="hljs-keyword">if</span> (!<span class="hljs-keyword">typeof</span> myNumber === <span class="hljs-string">'string'</span>) {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'It is not a string!'</span>);
} <span class="hljs-keyword">else</span> {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'It is a string!'</span>);
}
<span class="hljs-keyword">if</span> (!<span class="hljs-keyword">typeof</span> myString === <span class="hljs-string">'number'</span>) {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'It is not a number!'</span>);
} <span class="hljs-keyword">else</span> {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'It is a number!'</span>);
}
</code></pre>
<!-- codeblock-end -->

- 1: SyntaxError

- 2: It is not a string!, It is not a number!

- 3: It is not a string!, It is a number!

- 4: It is a string!, It is a number!  

==================== Answer ====================  

Answer: 4

The return value of `typeof myNumber` or `typeof myString` is always a truthy value (either "number" or "string"). The ! operator operates on either `typeof myNumber` or `typeof myString`, converting them to boolean values. Since the value of both `!typeof myNumber` and `!typeof myString` is false, the if condition fails, and control goes to else block.

To make the ! operator operate on the equality expression, one needs to add parentheses:

<!-- codeblock-start -->
<pre><code>if (!(typeof myNumber === "string"))
</code></pre>
<!-- codeblock-end -->

Or simply use the inequality operator:

<!-- codeblock-start -->
<pre><code>if (typeof myNumber !== "string")
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
480

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#480-What-is-the-output-of-below-code-javasc

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
