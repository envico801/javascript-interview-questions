==================== Question ====================  

### What is the output of below code?

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> <span class="hljs-keyword">of</span> = [<span class="hljs-string">'of'</span>];
<span class="hljs-keyword">for</span> (<span class="hljs-keyword">var</span> <span class="hljs-keyword">of</span> <span class="hljs-keyword">of</span> <span class="hljs-keyword">of</span>) {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-keyword">of</span>);
}
</code></pre>
<!-- codeblock-end -->

- 1: of

- 2: SyntaxError: Unexpected token of

- 3: SyntaxError: Identifier 'of' has already been declared

- 4: ReferenceError: of is not defined  

==================== Answer ====================  

Answer: 1

In JavaScript, `of` is not considered as a reserved keyword. So the variable declaration with `of` is accepted and prints the array value `of` using for..of loop.

But if you use reserved keyword such as `in` then there will be a syntax error saying `SyntaxError: Unexpected token in`,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> <span class="hljs-keyword">in</span> = [<span class="hljs-string">'in'</span>];
<span class="hljs-keyword">for</span>(<span class="hljs-keyword">var</span> <span class="hljs-keyword">in</span> <span class="hljs-keyword">in</span> <span class="hljs-keyword">in</span>) {
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-keyword">in</span>[<span class="hljs-keyword">in</span>]);
}
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
512

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#512-What-is-the-output-of-below-code-javas

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
