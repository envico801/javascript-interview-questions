==================== Question ====================  

### How to remove all line breaks from a string  

==================== Answer ====================  

The easiest approach is using regular expressions to detect and replace newlines in the string. In this case, we use replace function along with string to replace with, which in our case is an empty string.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">remove_linebreaks</span>(<span class="hljs-params"> <span class="hljs-keyword">var</span> message </span>) {
     <span class="hljs-keyword">return</span> message.<span class="hljs-title function_">replace</span>( <span class="hljs-regexp">/[\r\n]+/gm</span>, <span class="hljs-string">""</span> );
}
</code></pre>
<!-- codeblock-end -->

In the above expression, g and m are for global and multiline flags.

==================== Id ====================  
354

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#354-How-to-remove-all-line-breaks-from-a-strin

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
