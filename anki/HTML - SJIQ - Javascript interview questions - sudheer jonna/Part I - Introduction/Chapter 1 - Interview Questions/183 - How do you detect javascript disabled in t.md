==================== Question ====================  

### How do you detect javascript disabled in the page  

==================== Answer ====================  

You can use the `<noscript>` tag to detect javascript disabled or not. The code block inside `<noscript>` gets executed when JavaScript is disabled, and is typically used to display alternative content when the page generated in JavaScript.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript">&#x3C;script type=<span class="hljs-string">"javascript"</span>>
     <span class="hljs-comment">// JS related code goes here</span>
&#x3C;/script>
<span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">noscript</span>></span>
     <span class="hljs-tag">&#x3C;<span class="hljs-name">a</span> <span class="hljs-attr">href</span>=<span class="hljs-string">"next_page.html?noJS=true"</span>></span>JavaScript is disabled in the page. Please click Next Page<span class="hljs-tag">&#x3C;/<span class="hljs-name">a</span>></span>
<span class="hljs-tag">&#x3C;/<span class="hljs-name">noscript</span>></span></span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
183

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#183-How-do-you-detect-javascript-disabled-in-t

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
