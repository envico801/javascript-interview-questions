==================== Question ====================  

### What are the options in a cookie  

==================== Answer ====================  

There are few below options available for a cookie,

1. By default, the cookie is deleted when the browser is closed but you can change this behavior by setting expiry date (in UTC time).

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-variable language_">document</span>.<span class="hljs-property">cookie</span> = <span class="hljs-string">'username=John; expires=Sat, 8 Jun 2019 12:00:00 UTC'</span>;
</code></pre>
<!-- codeblock-end -->

1. By default, the cookie belongs to a current page. But you can tell the browser what path the cookie belongs to using a path parameter.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-variable language_">document</span>.<span class="hljs-property">cookie</span> = <span class="hljs-string">'username=John; path=/services'</span>;
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
39

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#39-What-are-the-options-in-a-cookie

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
