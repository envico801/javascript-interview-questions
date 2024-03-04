==================== Question ====================  

### How do you convert character to ASCII code  

==================== Answer ====================  

You can use the `String.prototype.charCodeAt()` method to convert string characters to ASCII numbers. For example, let's find ASCII code for the first letter of 'ABC' string,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-string">'ABC'</span>.<span class="hljs-title function_">charCodeAt</span>(<span class="hljs-number">0</span>); <span class="hljs-comment">// returns 65</span>
</code></pre>
<!-- codeblock-end -->

Whereas `String.fromCharCode()` method converts numbers to equal ASCII characters.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-title class_">String</span>.<span class="hljs-title function_">fromCharCode</span>(<span class="hljs-number">65</span>, <span class="hljs-number">66</span>, <span class="hljs-number">67</span>); <span class="hljs-comment">// returns 'ABC'</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
335

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#335-How-do-you-convert-character-to-ascii-code

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
