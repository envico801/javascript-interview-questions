==================== Question ====================  

### What is the use of stopPropagation method  

==================== Answer ====================  

The stopPropagation method is used to stop the event from bubbling up the event chain. For example, the below nested divs with stopPropagation method prevents default event propagation when clicking on nested div(Div1)

<!-- codeblock-start -->
<pre><code class="hljs language-javascript">&#x3C;p><span class="hljs-title class_">Click</span> <span class="hljs-title class_">DIV1</span> <span class="hljs-title class_">Element</span>&#x3C;/p>
<span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span> <span class="hljs-attr">onclick</span>=<span class="hljs-string">"secondFunc()"</span>></span>DIV 2
  <span class="hljs-tag">&#x3C;<span class="hljs-name">div</span> <span class="hljs-attr">onclick</span>=<span class="hljs-string">"firstFunc(event)"</span>></span>DIV 1<span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span>
<span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span></span>
<span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">script</span>></span><span class="javascript">
<span class="hljs-keyword">function</span> <span class="hljs-title function_">firstFunc</span>(<span class="hljs-params">event</span>) {
  <span class="hljs-title function_">alert</span>(<span class="hljs-string">"DIV 1"</span>);
  event.<span class="hljs-title function_">stopPropagation</span>();
}
<span class="hljs-keyword">function</span> <span class="hljs-title function_">secondFunc</span>(<span class="hljs-params"></span>) {
  <span class="hljs-title function_">alert</span>(<span class="hljs-string">"DIV 2"</span>);
}
</span><span class="hljs-tag">&#x3C;/<span class="hljs-name">script</span>></span></span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
103

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#103-What-is-the-use-of-stoppropagation-method

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
