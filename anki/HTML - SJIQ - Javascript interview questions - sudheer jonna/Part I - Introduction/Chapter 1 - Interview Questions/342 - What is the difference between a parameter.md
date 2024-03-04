==================== Question ====================  

### What is the difference between a parameter and an argument  

==================== Answer ====================  

Parameter is the variable name of a function definition whereas an argument represents the value given to a function when it is invoked. Let's explain this with a simple function

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">myFunction</span>(<span class="hljs-params">parameter1, parameter2, parameter3</span>) {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-variable language_">arguments</span>[<span class="hljs-number">0</span>]); <span class="hljs-comment">// "argument1"</span>
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-variable language_">arguments</span>[<span class="hljs-number">1</span>]); <span class="hljs-comment">// "argument2"</span>
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-variable language_">arguments</span>[<span class="hljs-number">2</span>]); <span class="hljs-comment">// "argument3"</span>
}
<span class="hljs-title function_">myFunction</span>(<span class="hljs-string">'argument1'</span>, <span class="hljs-string">'argument2'</span>, <span class="hljs-string">'argument3'</span>);
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
342

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#342-What-is-the-difference-between-a-parameter

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
