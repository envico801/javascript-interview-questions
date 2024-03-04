==================== Question ====================  

### What happens if we add two arrays  

==================== Answer ====================  

If you add two arrays together, it will convert them both to strings and concatenate them. For example, the result of adding arrays would be as below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>([<span class="hljs-string">'a'</span>] + [<span class="hljs-string">'b'</span>]); <span class="hljs-comment">// "ab"</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>([] + []); <span class="hljs-comment">// ""</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(![] + []); <span class="hljs-comment">// "false", because ![] returns false.</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
357

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#357-What-happens-if-we-add-two-arrays

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
