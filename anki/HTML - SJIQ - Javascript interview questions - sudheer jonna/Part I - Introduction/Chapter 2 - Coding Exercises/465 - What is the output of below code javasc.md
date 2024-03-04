==================== Question ====================  

### What is the output of below code

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-number">10</span> == [<span class="hljs-number">10</span>]);
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-number">10</span> == [[[[[[[<span class="hljs-number">10</span>]]]]]]]);
</code></pre>
<!-- codeblock-end -->

- 1: True, True

- 2: True, False

- 3: False, False

- 4: False, True  

==================== Answer ====================  

Answer: 1

As per the comparison algorithm in the ECMAScript specification(ECMA-262), the above expression converted into JS as below

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-number">10</span> === <span class="hljs-title class_">Number</span>([<span class="hljs-number">10</span>].<span class="hljs-title function_">valueOf</span>().<span class="hljs-title function_">toString</span>()); <span class="hljs-comment">// 10</span>
</code></pre>
<!-- codeblock-end -->

So it doesn't matter about number brackets([]) around the number, it is always converted to a number in the expression.

==================== Id ====================  
465

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#465-What-is-the-output-of-below-code-javasc

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
