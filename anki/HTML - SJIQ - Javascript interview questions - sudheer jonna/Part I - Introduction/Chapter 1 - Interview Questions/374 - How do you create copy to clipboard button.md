==================== Question ====================  

### How do you create copy to clipboard button  

==================== Answer ====================  

You need to select the content(using .select() method) of the input element and execute the copy command with execCommand (i.e, execCommand('copy')). You can also execute other system commands like cut and paste.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-variable language_">document</span>.<span class="hljs-title function_">querySelector</span>(<span class="hljs-string">'#copy-button'</span>).<span class="hljs-property">onclick</span> = <span class="hljs-keyword">function</span> (<span class="hljs-params"></span>) {
  <span class="hljs-comment">// Select the content</span>
  <span class="hljs-variable language_">document</span>.<span class="hljs-title function_">querySelector</span>(<span class="hljs-string">'#copy-input'</span>).<span class="hljs-title function_">select</span>();
  <span class="hljs-comment">// Copy to the clipboard</span>
  <span class="hljs-variable language_">document</span>.<span class="hljs-title function_">execCommand</span>(<span class="hljs-string">'copy'</span>);
};
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
374

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#374-How-do-you-create-copy-to-clipboard-button

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
