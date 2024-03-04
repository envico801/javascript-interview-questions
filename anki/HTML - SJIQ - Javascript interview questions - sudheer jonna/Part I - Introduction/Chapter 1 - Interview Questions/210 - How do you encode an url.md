==================== Question ====================  

### How do you encode an URL  

==================== Answer ====================  

The encodeURI() function is used to encode complete URI which has special characters except (, / ? : @ & = + $ #) characters.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> uri = <span class="hljs-string">'https://mozilla.org/?x=шеллы'</span>;
<span class="hljs-keyword">var</span> encoded = <span class="hljs-built_in">encodeURI</span>(uri);
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(encoded); <span class="hljs-comment">// https://mozilla.org/?x=%D1%88%D0%B5%D0%BB%D0%BB%D1%8B</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
210

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#210-How-do-you-encode-an-url

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
