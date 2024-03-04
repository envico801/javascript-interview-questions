==================== Question ====================  

### What is the purpose of compareFunction while sorting arrays  

==================== Answer ====================  

The compareFunction is used to define the sort order. If omitted, the array elements are converted to strings, then sorted according to each character's Unicode code point value. Let's take an example to see the usage of compareFunction,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">let</span> numbers = [<span class="hljs-number">1</span>, <span class="hljs-number">2</span>, <span class="hljs-number">5</span>, <span class="hljs-number">3</span>, <span class="hljs-number">4</span>];
numbers.<span class="hljs-title function_">sort</span>(<span class="hljs-function">(<span class="hljs-params">a, b</span>) =></span> b - a);
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(numbers); <span class="hljs-comment">// [5, 4, 3, 2, 1]</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
243

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#243-What-is-the-purpose-of-comparefunction-whi

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
