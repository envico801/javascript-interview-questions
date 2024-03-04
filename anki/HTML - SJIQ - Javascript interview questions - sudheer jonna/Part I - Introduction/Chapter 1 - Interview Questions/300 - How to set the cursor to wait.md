==================== Question ====================  

### How to set the cursor to wait  

==================== Answer ====================  

The cursor can be set to wait in JavaScript by using the property "cursor". Let's perform this behavior on page load using the below function.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">myFunction</span>(<span class="hljs-params"></span>) {
  <span class="hljs-variable language_">window</span>.<span class="hljs-property">document</span>.<span class="hljs-property">body</span>.<span class="hljs-property">style</span>.<span class="hljs-property">cursor</span> = <span class="hljs-string">'wait'</span>;
}
</code></pre>
<!-- codeblock-end -->

and this function invoked on page load

<!-- codeblock-start -->
<pre><code class="hljs language-html"><span class="hljs-tag">&#x3C;<span class="hljs-name">body</span> <span class="hljs-attr">onload</span>=<span class="hljs-string">"myFunction()"</span>></span><span class="hljs-tag">&#x3C;/<span class="hljs-name">body</span>></span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
300

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#300-How-to-set-the-cursor-to-wait

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
