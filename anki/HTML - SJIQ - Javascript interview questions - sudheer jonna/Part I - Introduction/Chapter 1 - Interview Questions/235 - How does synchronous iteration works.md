==================== Question ====================  

### How does synchronous iteration works  

==================== Answer ====================  

Synchronous iteration was introduced in ES6 and it works with below set of components,

**Iterable:** It is an object which can be iterated over via a method whose key is Symbol.iterator.

**Iterator:** It is an object returned by invoking `[Symbol.iterator]()` on an iterable. This iterator object wraps each iterated element in an object and returns it via `next()` method one by one.

**IteratorResult:** It is an object returned by `next()` method. The object contains two properties; the `value` property contains an iterated element and the `done` property determines whether the element is the last element or not.

Let's demonstrate synchronous iteration with an array as below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> iterable = [<span class="hljs-string">'one'</span>, <span class="hljs-string">'two'</span>, <span class="hljs-string">'three'</span>];
<span class="hljs-keyword">const</span> iterator = iterable[<span class="hljs-title class_">Symbol</span>.<span class="hljs-property">iterator</span>]();
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(iterator.<span class="hljs-title function_">next</span>()); <span class="hljs-comment">// { value: 'one', done: false }</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(iterator.<span class="hljs-title function_">next</span>()); <span class="hljs-comment">// { value: 'two', done: false }</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(iterator.<span class="hljs-title function_">next</span>()); <span class="hljs-comment">// { value: 'three', done: false }</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(iterator.<span class="hljs-title function_">next</span>()); <span class="hljs-comment">// { value: 'undefined, done: true }</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
235

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#235-How-does-synchronous-iteration-works

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
