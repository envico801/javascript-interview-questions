==================== Question ====================  

### How do you change the style of a HTML element  

==================== Answer ====================  

You can change inline style or classname of a HTML element using javascript

1. **Using style property:** You can modify inline style using style property

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-variable language_">document</span>.<span class="hljs-title function_">getElementById</span>(<span class="hljs-string">'title'</span>).<span class="hljs-property">style</span>.<span class="hljs-property">fontSize</span> = <span class="hljs-string">'30px'</span>;
</code></pre>
<!-- codeblock-end -->

1. **Using ClassName property:** It is easy to modify element class using className property

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-variable language_">document</span>.<span class="hljs-title function_">getElementById</span>(<span class="hljs-string">'title'</span>).<span class="hljs-property">className</span> = <span class="hljs-string">'custom-title'</span>;
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
161

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#161-How-do-you-change-the-style-of-a-html-elem

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
