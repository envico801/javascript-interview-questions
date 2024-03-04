==================== Question ====================  

### What is the output of below code

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span>* <span class="hljs-title function_">myGenFunc</span>(<span class="hljs-params"></span>) {
  <span class="hljs-keyword">yield</span> <span class="hljs-number">1</span>;
  <span class="hljs-keyword">yield</span> <span class="hljs-number">2</span>;
  <span class="hljs-keyword">yield</span> <span class="hljs-number">3</span>;
}
<span class="hljs-keyword">var</span> myGenObj = <span class="hljs-keyword">new</span> <span class="hljs-title function_">myGenFunc</span>();
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(myGenObj.<span class="hljs-title function_">next</span>().<span class="hljs-property">value</span>);
</code></pre>
<!-- codeblock-end -->

- 1: 1

- 2: undefined

- 3: SyntaxError

- 4: TypeError  

==================== Answer ====================  

Answer: 4

Generators are not constructible type. But if you still proceed to do, there will be an error saying "TypeError: myGenFunc is not a constructor"

==================== Id ====================  
493

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#493-What-is-the-output-of-below-code-javasc

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
