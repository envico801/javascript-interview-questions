==================== Question ====================  

### How do you perform form validation without javascript  

==================== Answer ====================  

You can perform HTML form validation automatically without using javascript. The validation enabled by applying the `required` attribute to prevent form submission when the input is empty.

<!-- codeblock-start -->
<pre><code class="hljs language-html"><span class="hljs-tag">&#x3C;<span class="hljs-name">form</span> <span class="hljs-attr">method</span>=<span class="hljs-string">"post"</span>></span>
  <span class="hljs-tag">&#x3C;<span class="hljs-name">input</span> <span class="hljs-attr">type</span>=<span class="hljs-string">"text"</span> <span class="hljs-attr">name</span>=<span class="hljs-string">"uname"</span> <span class="hljs-attr">required</span> /></span>
  <span class="hljs-tag">&#x3C;<span class="hljs-name">input</span> <span class="hljs-attr">type</span>=<span class="hljs-string">"submit"</span> <span class="hljs-attr">value</span>=<span class="hljs-string">"Submit"</span> /></span>
<span class="hljs-tag">&#x3C;/<span class="hljs-name">form</span>></span>
</code></pre>
<!-- codeblock-end -->

**Note:** Automatic form validation does not work in Internet Explorer 9 or earlier.

==================== Id ====================  
273

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#273-How-do-you-perform-form-validation-without

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
