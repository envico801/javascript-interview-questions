==================== Question ====================  

### How do you make an object iterable in javascript  

==================== Answer ====================  

By default, plain objects are not iterable. But you can make the object iterable by defining a `Symbol.iterator` property on it.

Let's demonstrate this with an example,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> collection = {
  <span class="hljs-attr">one</span>: <span class="hljs-number">1</span>,
  <span class="hljs-attr">two</span>: <span class="hljs-number">2</span>,
  <span class="hljs-attr">three</span>: <span class="hljs-number">3</span>,
  [<span class="hljs-title class_">Symbol</span>.<span class="hljs-property">iterator</span>]() {
     <span class="hljs-keyword">const</span> values = <span class="hljs-title class_">Object</span>.<span class="hljs-title function_">keys</span>(<span class="hljs-variable language_">this</span>);
     <span class="hljs-keyword">let</span> i = <span class="hljs-number">0</span>;
     <span class="hljs-keyword">return</span> {
       <span class="hljs-attr">next</span>: <span class="hljs-function">() =></span> {
         <span class="hljs-keyword">return</span> {
           <span class="hljs-attr">value</span>: <span class="hljs-variable language_">this</span>[values[i++]],
           <span class="hljs-attr">done</span>: i > values.<span class="hljs-property">length</span>,
         };
       },
     };
  },
};
<span class="hljs-keyword">const</span> iterator = collection[<span class="hljs-title class_">Symbol</span>.<span class="hljs-property">iterator</span>]();
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(iterator.<span class="hljs-title function_">next</span>()); <span class="hljs-comment">// → {value: 1, done: false}</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(iterator.<span class="hljs-title function_">next</span>()); <span class="hljs-comment">// → {value: 2, done: false}</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(iterator.<span class="hljs-title function_">next</span>()); <span class="hljs-comment">// → {value: 3, done: false}</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(iterator.<span class="hljs-title function_">next</span>()); <span class="hljs-comment">// → {value: undefined, done: true}</span>
</code></pre>
<!-- codeblock-end -->

The above process can be simplified using a generator function,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> collection = {
  <span class="hljs-attr">one</span>: <span class="hljs-number">1</span>,
  <span class="hljs-attr">two</span>: <span class="hljs-number">2</span>,
  <span class="hljs-attr">three</span>: <span class="hljs-number">3</span>,
  [<span class="hljs-title class_">Symbol</span>.<span class="hljs-property">iterator</span>]: <span class="hljs-keyword">function</span>* () {
     <span class="hljs-keyword">for</span> (<span class="hljs-keyword">let</span> key <span class="hljs-keyword">in</span> <span class="hljs-variable language_">this</span>) {
       <span class="hljs-keyword">yield</span> <span class="hljs-variable language_">this</span>[key];
     }
  },
};
<span class="hljs-keyword">const</span> iterator = collection[<span class="hljs-title class_">Symbol</span>.<span class="hljs-property">iterator</span>]();
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(iterator.<span class="hljs-title function_">next</span>()); <span class="hljs-comment">// {value: 1, done: false}</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(iterator.<span class="hljs-title function_">next</span>()); <span class="hljs-comment">// {value: 2, done: false}</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(iterator.<span class="hljs-title function_">next</span>()); <span class="hljs-comment">// {value: 3, done: false}</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(iterator.<span class="hljs-title function_">next</span>()); <span class="hljs-comment">// {value: undefined, done: true}</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
410

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#410-How-do-you-make-an-object-iterable-in-java

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
