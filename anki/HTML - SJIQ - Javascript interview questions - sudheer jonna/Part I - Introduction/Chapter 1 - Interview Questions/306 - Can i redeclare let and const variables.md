==================== Question ====================  

### Can I redeclare let and const variables  

==================== Answer ====================  

No, you cannot redeclare let and const variables. If you do, it throws below error

<!-- codeblock-start -->
<pre><code class="hljs language-bash">Uncaught SyntaxError: Identifier <span class="hljs-string">'someVariable'</span> has already been declared
</code></pre>
<!-- codeblock-end -->

**Explanation:** The variable declaration with `var` keyword refers to a function scope and the variable is treated as if it were declared at the top of the enclosing scope due to hoisting feature. So all the multiple declarations contributing to the same hoisted variable without any error. Let's take an example of re-declaring variables in the same scope for both var and let/const variables.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> name = <span class="hljs-string">'John'</span>;
<span class="hljs-keyword">function</span> <span class="hljs-title function_">myFunc</span>(<span class="hljs-params"></span>) {
  <span class="hljs-keyword">var</span> name = <span class="hljs-string">'Nick'</span>;
  <span class="hljs-keyword">var</span> name = <span class="hljs-string">'Abraham'</span>; <span class="hljs-comment">// Re-assigned in the same function block</span>
  <span class="hljs-title function_">alert</span>(name); <span class="hljs-comment">// Abraham</span>
}
<span class="hljs-title function_">myFunc</span>();
<span class="hljs-title function_">alert</span>(name); <span class="hljs-comment">// John</span>
</code></pre>
<!-- codeblock-end -->

The block-scoped multi-declaration throws syntax error,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">let</span> name = <span class="hljs-string">'John'</span>;
<span class="hljs-keyword">function</span> <span class="hljs-title function_">myFunc</span>(<span class="hljs-params"></span>) {
  <span class="hljs-keyword">let</span> name = <span class="hljs-string">'Nick'</span>;
  <span class="hljs-keyword">let</span> name = <span class="hljs-string">'Abraham'</span>; <span class="hljs-comment">// Uncaught SyntaxError: Identifier 'name' has already been declared</span>
  <span class="hljs-title function_">alert</span>(name);
}
<span class="hljs-title function_">myFunc</span>();
<span class="hljs-title function_">alert</span>(name);
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
306

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#306-Can-i-redeclare-let-and-const-variables

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
