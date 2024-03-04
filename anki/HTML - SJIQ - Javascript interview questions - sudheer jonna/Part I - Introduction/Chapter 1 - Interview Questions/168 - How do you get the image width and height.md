==================== Question ====================  

### How do you get the image width and height using JS  

==================== Answer ====================  

You can programmatically get the image and check the dimensions(width and height) using Javascript.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> img = <span class="hljs-keyword">new</span> <span class="hljs-title class_">Image</span>();
img.<span class="hljs-property">onload</span> = <span class="hljs-keyword">function</span> (<span class="hljs-params"></span>) {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-variable language_">this</span>.<span class="hljs-property">width</span> + <span class="hljs-string">'x'</span> + <span class="hljs-variable language_">this</span>.<span class="hljs-property">height</span>);
};
img.<span class="hljs-property">src</span> = <span class="hljs-string">'http://www.google.com/intl/en_ALL/images/logo.gif'</span>;
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
168

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#168-How-do-you-get-the-image-width-and-height

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
