==================== Question ====================  

### What is the purpose of void 0  

==================== Answer ====================  

Void(0) is used to prevent the page from refreshing. This will be helpful to eliminate the unwanted side-effect, because it will return the undefined primitive value. It is commonly used for HTML documents that use href="JavaScript:Void(0);" within an `<a>` element. i.e, when you click a link, the browser loads a new page or refreshes the same page. But this behavior will be prevented using this expression.

For example, the below link notify the message without reloading the page

<!-- codeblock-start -->
<pre><code class="hljs language-javascript">&#x3C;a href=<span class="hljs-string">'JavaScript:void(0);'</span> onclick=<span class="hljs-string">"alert('Well done!')"</span>>
  <span class="hljs-title class_">Click</span> <span class="hljs-title class_">Me</span>!
&#x3C;/a>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
96

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#96-What-is-the-purpose-of-void-0

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
