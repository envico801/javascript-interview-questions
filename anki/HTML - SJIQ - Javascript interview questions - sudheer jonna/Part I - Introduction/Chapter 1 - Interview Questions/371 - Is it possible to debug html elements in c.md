==================== Question ====================  

### Is it possible to debug HTML elements in console  

==================== Answer ====================  

Yes, it is possible to get and debug HTML elements in the console just like inspecting elements.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> element = <span class="hljs-variable language_">document</span>.<span class="hljs-title function_">getElementsByTagName</span>(<span class="hljs-string">'body'</span>)[<span class="hljs-number">0</span>];
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(element);
</code></pre>
<!-- codeblock-end -->

It prints the HTML element in the console,

![console-html](../../../../images/console-html.png)

==================== Id ====================  
371

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#371-Is-it-possible-to-debug-html-elements-in-c

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
