==================== Question ====================  

### What is a callback function  

==================== Answer ====================  

A callback function is a function passed into another function as an argument. This function is invoked inside the outer function to complete an action.

Let's take a simple example of how to use callback function

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">callbackFunction</span>(<span class="hljs-params">name</span>) {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'Hello '</span> + name);
}
<span class="hljs-keyword">function</span> <span class="hljs-title function_">outerFunction</span>(<span class="hljs-params">callback</span>) {
  <span class="hljs-keyword">let</span> name = <span class="hljs-title function_">prompt</span>(<span class="hljs-string">'Please enter your name.'</span>);
  <span class="hljs-title function_">callback</span>(name);
}
<span class="hljs-title function_">outerFunction</span>(callbackFunction);
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
54

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#54-What-is-a-callback-function

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
