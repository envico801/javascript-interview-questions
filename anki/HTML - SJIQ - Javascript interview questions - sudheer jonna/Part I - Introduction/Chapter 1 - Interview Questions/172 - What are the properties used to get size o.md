==================== Question ====================  

### What are the properties used to get size of window  

==================== Answer ====================  

You can use innerWidth, innerHeight, clientWidth, clientHeight properties of windows, document element and document body objects to find the size of a window. Let's use them combination of these properties to calculate the size of a window or document,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> width = <span class="hljs-variable language_">window</span>.<span class="hljs-property">innerWidth</span> || <span class="hljs-variable language_">document</span>.<span class="hljs-property">documentElement</span>.<span class="hljs-property">clientWidth</span> || <span class="hljs-variable language_">document</span>.<span class="hljs-property">body</span>.<span class="hljs-property">clientWidth</span>;
<span class="hljs-keyword">var</span> height = <span class="hljs-variable language_">window</span>.<span class="hljs-property">innerHeight</span> || <span class="hljs-variable language_">document</span>.<span class="hljs-property">documentElement</span>.<span class="hljs-property">clientHeight</span> || <span class="hljs-variable language_">document</span>.<span class="hljs-property">body</span>.<span class="hljs-property">clientHeight</span>;
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
172

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#172-What-are-the-properties-used-to-get-size-o

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
