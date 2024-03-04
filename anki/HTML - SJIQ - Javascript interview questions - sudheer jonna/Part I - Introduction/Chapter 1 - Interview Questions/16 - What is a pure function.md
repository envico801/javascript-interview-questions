==================== Question ====================  

### What is a pure function  

==================== Answer ====================  

A **Pure function** is a function where the return value is only determined by its arguments without any side effects. i.e, If you call a function with the same arguments 'n' number of times and 'n' number of places in the application then it will always return the same value.

Let's take an example to see the difference between pure and impure functions,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-comment">//Impure</span>
<span class="hljs-keyword">let</span> numberArray = [];
<span class="hljs-keyword">const</span> <span class="hljs-title function_">impureAddNumber</span> = (<span class="hljs-params">number</span>) => numberArray.<span class="hljs-title function_">push</span>(number);
<span class="hljs-comment">//Pure</span>
<span class="hljs-keyword">const</span> <span class="hljs-title function_">pureAddNumber</span> = (<span class="hljs-params">number</span>) => <span class="hljs-function">(<span class="hljs-params">argNumberArray</span>) =></span> argNumberArray.<span class="hljs-title function_">concat</span>([number]);
<span class="hljs-comment">//Display the results</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-title function_">impureAddNumber</span>(<span class="hljs-number">6</span>)); <span class="hljs-comment">// returns 1</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(numberArray); <span class="hljs-comment">// returns [6]</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-title function_">pureAddNumber</span>(<span class="hljs-number">7</span>)(numberArray)); <span class="hljs-comment">// returns [6, 7]</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(numberArray); <span class="hljs-comment">// returns [6]</span>
</code></pre>
<!-- codeblock-end -->

As per the above code snippets, the **Push** function is impure itself by altering the array and returning a push number index independent of the parameter value, whereas **Concat** on the other hand takes the array and concatenates it with the other array producing a whole new array without side effects. Also, the return value is a concatenation of the previous array.

Remember that Pure functions are important as they simplify unit testing without any side effects and no need for dependency injection. They also avoid tight coupling and make it harder to break your application by not having any side effects. These principles are coming together with the **Immutability** concept of ES6: giving preference to **const** over **let** usage.

==================== Id ====================  
16

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#16-What-is-a-pure-function

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
