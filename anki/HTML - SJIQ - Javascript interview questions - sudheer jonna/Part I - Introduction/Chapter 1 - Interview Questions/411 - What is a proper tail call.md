==================== Question ====================  

### What is a Proper Tail Call  

==================== Answer ====================  

First, we should know about tail call before talking about "Proper Tail Call". A tail call is a subroutine or function call performed as the final action of a calling function. Whereas **Proper tail call(PTC)** is a technique where the program or code will not create additional stack frames for a recursion when the function call is a tail call.

For example, the below classic or head recursion of factorial function relies on stack for each step. Each step need to be processed upto `n * factorial(n - 1)`

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">factorial</span>(<span class="hljs-params">n</span>) {
  <span class="hljs-keyword">if</span> (n === <span class="hljs-number">0</span>) {
     <span class="hljs-keyword">return</span> <span class="hljs-number">1</span>;
  }
  <span class="hljs-keyword">return</span> n * <span class="hljs-title function_">factorial</span>(n - <span class="hljs-number">1</span>);
}
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-title function_">factorial</span>(<span class="hljs-number">5</span>)); <span class="hljs-comment">//120</span>
</code></pre>
<!-- codeblock-end -->

But if you use Tail recursion functions, they keep passing all the necessary data it needs down the recursion without relying on the stack.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">factorial</span>(<span class="hljs-params">n, acc = <span class="hljs-number">1</span></span>) {
  <span class="hljs-keyword">if</span> (n === <span class="hljs-number">0</span>) {
     <span class="hljs-keyword">return</span> acc;
  }
  <span class="hljs-keyword">return</span> <span class="hljs-title function_">factorial</span>(n - <span class="hljs-number">1</span>, n * acc);
}
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-title function_">factorial</span>(<span class="hljs-number">5</span>)); <span class="hljs-comment">//120</span>
</code></pre>
<!-- codeblock-end -->

The above pattern returns the same output as the first one. But the accumulator keeps track of total as an argument without using stack memory on recursive calls.

==================== Id ====================  
411

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#411-What-is-a-proper-tail-call

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
