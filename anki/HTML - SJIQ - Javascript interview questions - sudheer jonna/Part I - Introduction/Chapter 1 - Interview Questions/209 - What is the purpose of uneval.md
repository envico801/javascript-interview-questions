==================== Question ====================  

### What is the purpose of uneval  

==================== Answer ====================  

The uneval() is an inbuilt function which is used to create a string representation of the source code of an Object. It is a top-level function and is not associated with any object. Let's see the below example to know more about it's functionality,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> a = <span class="hljs-number">1</span>;
<span class="hljs-title function_">uneval</span>(a); <span class="hljs-comment">// returns a String containing 1</span>
<span class="hljs-title function_">uneval</span>(<span class="hljs-keyword">function</span> <span class="hljs-title function_">user</span>(<span class="hljs-params"></span>) {}); <span class="hljs-comment">// returns "(function user(){})"</span>
</code></pre>
<!-- codeblock-end -->

The `uneval()` function has been deprecated. It is recommended to use `toString()` for functions and `JSON.toStringify()` for other cases.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">user</span>(<span class="hljs-params"></span>) {}
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(user.<span class="hljs-title function_">toString</span>()); <span class="hljs-comment">// returns "(function user(){})"</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
209

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#209-What-is-the-purpose-of-uneval

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
