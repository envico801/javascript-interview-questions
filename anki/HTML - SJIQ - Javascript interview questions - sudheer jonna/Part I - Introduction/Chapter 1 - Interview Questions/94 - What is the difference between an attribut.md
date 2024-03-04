==================== Question ====================  

### What is the difference between an attribute and a property  

==================== Answer ====================  

Attributes are defined on the HTML markup whereas properties are defined on the DOM. For example, the below HTML element has 2 attributes type and value,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript">&#x3C;input type=<span class="hljs-string">"text"</span> value=<span class="hljs-string">"Name:"</span>>
</code></pre>
<!-- codeblock-end -->

You can retrieve the attribute value as below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> input = <span class="hljs-variable language_">document</span>.<span class="hljs-title function_">querySelector</span>(<span class="hljs-string">'input'</span>);
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(input.<span class="hljs-title function_">getAttribute</span>(<span class="hljs-string">'value'</span>)); <span class="hljs-comment">// Good morning</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(input.<span class="hljs-property">value</span>); <span class="hljs-comment">// Good morning</span>
</code></pre>
<!-- codeblock-end -->

And after you change the value of the text field to "Good evening", it becomes like

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(input.<span class="hljs-title function_">getAttribute</span>(<span class="hljs-string">'value'</span>)); <span class="hljs-comment">// Good evening</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(input.<span class="hljs-property">value</span>); <span class="hljs-comment">// Good evening</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
94

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#94-What-is-the-difference-between-an-attribut

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
