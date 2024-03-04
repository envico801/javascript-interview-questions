==================== Question ====================  

### How do you perform language specific date and time formatting  

==================== Answer ====================  

You can use the `Intl.DateTimeFormat` object which is a constructor for objects that enable language-sensitive date and time formatting. Let's see this behavior with an example,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> date = <span class="hljs-keyword">new</span> <span class="hljs-title class_">Date</span>(<span class="hljs-title class_">Date</span>.<span class="hljs-title function_">UTC</span>(<span class="hljs-number">2019</span>, <span class="hljs-number">07</span>, <span class="hljs-number">07</span>, <span class="hljs-number">3</span>, <span class="hljs-number">0</span>, <span class="hljs-number">0</span>));
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-keyword">new</span> <span class="hljs-title class_">Intl</span>.<span class="hljs-title class_">DateTimeFormat</span>(<span class="hljs-string">'en-GB'</span>).<span class="hljs-title function_">format</span>(date)); <span class="hljs-comment">// 07/08/2019</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-keyword">new</span> <span class="hljs-title class_">Intl</span>.<span class="hljs-title class_">DateTimeFormat</span>(<span class="hljs-string">'en-AU'</span>).<span class="hljs-title function_">format</span>(date)); <span class="hljs-comment">// 07/08/2019</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
233

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#233-How-do-you-perform-language-specific-date

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
