==================== Question ====================  

### How do you map the array values without using map method  

==================== Answer ====================  

You can map the array values without using the `map` method by just using the `from` method of Array. Let's map city names from Countries array,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> countries = [
  { <span class="hljs-attr">name</span>: <span class="hljs-string">'India'</span>, <span class="hljs-attr">capital</span>: <span class="hljs-string">'Delhi'</span> },
  { <span class="hljs-attr">name</span>: <span class="hljs-string">'US'</span>, <span class="hljs-attr">capital</span>: <span class="hljs-string">'Washington'</span> },
  { <span class="hljs-attr">name</span>: <span class="hljs-string">'Russia'</span>, <span class="hljs-attr">capital</span>: <span class="hljs-string">'Moscow'</span> },
  { <span class="hljs-attr">name</span>: <span class="hljs-string">'Singapore'</span>, <span class="hljs-attr">capital</span>: <span class="hljs-string">'Singapore'</span> },
  { <span class="hljs-attr">name</span>: <span class="hljs-string">'China'</span>, <span class="hljs-attr">capital</span>: <span class="hljs-string">'Beijing'</span> },
  { <span class="hljs-attr">name</span>: <span class="hljs-string">'France'</span>, <span class="hljs-attr">capital</span>: <span class="hljs-string">'Paris'</span> },
];
<span class="hljs-keyword">const</span> cityNames = <span class="hljs-title class_">Array</span>.<span class="hljs-title function_">from</span>(countries, <span class="hljs-function">(<span class="hljs-params">{ capital }</span>) =></span> capital);
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(cityNames); <span class="hljs-comment">// ['Delhi, 'Washington', 'Moscow', 'Singapore', 'Beijing', 'Paris']</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
363

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#363-How-do-you-map-the-array-values-without-us

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
