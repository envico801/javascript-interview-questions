==================== Question ====================  

### Does JavaScript supports namespace  

==================== Answer ====================  

JavaScript doesn’t support namespace by default. So if you create any element(function, method, object, variable) then it becomes global and pollutes the global namespace. Let's take an example of defining two functions without any namespace,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">func1</span>(<span class="hljs-params"></span>) {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'This is a first definition'</span>);
}
<span class="hljs-keyword">function</span> <span class="hljs-title function_">func1</span>(<span class="hljs-params"></span>) {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'This is a second definition'</span>);
}
<span class="hljs-title function_">func1</span>(); <span class="hljs-comment">// This is a second definition</span>
</code></pre>
<!-- codeblock-end -->

It always calls the second function definition. In this case, namespace will solve the name collision problem.

==================== Id ====================  
290

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#290-Does-javascript-supports-namespace

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
