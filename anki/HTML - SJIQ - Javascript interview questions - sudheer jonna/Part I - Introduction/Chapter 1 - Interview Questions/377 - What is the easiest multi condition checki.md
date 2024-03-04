==================== Question ====================  

### What is the easiest multi condition checking  

==================== Answer ====================  

You can use `indexOf` to compare input with multiple values instead of checking each value as one condition.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-comment">// Verbose approach</span>
<span class="hljs-keyword">if</span> (input === <span class="hljs-string">'first'</span> || input === <span class="hljs-number">1</span> || input === <span class="hljs-string">'second'</span> || input === <span class="hljs-number">2</span>) {
  <span class="hljs-title function_">someFunction</span>();
}
<span class="hljs-comment">// Shortcut</span>
<span class="hljs-keyword">if</span> ([<span class="hljs-string">'first'</span>, <span class="hljs-number">1</span>, <span class="hljs-string">'second'</span>, <span class="hljs-number">2</span>].<span class="hljs-title function_">indexOf</span>(input) !== -<span class="hljs-number">1</span>) {
  <span class="hljs-title function_">someFunction</span>();
}
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
377

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#377-What-is-the-easiest-multi-condition-checki

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
