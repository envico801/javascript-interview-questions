==================== Question ====================  

### What is ArrayBuffer  

==================== Answer ====================  

An ArrayBuffer object is used to represent a generic, fixed-length raw binary data buffer. You can create it as below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">let</span> buffer = <span class="hljs-keyword">new</span> <span class="hljs-title class_">ArrayBuffer</span>(<span class="hljs-number">16</span>); <span class="hljs-comment">// create a buffer of length 16</span>
<span class="hljs-title function_">alert</span>(buffer.<span class="hljs-property">byteLength</span>); <span class="hljs-comment">// 16</span>
</code></pre>
<!-- codeblock-end -->

To manipulate an ArrayBuffer, we need to use a “view” object.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-comment">//Create a DataView referring to the buffer</span>
<span class="hljs-keyword">let</span> view = <span class="hljs-keyword">new</span> <span class="hljs-title class_">DataView</span>(buffer);
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
336

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#336-What-is-arraybuffer

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
