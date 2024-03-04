==================== Question ====================  

### How do you validate an email in javascript  

==================== Answer ====================  

You can validate an email in javascript using regular expressions. It is recommended to do validations on the server side instead of the client side. Because the javascript can be disabled on the client side.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">validateEmail</span>(<span class="hljs-params">email</span>) {
  <span class="hljs-keyword">var</span> re = <span class="hljs-regexp">/^(([^&#x3C;>()\[\]\\.,;:\s@"]+(\.[^&#x3C;>()\[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/</span>;
  <span class="hljs-keyword">return</span> re.<span class="hljs-title function_">test</span>(<span class="hljs-title class_">String</span>(email).<span class="hljs-title function_">toLowerCase</span>());
}
</code></pre>
<!-- codeblock-end -->

The above regular expression accepts unicode characters.

==================== Id ====================  
121

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#121-How-do-you-validate-an-email-in-javascript

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
