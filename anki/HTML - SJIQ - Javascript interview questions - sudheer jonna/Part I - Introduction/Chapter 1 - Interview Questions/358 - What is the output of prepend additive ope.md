==================== Question ====================  

### What is the output of prepend additive operator on falsy values  

==================== Answer ====================  

If you prepend the additive(+) operator on falsy values(null, undefined, NaN, false, ""), the falsy value converts to a number value zero. Let's display them on browser console as below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(+<span class="hljs-literal">null</span>); <span class="hljs-comment">// 0</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(+<span class="hljs-literal">undefined</span>); <span class="hljs-comment">// NaN</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(+<span class="hljs-literal">false</span>); <span class="hljs-comment">// 0</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(+<span class="hljs-title class_">NaN</span>); <span class="hljs-comment">// NaN</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(+<span class="hljs-string">''</span>); <span class="hljs-comment">// 0</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
358

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#358-What-is-the-output-of-prepend-additive-ope

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
