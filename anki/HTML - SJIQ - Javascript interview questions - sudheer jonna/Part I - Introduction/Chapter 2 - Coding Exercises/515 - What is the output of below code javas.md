==================== Question ====================  

### What is the output of below code?

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(name);
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-title function_">message</span>());
<span class="hljs-keyword">var</span> name = <span class="hljs-string">'John'</span>;
(<span class="hljs-keyword">function</span> <span class="hljs-title function_">message</span>(<span class="hljs-params"></span>) {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'Hello John: Welcome'</span>);
});
</code></pre>
<!-- codeblock-end -->

- 1: John, Hello John: Welcome

- 2: undefined, Hello John, Welcome

- 3: Reference error: name is not defined, Reference error: message is not defined

- 4: undefined, Reference error: message is not defined  

==================== Answer ====================  

Answer: 4

IIFE(Immediately Invoked Function Expression) is just like any other function expression which won't be hoisted. Hence, there will be a reference error for message call.

The behavior would be the same with below function expression of message1,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(name);
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-title function_">message</span>());
<span class="hljs-keyword">var</span> name = <span class="hljs-string">'John'</span>;
<span class="hljs-keyword">var</span> message = <span class="hljs-keyword">function</span> (<span class="hljs-params"></span>) {
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'Hello John: Welcome'</span>);
});
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
515

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#515-What-is-the-output-of-below-code-javas

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
