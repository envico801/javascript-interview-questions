==================== Question ====================  

### What is typescript  

==================== Answer ====================  

TypeScript is a typed superset of JavaScript created by Microsoft that adds optional types, classes, async/await, and many other features, and compiles to plain JavaScript. Angular built entirely in TypeScript and used as a primary language. You can install it globally as

<!-- codeblock-start -->
<pre><code class="hljs language-bash">npm install -g typescript
</code></pre>
<!-- codeblock-end -->

Let's see a simple example of TypeScript usage,

<!-- codeblock-start -->
<pre><code class="hljs language-typescript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">greeting</span>(<span class="hljs-params">name: <span class="hljs-built_in">string</span></span>): <span class="hljs-built_in">string</span> {
  <span class="hljs-keyword">return</span> <span class="hljs-string">'Hello, '</span> + name;
}
<span class="hljs-keyword">let</span> user = <span class="hljs-string">'Sudheer'</span>;
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-title function_">greeting</span>(user));
</code></pre>
<!-- codeblock-end -->

The greeting method allows only string type as argument.

==================== Id ====================  
251

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#251-What-is-typescript

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
