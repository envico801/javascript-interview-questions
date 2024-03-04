==================== Question ====================  

### How do you trim a string in javascript  

==================== Answer ====================  

JavaScript provided a trim method on string types to trim any whitespaces present at the beginning or ending of the string.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-string">'  Hello World   '</span>.<span class="hljs-title function_">trim</span>(); <span class="hljs-comment">//Hello World</span>
</code></pre>
<!-- codeblock-end -->

If your browser(<IE9) doesn't support this method then you can use below polyfill.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">if</span> (!<span class="hljs-title class_">String</span>.<span class="hljs-property"><span class="hljs-keyword">prototype</span></span>.<span class="hljs-property">trim</span>) {
  (<span class="hljs-keyword">function</span> (<span class="hljs-params"></span>) {
     <span class="hljs-comment">// Make sure we trim BOM and NBSP</span>
     <span class="hljs-keyword">var</span> rtrim = <span class="hljs-regexp">/^[\s\uFEFF\xA0]+|[\s\uFEFF\xA0]+$/g</span>;
     <span class="hljs-title class_">String</span>.<span class="hljs-property"><span class="hljs-keyword">prototype</span></span>.<span class="hljs-property">trim</span> = <span class="hljs-keyword">function</span> (<span class="hljs-params"></span>) {
       <span class="hljs-keyword">return</span> <span class="hljs-variable language_">this</span>.<span class="hljs-title function_">replace</span>(rtrim, <span class="hljs-string">''</span>);
     };
  })();
}
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
134

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#134-How-do-you-trim-a-string-in-javascript

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
