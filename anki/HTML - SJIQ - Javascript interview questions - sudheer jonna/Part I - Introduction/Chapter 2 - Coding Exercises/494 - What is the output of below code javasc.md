==================== Question ====================  

### What is the output of below code

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span>* <span class="hljs-title function_">yieldAndReturn</span>(<span class="hljs-params"></span>) {
  <span class="hljs-keyword">yield</span> <span class="hljs-number">1</span>;
  <span class="hljs-keyword">return</span> <span class="hljs-number">2</span>;
  <span class="hljs-keyword">yield</span> <span class="hljs-number">3</span>;
}
<span class="hljs-keyword">var</span> myGenObj = <span class="hljs-title function_">yieldAndReturn</span>();
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(myGenObj.<span class="hljs-title function_">next</span>());
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(myGenObj.<span class="hljs-title function_">next</span>());
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(myGenObj.<span class="hljs-title function_">next</span>());
</code></pre>
<!-- codeblock-end -->

- 1: { value: 1, done: false }, { value: 2, done: true }, { value: undefined, done: true }

- 2: { value: 1, done: false }, { value: 2, done: false }, { value: undefined, done: true }

- 3: { value: 1, done: false }, { value: 2, done: true }, { value: 3, done: true }

- 4: { value: 1, done: false }, { value: 2, done: false }, { value: 3, done: true }  

==================== Answer ====================  

Answer: 1

A return statement in a generator function will make the generator finish. If a value is returned, it will be set as the value property of the object and done property to true. When a generator is finished, subsequent next() calls return an object of this form: `{value: undefined, done: true}`.

==================== Id ====================  
494

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#494-What-is-the-output-of-below-code-javasc

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
