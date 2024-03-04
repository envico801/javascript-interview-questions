==================== Question ====================  

### What Is Obfuscation in javascript  

==================== Answer ====================  

Obfuscation is the deliberate act of creating obfuscated javascript code(i.e, source or machine code) that is difficult for humans to understand. It is something similar to encryption, but a machine can understand the code and execute it.

Let's see the below function before Obfuscation,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">greeting</span>(<span class="hljs-params"></span>) {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'Hello, welcome to JS world'</span>);
}
</code></pre>
<!-- codeblock-end -->

And after the code Obfuscation, it would be appeared as below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-built_in">eval</span>(
  (<span class="hljs-keyword">function</span> (<span class="hljs-params">p, a, c, k, e, d</span>) {
     e = <span class="hljs-keyword">function</span> (<span class="hljs-params">c</span>) {
       <span class="hljs-keyword">return</span> c;
     };
     <span class="hljs-keyword">if</span> (!<span class="hljs-string">''</span>.<span class="hljs-title function_">replace</span>(<span class="hljs-regexp">/^/</span>, <span class="hljs-title class_">String</span>)) {
       <span class="hljs-keyword">while</span> (c--) {
         d[c] = k[c] || c;
       }
       k = [
         <span class="hljs-keyword">function</span> (<span class="hljs-params">e</span>) {
           <span class="hljs-keyword">return</span> d[e];
         },
       ];
       e = <span class="hljs-keyword">function</span> (<span class="hljs-params"></span>) {
         <span class="hljs-keyword">return</span> <span class="hljs-string">'\\w+'</span>;
       };
       c = <span class="hljs-number">1</span>;
     }
     <span class="hljs-keyword">while</span> (c--) {
       <span class="hljs-keyword">if</span> (k[c]) {
         p = p.<span class="hljs-title function_">replace</span>(<span class="hljs-keyword">new</span> <span class="hljs-title class_">RegExp</span>(<span class="hljs-string">'\\b'</span> + <span class="hljs-title function_">e</span>(c) + <span class="hljs-string">'\\b'</span>, <span class="hljs-string">'g'</span>), k[c]);
       }
     }
     <span class="hljs-keyword">return</span> p;
  })(<span class="hljs-string">"2 1(){0.3('4, 7 6 5 8')}"</span>, <span class="hljs-number">9</span>, <span class="hljs-number">9</span>, <span class="hljs-string">'console|greeting|function|log|Hello|JS|to|welcome|world'</span>.<span class="hljs-title function_">split</span>(<span class="hljs-string">'|'</span>), <span class="hljs-number">0</span>, {}),
);
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
266

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#266-What-is-obfuscation-in-javascript

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
