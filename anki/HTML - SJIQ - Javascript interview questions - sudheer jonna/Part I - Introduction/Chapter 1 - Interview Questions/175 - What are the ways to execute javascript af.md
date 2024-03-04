==================== Question ====================  

### What are the ways to execute javascript after page load  

==================== Answer ====================  

You can execute javascript after page load in many different ways,

1. **window.onload:**

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-variable language_">window</span>.<span class="hljs-property">onload</span> = <span class="hljs-keyword">function</span> ...
</code></pre>
<!-- codeblock-end -->

1. **document.onload:**

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-variable language_">document</span>.<span class="hljs-property">onload</span> = <span class="hljs-keyword">function</span> ...
</code></pre>
<!-- codeblock-end -->

1. **body onload:**

<!-- codeblock-start -->
<pre><code class="hljs language-javascript">&#x3C;body onload=<span class="hljs-string">"script();"</span>>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
175

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#175-What-are-the-ways-to-execute-javascript-af

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
