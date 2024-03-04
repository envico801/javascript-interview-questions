==================== Question ====================  

### What are typed arrays  

==================== Answer ====================  

Typed arrays are array-like objects from ECMAScript 6 API for handling binary data. JavaScript provides 8 Typed array types,

1. Int8Array: An array of 8-bit signed integers

2. Int16Array: An array of 16-bit signed integers

3. Int32Array: An array of 32-bit signed integers

4. Uint8Array: An array of 8-bit unsigned integers

5. Uint16Array: An array of 16-bit unsigned integers

6. Uint32Array: An array of 32-bit unsigned integers

7. Float32Array: An array of 32-bit floating point numbers

8. Float64Array: An array of 64-bit floating point numbers

For example, you can create an array of 8-bit signed integers as below

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> a = <span class="hljs-keyword">new</span> <span class="hljs-title class_">Int8Array</span>();
<span class="hljs-comment">// You can pre-allocate n bytes</span>
<span class="hljs-keyword">const</span> bytes = <span class="hljs-number">1024</span>;
<span class="hljs-keyword">const</span> a = <span class="hljs-keyword">new</span> <span class="hljs-title class_">Int8Array</span>(bytes);
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
320

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#320-What-are-typed-arrays

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
