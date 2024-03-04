==================== Question ====================  

### What are break and continue statements  

==================== Answer ====================  

The break statement is used to "jump out" of a loop. i.e, It breaks the loop and continues executing the code after the loop.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">for</span> (i = <span class="hljs-number">0</span>; i &#x3C; <span class="hljs-number">10</span>; i++) {
  <span class="hljs-keyword">if</span> (i === <span class="hljs-number">5</span>) {
     <span class="hljs-keyword">break</span>;
  }
  text += <span class="hljs-string">'Number: '</span> + i + <span class="hljs-string">'&#x3C;br>'</span>;
}
</code></pre>
<!-- codeblock-end -->

The continue statement is used to "jump over" one iteration in the loop. i.e, It breaks one iteration (in the loop), if a specified condition occurs, and continues with the next iteration in the loop.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">for</span> (i = <span class="hljs-number">0</span>; i &#x3C; <span class="hljs-number">10</span>; i++) {
  <span class="hljs-keyword">if</span> (i === <span class="hljs-number">5</span>) {
     <span class="hljs-keyword">continue</span>;
  }
  text += <span class="hljs-string">'Number: '</span> + i + <span class="hljs-string">'&#x3C;br>'</span>;
}
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
143

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#143-What-are-break-and-continue-statements

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
