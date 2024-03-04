==================== Question ====================  

### What is a constructor method  

==================== Answer ====================  

The constructor method is a special method for creating and initializing an object created within a class. If you do not specify a constructor method, a default constructor is used. The example usage of constructor would be as below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">class</span> <span class="hljs-title class_">Employee</span> {
  <span class="hljs-title function_">constructor</span>(<span class="hljs-params"></span>) {
     <span class="hljs-variable language_">this</span>.<span class="hljs-property">name</span> = <span class="hljs-string">'John'</span>;
  }
}
<span class="hljs-keyword">var</span> employeeObject = <span class="hljs-keyword">new</span> <span class="hljs-title class_">Employee</span>();
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(employeeObject.<span class="hljs-property">name</span>); <span class="hljs-comment">// John</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
255

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#255-What-is-a-constructor-method

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
