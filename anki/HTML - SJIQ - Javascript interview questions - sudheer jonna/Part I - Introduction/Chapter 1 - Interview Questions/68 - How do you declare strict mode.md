==================== Question ====================  

### How do you declare strict mode  

==================== Answer ====================  

The strict mode is declared by adding "use strict"; to the beginning of a script or a function.

If declared at the beginning of a script, it has global scope.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-meta">
'use strict'</span>;
x = <span class="hljs-number">3.14</span>; <span class="hljs-comment">// This will cause an error because x is not declared</span>
</code></pre>
<!-- codeblock-end -->

and if you declare inside a function, it has local scope

<!-- codeblock-start -->
<pre><code class="hljs language-javascript">x = <span class="hljs-number">3.14</span>; <span class="hljs-comment">// This will not cause an error.</span>
<span class="hljs-title function_">myFunction</span>();
<span class="hljs-keyword">function</span> <span class="hljs-title function_">myFunction</span>(<span class="hljs-params"></span>) {
  <span class="hljs-string">'use strict'</span>;
  y = <span class="hljs-number">3.14</span>; <span class="hljs-comment">// This will cause an error</span>
}
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
68

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#68-How-do-you-declare-strict-mode

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
