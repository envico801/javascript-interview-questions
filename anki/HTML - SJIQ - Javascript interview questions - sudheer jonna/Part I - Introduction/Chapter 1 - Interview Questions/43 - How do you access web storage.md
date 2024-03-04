==================== Question ====================  

### How do you access web storage  

==================== Answer ====================  

The Window object implements the `WindowLocalStorage` and `WindowSessionStorage` objects which has `localStorage`(window.localStorage) and `sessionStorage`(window.sessionStorage) properties respectively. These properties create an instance of the Storage object, through which data items can be set, retrieved and removed for a specific domain and storage type (session or local).

For example, you can read and write on local storage objects as below

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-variable language_">localStorage</span>.<span class="hljs-title function_">setItem</span>(<span class="hljs-string">'logo'</span>, <span class="hljs-variable language_">document</span>.<span class="hljs-title function_">getElementById</span>(<span class="hljs-string">'logo'</span>).<span class="hljs-property">value</span>);
<span class="hljs-variable language_">localStorage</span>.<span class="hljs-title function_">getItem</span>(<span class="hljs-string">'logo'</span>);
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
43

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#43-How-do-you-access-web-storage

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
