==================== Question ====================  

### What is Hoisting  

==================== Answer ====================  

Hoisting is a JavaScript mechanism where variables, function declarations and classes are moved to the top of their scope before code execution. Remember that JavaScript only hoists declarations, not initialisation.

Let's take a simple example of variable hoisting,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(message); <span class="hljs-comment">//output : undefined</span>
<span class="hljs-keyword">var</span> message = <span class="hljs-string">'The variable Has been hoisted'</span>;
</code></pre>
<!-- codeblock-end -->

The above code looks like as below to the interpreter,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> message;
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(message);
message = <span class="hljs-string">'The variable Has been hoisted'</span>;
</code></pre>
<!-- codeblock-end -->

In the same fashion, function declarations are hoisted too

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-title function_">message</span>(<span class="hljs-string">'Good morning'</span>); <span class="hljs-comment">//Good morning</span>
<span class="hljs-keyword">function</span> <span class="hljs-title function_">message</span>(<span class="hljs-params">name</span>) {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(name);
}
</code></pre>
<!-- codeblock-end -->

This hoisting makes functions to be safely used in code before they are declared.

==================== Id ====================  
25

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#25-What-is-hoisting

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
