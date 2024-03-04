==================== Question ====================  

### What is debouncing?  

==================== Answer ====================  

Debouncing is a programming pattern that allows delaying execution of some piece of code until a specified time to avoid unnecessary _CPU cycles, API calls and improve performance_. The debounce function make sure that your code is only triggered once per user input. The common usecases are Search box suggestions, text-field auto-saves, and eliminating double-button clicks.

Let's say you want to show suggestions for a search query, but only after a visitor has finished typing it. So here you write a debounce function where the user keeps writing the characters with in 500ms then previous timer cleared out using `clearTimeout` and reschedule API call/DB query for a new time—300 ms in the future.

<!-- codeblock-start -->
<pre><code class="hljs language-js"><span class="hljs-keyword">function</span> <span class="hljs-title function_">debounce</span>(<span class="hljs-params">func, timeout = <span class="hljs-number">500</span></span>) {
  <span class="hljs-keyword">let</span> timer;
  <span class="hljs-keyword">return</span> <span class="hljs-function">(<span class="hljs-params">...args</span>) =></span> {
     <span class="hljs-built_in">clearTimeout</span>(timer);
     timer = <span class="hljs-built_in">setTimeout</span>(<span class="hljs-function">() =></span> {
       func.<span class="hljs-title function_">apply</span>(<span class="hljs-variable language_">this</span>, args);
     }, timeout);
  };
}
<span class="hljs-keyword">function</span> <span class="hljs-title function_">fetchResults</span>(<span class="hljs-params"></span>) {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'Fetching input suggestions'</span>);
}
<span class="hljs-keyword">const</span> processChange = <span class="hljs-title function_">debounce</span>(<span class="hljs-function">() =></span> <span class="hljs-title function_">fetchResults</span>());
</code></pre>
<!-- codeblock-end -->

The _debounce()_ function can be used on input, button and window events

**Input:**

<!-- codeblock-start -->
<pre><code class="hljs language-html"><span class="hljs-tag">&#x3C;<span class="hljs-name">input</span> <span class="hljs-attr">type</span>=<span class="hljs-string">"text"</span> <span class="hljs-attr">onkeyup</span>=<span class="hljs-string">"processChange()"</span> /></span>
</code></pre>
<!-- codeblock-end -->

**Button:**

<!-- codeblock-start -->
<pre><code class="hljs language-html"><span class="hljs-tag">&#x3C;<span class="hljs-name">button</span> <span class="hljs-attr">onclick</span>=<span class="hljs-string">"processChange()"</span>></span>Click me<span class="hljs-tag">&#x3C;/<span class="hljs-name">button</span>></span>
</code></pre>
<!-- codeblock-end -->

**Windows event:**

<!-- codeblock-start -->
<pre><code class="hljs language-html">window.addEventListener("scroll", processChange);
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
434

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#434-What-is-debouncing

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
