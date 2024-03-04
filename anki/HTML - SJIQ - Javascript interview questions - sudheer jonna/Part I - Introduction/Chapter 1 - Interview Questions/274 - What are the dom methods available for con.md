==================== Question ====================  

### What are the DOM methods available for constraint validation  

==================== Answer ====================  

The below DOM methods are available for constraint validation on an invalid input,

1. checkValidity(): It returns true if an input element contains valid data.

2. setCustomValidity(): It is used to set the validationMessage property of an input element.

    Let's take an user login form with DOM validations

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">myFunction</span>(<span class="hljs-params"></span>) {
  <span class="hljs-keyword">var</span> userName = <span class="hljs-variable language_">document</span>.<span class="hljs-title function_">getElementById</span>(<span class="hljs-string">'uname'</span>);
  <span class="hljs-keyword">if</span> (!userName.<span class="hljs-title function_">checkValidity</span>()) {
     <span class="hljs-variable language_">document</span>.<span class="hljs-title function_">getElementById</span>(<span class="hljs-string">'message'</span>).<span class="hljs-property">innerHTML</span> = userName.<span class="hljs-property">validationMessage</span>;
  } <span class="hljs-keyword">else</span> {
     <span class="hljs-variable language_">document</span>.<span class="hljs-title function_">getElementById</span>(<span class="hljs-string">'message'</span>).<span class="hljs-property">innerHTML</span> = <span class="hljs-string">'Entered a valid username'</span>;
  }
}
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
274

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#274-What-are-the-dom-methods-available-for-con

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
