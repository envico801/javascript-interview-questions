==================== Question ====================  

### What is the output of below code?

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> currentCity = <span class="hljs-string">'NewYork'</span>;
<span class="hljs-keyword">var</span> changeCurrentCity = <span class="hljs-keyword">function</span> (<span class="hljs-params"></span>) {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'Current City:'</span>, currentCity);
  <span class="hljs-keyword">var</span> currentCity = <span class="hljs-string">'Singapore'</span>;
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'Current City:'</span>, currentCity);
};
<span class="hljs-title function_">changeCurrentCity</span>();
</code></pre>
<!-- codeblock-end -->

- 1: NewYork, Singapore

- 2: NewYork, NewYork

- 3: undefined, Singapore

- 4: Singapore, Singapore  

==================== Answer ====================  

Answer: 3

Due to hositing feature, the variables declared with `var` will have `undefined` value in the creation phase so the outer variable `currentCity` will get same `undefined` value. But after few lines of code JavaScript engine found a new function call(`changeCurrentCity()`) to update the current city with `var` re-declaration. Since each function call will create a new execution context, the same variable will have `undefined` value before the declaration and new value(`Singapore`) after the declarion. Hence, the value `undefined` print first followed by new value `Singapore` in the execution phase.

==================== Id ====================  
517

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#517-What-is-the-output-of-below-code-javas

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
