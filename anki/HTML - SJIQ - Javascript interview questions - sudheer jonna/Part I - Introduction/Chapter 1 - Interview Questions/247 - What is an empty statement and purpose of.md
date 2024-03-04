==================== Question ====================  

### What is an empty statement and purpose of it  

==================== Answer ====================  

The empty statement is a semicolon (;) indicating that no statement will be executed, even if JavaScript syntax requires one. Since there is no action with an empty statement you might think that it's usage is quite less, but the empty statement is occasionally useful when you want to create a loop that has an empty body. For example, you can initialize an array with zero values as below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-comment">// Initialize an array a</span>
<span class="hljs-keyword">for</span> (<span class="hljs-keyword">let</span> i = <span class="hljs-number">0</span>; i &#x3C; a.<span class="hljs-property">length</span>; a[i++] = <span class="hljs-number">0</span>);
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
247

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#247-What-is-an-empty-statement-and-purpose-of

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
