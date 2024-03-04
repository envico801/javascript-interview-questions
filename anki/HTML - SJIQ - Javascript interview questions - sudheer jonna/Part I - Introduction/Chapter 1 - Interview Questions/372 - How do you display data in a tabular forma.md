==================== Question ====================  

### How do you display data in a tabular format using console object  

==================== Answer ====================  

The `console.table()` is used to display data in the console in a tabular format to visualize complex arrays or objects.

<!-- codeblock-start -->
<pre><code class="hljs language-js"><span class="hljs-keyword">const</span> users = [
  { <span class="hljs-attr">name</span>: <span class="hljs-string">'John'</span>, <span class="hljs-attr">id</span>: <span class="hljs-number">1</span>, <span class="hljs-attr">city</span>: <span class="hljs-string">'Delhi'</span> },
  { <span class="hljs-attr">name</span>: <span class="hljs-string">'Max'</span>, <span class="hljs-attr">id</span>: <span class="hljs-number">2</span>, <span class="hljs-attr">city</span>: <span class="hljs-string">'London'</span> },
  { <span class="hljs-attr">name</span>: <span class="hljs-string">'Rod'</span>, <span class="hljs-attr">id</span>: <span class="hljs-number">3</span>, <span class="hljs-attr">city</span>: <span class="hljs-string">'Paris'</span> },
];
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">table</span>(users);
</code></pre>
<!-- codeblock-end -->

The data visualized in a table format,

![console-table](../../../../images/console-table.png)

**Not:** Remember that `console.table()` is not supported in IE.

==================== Id ====================  
372

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#372-How-do-you-display-data-in-a-tabular-forma

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
