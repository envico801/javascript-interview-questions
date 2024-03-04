==================== Question ====================  

### What is the output of below code

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">let</span> numbers = [<span class="hljs-number">1</span>, <span class="hljs-number">2</span>, <span class="hljs-number">3</span>, <span class="hljs-number">4</span>, <span class="hljs-title class_">NaN</span>];
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(numbers.<span class="hljs-title function_">indexOf</span>(<span class="hljs-title class_">NaN</span>));
</code></pre>
<!-- codeblock-end -->

- 1: 4

- 2: NaN

- 3: SyntaxError

- 4: -1  

==================== Answer ====================  

Answer: 4

The `indexOf` uses strict equality operator(===) internally and `NaN === NaN` evaluates to false. Since indexOf won't be able to find NaN inside an array, it returns -1 always.

But you can use `Array.prototype.findIndex` method to find out the index of NaN in an array or You can use `Array.prototype.includes` to check if NaN is present in an array or not.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">let</span> numbers = [<span class="hljs-number">1</span>, <span class="hljs-number">2</span>, <span class="hljs-number">3</span>, <span class="hljs-number">4</span>, <span class="hljs-title class_">NaN</span>];
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(numbers.<span class="hljs-title function_">findIndex</span>(<span class="hljs-title class_">Number</span>.<span class="hljs-property">isNaN</span>)); <span class="hljs-comment">// 4</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(numbers.<span class="hljs-title function_">includes</span>(<span class="hljs-title class_">NaN</span>)); <span class="hljs-comment">// true</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
471

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#471-What-is-the-output-of-below-code-javasc

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
