==================== Question ====================  

### How do you return all matching strings against a regular expression  

==================== Answer ====================  

The `matchAll()` method can be used to return an iterator of all results matching a string against a regular expression. For example, the below example returns an array of matching string results against a regular expression,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">let</span> regexp = <span class="hljs-regexp">/Hello(\d?))/g</span>;
<span class="hljs-keyword">let</span> greeting = <span class="hljs-string">'Hello1Hello2Hello3'</span>;
<span class="hljs-keyword">let</span> greetingList = [...greeting.<span class="hljs-title function_">matchAll</span>(regexp)];
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(greetingList[<span class="hljs-number">0</span>]); <span class="hljs-comment">//Hello1</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(greetingList[<span class="hljs-number">1</span>]); <span class="hljs-comment">//Hello2</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(greetingList[<span class="hljs-number">2</span>]); <span class="hljs-comment">//Hello3</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
347

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#347-How-do-you-return-all-matching-strings-aga

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
