==================== Question ====================  

### How do you compare two date objects  

==================== Answer ====================  

You need to use date.getTime() method to compare date values instead of comparison operators (==, !=, ===, and !== operators)

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> d1 = <span class="hljs-keyword">new</span> <span class="hljs-title class_">Date</span>();
<span class="hljs-keyword">var</span> d2 = <span class="hljs-keyword">new</span> <span class="hljs-title class_">Date</span>(d1);
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(d1.<span class="hljs-title function_">getTime</span>() === d2.<span class="hljs-title function_">getTime</span>()); <span class="hljs-comment">//True</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(d1 === d2); <span class="hljs-comment">// False</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
132

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#132-How-do-you-compare-two-date-objects

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
