==================== Question ====================  

### How do you detect a browser language preference  

==================== Answer ====================  

You can use navigator object to detect a browser language preference as below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> language =
  (navigator.<span class="hljs-property">languages</span> &#x26;&#x26; navigator.<span class="hljs-property">languages</span>[<span class="hljs-number">0</span>]) || <span class="hljs-comment">// Chrome / Firefox</span>
  navigator.<span class="hljs-property">language</span> || <span class="hljs-comment">// All browsers</span>
  navigator.<span class="hljs-property">userLanguage</span>; <span class="hljs-comment">// IE &#x3C;= 10</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(language);
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
181

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#181-How-do-you-detect-a-browser-language-prefe

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
