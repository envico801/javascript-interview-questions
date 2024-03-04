==================== Question ====================  

### How do you submit a form using JavaScript  

==================== Answer ====================  

You can submit a form using `document.forms[0].submit()`. All the form input's information is submitted using onsubmit event handler

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">submit</span>(<span class="hljs-params"></span>) {
  <span class="hljs-variable language_">document</span>.<span class="hljs-property">forms</span>[<span class="hljs-number">0</span>].<span class="hljs-title function_">submit</span>();
}
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
88

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#88-How-do-you-submit-a-form-using-javascript

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
