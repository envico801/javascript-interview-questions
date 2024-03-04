==================== Question ====================  

### What is the currying function  

==================== Answer ====================  

Currying is the process of taking a function with multiple arguments and turning it into a sequence of functions each with only a single argument. Currying is named after a mathematician **Haskell Curry**. By applying currying, an n-ary function turns into a unary function.

Let's take an example of n-ary function and how it turns into a currying function,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> <span class="hljs-title function_">multiArgFunction</span> = (<span class="hljs-params">a, b, c</span>) => a + b + c;
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-title function_">multiArgFunction</span>(<span class="hljs-number">1</span>, <span class="hljs-number">2</span>, <span class="hljs-number">3</span>)); <span class="hljs-comment">// 6</span>
<span class="hljs-keyword">const</span> <span class="hljs-title function_">curryUnaryFunction</span> = (<span class="hljs-params">a</span>) => <span class="hljs-function">(<span class="hljs-params">b</span>) =></span> <span class="hljs-function">(<span class="hljs-params">c</span>) =></span> a + b + c;
<span class="hljs-title function_">curryUnaryFunction</span>(<span class="hljs-number">1</span>); <span class="hljs-comment">// returns a function: b => c =>  1 + b + c</span>
<span class="hljs-title function_">curryUnaryFunction</span>(<span class="hljs-number">1</span>)(<span class="hljs-number">2</span>); <span class="hljs-comment">// returns a function: c => 3 + c</span>
<span class="hljs-title function_">curryUnaryFunction</span>(<span class="hljs-number">1</span>)(<span class="hljs-number">2</span>)(<span class="hljs-number">3</span>); <span class="hljs-comment">// returns the number 6</span>
</code></pre>
<!-- codeblock-end -->

Curried functions are great to improve **code reusability** and **functional composition**.

==================== Id ====================  
15

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#15-What-is-the-currying-function

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
