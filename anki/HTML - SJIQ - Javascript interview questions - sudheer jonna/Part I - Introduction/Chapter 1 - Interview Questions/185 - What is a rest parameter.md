==================== Question ====================  

### What is a rest parameter  

==================== Answer ====================  

Rest parameter is an improved way to handle function parameters which allows us to represent an indefinite number of arguments as an array. The syntax would be as below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">f</span>(<span class="hljs-params">a, b, ...theArgs</span>) {
  <span class="hljs-comment">// ...</span>
}
</code></pre>
<!-- codeblock-end -->

For example, let's take a sum example to calculate on dynamic number of parameters,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">sum</span>(<span class="hljs-params">...args</span>) {
  <span class="hljs-keyword">let</span> total = <span class="hljs-number">0</span>;
  <span class="hljs-keyword">for</span> (<span class="hljs-keyword">const</span> i <span class="hljs-keyword">of</span> args) {
     total += i;
  }
  <span class="hljs-keyword">return</span> total;
}
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-title function_">sum</span>(<span class="hljs-number">1</span>, <span class="hljs-number">2</span>)); <span class="hljs-comment">//3</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-title function_">sum</span>(<span class="hljs-number">1</span>, <span class="hljs-number">2</span>, <span class="hljs-number">3</span>)); <span class="hljs-comment">//6</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-title function_">sum</span>(<span class="hljs-number">1</span>, <span class="hljs-number">2</span>, <span class="hljs-number">3</span>, <span class="hljs-number">4</span>)); <span class="hljs-comment">//13</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-title function_">sum</span>(<span class="hljs-number">1</span>, <span class="hljs-number">2</span>, <span class="hljs-number">3</span>, <span class="hljs-number">4</span>, <span class="hljs-number">5</span>)); <span class="hljs-comment">//15</span>
</code></pre>
<!-- codeblock-end -->

**Note:** Rest parameter is added in ES2015 or ES6

==================== Id ====================  
185

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#185-What-is-a-rest-parameter

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
