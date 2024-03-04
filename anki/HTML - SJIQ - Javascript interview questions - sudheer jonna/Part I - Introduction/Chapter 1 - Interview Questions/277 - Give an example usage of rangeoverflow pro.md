==================== Question ====================  

### Give an example usage of rangeOverflow property  

==================== Answer ====================  

If an element's value is greater than its max attribute then rangeOverflow property returns true. For example, the below form submission throws an error if the value is more than 100,

<!-- codeblock-start -->
<pre><code class="hljs language-html"><span class="hljs-tag">&#x3C;<span class="hljs-name">input</span> <span class="hljs-attr">id</span>=<span class="hljs-string">"age"</span> <span class="hljs-attr">type</span>=<span class="hljs-string">"number"</span> <span class="hljs-attr">max</span>=<span class="hljs-string">"100"</span> /></span> <span class="hljs-tag">&#x3C;<span class="hljs-name">button</span> <span class="hljs-attr">onclick</span>=<span class="hljs-string">"myOverflowFunction()"</span>></span>OK<span class="hljs-tag">&#x3C;/<span class="hljs-name">button</span>></span>
</code></pre>
<!-- codeblock-end -->

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">myOverflowFunction</span>(<span class="hljs-params"></span>) {
  <span class="hljs-keyword">if</span> (<span class="hljs-variable language_">document</span>.<span class="hljs-title function_">getElementById</span>(<span class="hljs-string">'age'</span>).<span class="hljs-property">validity</span>.<span class="hljs-property">rangeOverflow</span>) {
     <span class="hljs-title function_">alert</span>(<span class="hljs-string">'The mentioned age is not allowed'</span>);
  }
}
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
277

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#277-Give-an-example-usage-of-rangeoverflow-pro

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
