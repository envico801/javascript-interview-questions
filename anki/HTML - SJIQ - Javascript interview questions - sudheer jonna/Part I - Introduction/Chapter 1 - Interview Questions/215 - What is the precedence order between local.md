==================== Question ====================  

### What is the precedence order between local and global variables  

==================== Answer ====================  

A local variable takes precedence over a global variable with the same name. Let's see this behavior in an example.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> msg = <span class="hljs-string">'Good morning'</span>;
<span class="hljs-keyword">function</span> <span class="hljs-title function_">greeting</span>(<span class="hljs-params"></span>) {
  msg = <span class="hljs-string">'Good Evening'</span>;
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(msg); <span class="hljs-comment">// Good Evening</span>
}
<span class="hljs-title function_">greeting</span>();
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
215

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#215-What-is-the-precedence-order-between-local

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
