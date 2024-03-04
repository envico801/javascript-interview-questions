==================== Question ====================  

### What is the output of below code?

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> user = {
  <span class="hljs-attr">name</span>: <span class="hljs-string">'John'</span>,
  <span class="hljs-title function_">eat</span>(<span class="hljs-params"></span>) {
     <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-variable language_">this</span>);
     <span class="hljs-keyword">var</span> eatFruit = <span class="hljs-keyword">function</span> (<span class="hljs-params"></span>) {
       <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-variable language_">this</span>);
     };
     <span class="hljs-title function_">eatFruit</span>();
  },
};
user.<span class="hljs-title function_">eat</span>();
</code></pre>
<!-- codeblock-end -->

- 1: {name: "John", eat: f}, {name: "John", eat: f}

- 2: Window {...}, Window {...}

- 3: {name: "John", eat: f}, undefined

- 4: {name: "John", eat: f}, Window {...}  

==================== Answer ====================  

Answer: 4

`this` keyword is dynamic scoped but not lexically scoped . In other words, it doesn't matter where `this` has been written but how it has been invoked really matter. In the above code snippet, the `user` object invokes `eat` function so `this` keyword refers to `user` object but `eatFruit` has been invoked by `eat` function and `this` will have default `Window` object.

The above pit fall fixed by three ways,

1. In ES6, the arrow function will make `this` keyword as lexically scoped. Since the surrounding object of `this` object is `user` object, the `eatFruit` function will contain `user` object for `this` object.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> user = {
  <span class="hljs-attr">name</span>: <span class="hljs-string">'John'</span>,
  <span class="hljs-title function_">eat</span>(<span class="hljs-params"></span>) {
     <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-variable language_">this</span>);
     <span class="hljs-keyword">var</span> <span class="hljs-title function_">eatFruit</span> = (<span class="hljs-params"></span>) => {
       <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-variable language_">this</span>);
     };
     <span class="hljs-title function_">eatFruit</span>();
  },
};
user.<span class="hljs-title function_">eat</span>();
</code></pre>
<!-- codeblock-end -->

The next two solutions have been used before ES6 introduced.

2.  It is possible create a reference of `this` into a separate variable and use that new variable inplace of `this` keyword inside `eatFruit` function. This is a common practice in jQuery and AngularJS before ES6 introduced.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> user = {
  <span class="hljs-attr">name</span>: <span class="hljs-string">'John'</span>,
  <span class="hljs-title function_">eat</span>(<span class="hljs-params"></span>) {
     <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-variable language_">this</span>);
     <span class="hljs-keyword">var</span> self = <span class="hljs-variable language_">this</span>;
     <span class="hljs-keyword">var</span> <span class="hljs-title function_">eatFruit</span> = (<span class="hljs-params"></span>) => {
       <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(self);
     };
     <span class="hljs-title function_">eatFruit</span>();
  },
};
user.<span class="hljs-title function_">eat</span>();
</code></pre>
<!-- codeblock-end -->

3. The `eatFruit` function can bind explicitly with `this` keyword where it refers `Window` object.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> user = {
  <span class="hljs-attr">name</span>: <span class="hljs-string">'John'</span>,
  <span class="hljs-title function_">eat</span>(<span class="hljs-params"></span>) {
     <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-variable language_">this</span>);
     <span class="hljs-keyword">var</span> eatFruit = <span class="hljs-keyword">function</span> (<span class="hljs-params"></span>) {
       <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-variable language_">this</span>);
     };
     <span class="hljs-keyword">return</span> eatFruit.<span class="hljs-title function_">bind</span>(<span class="hljs-variable language_">this</span>);
  },
};
user.<span class="hljs-title function_">eat</span>()();
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
520

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#520-What-is-the-output-of-below-code-javas

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
