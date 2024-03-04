==================== Question ====================  

### How do you perform form validation using javascript  

==================== Answer ====================  

JavaScript can be used to perform HTML form validation. For example, if the form field is empty, the function needs to notify, and return false, to prevent the form being submitted.

Lets' perform user login in an html form,

<!-- codeblock-start -->
<pre><code class="hljs language-html"><span class="hljs-tag">&#x3C;<span class="hljs-name">form</span> <span class="hljs-attr">name</span>=<span class="hljs-string">"myForm"</span> <span class="hljs-attr">onsubmit</span>=<span class="hljs-string">"return validateForm()"</span> <span class="hljs-attr">method</span>=<span class="hljs-string">"post"</span>></span>
  User name: <span class="hljs-tag">&#x3C;<span class="hljs-name">input</span> <span class="hljs-attr">type</span>=<span class="hljs-string">"text"</span> <span class="hljs-attr">name</span>=<span class="hljs-string">"uname"</span> /></span>
  <span class="hljs-tag">&#x3C;<span class="hljs-name">input</span> <span class="hljs-attr">type</span>=<span class="hljs-string">"submit"</span> <span class="hljs-attr">value</span>=<span class="hljs-string">"Submit"</span> /></span>
<span class="hljs-tag">&#x3C;/<span class="hljs-name">form</span>></span>
</code></pre>
<!-- codeblock-end -->

And the validation on user login is below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">validateForm</span>(<span class="hljs-params"></span>) {
  <span class="hljs-keyword">var</span> x = <span class="hljs-variable language_">document</span>.<span class="hljs-property">forms</span>[<span class="hljs-string">'myForm'</span>][<span class="hljs-string">'uname'</span>].<span class="hljs-property">value</span>;
  <span class="hljs-keyword">if</span> (x == <span class="hljs-string">''</span>) {
     <span class="hljs-title function_">alert</span>(<span class="hljs-string">"The username shouldn't be empty"</span>);
     <span class="hljs-keyword">return</span> <span class="hljs-literal">false</span>;
  }
}
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
272

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#272-How-do-you-perform-form-validation-using-j

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
