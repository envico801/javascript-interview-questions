==================== Question ====================  

### What happens if you write constructor more than once in a class  

==================== Answer ====================  

The "constructor" in a class is a special method and it should be defined only once in a class. i.e, If you write a constructor method more than once in a class it will throw a `SyntaxError` error.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"> <span class="hljs-keyword">class</span> <span class="hljs-title class_">Employee</span> {
    <span class="hljs-title function_">constructor</span>(<span class="hljs-params"></span>) {
      <span class="hljs-variable language_">this</span>.<span class="hljs-property">name</span> = <span class="hljs-string">"John"</span>;
    }
    <span class="hljs-title function_">constructor</span>(<span class="hljs-params"></span>) {   <span class="hljs-comment">//  Uncaught SyntaxError: A class may only have one constructor</span>
      <span class="hljs-variable language_">this</span>.<span class="hljs-property">age</span> = <span class="hljs-number">30</span>;
    }
 }
 <span class="hljs-keyword">var</span> employeeObject = <span class="hljs-keyword">new</span> <span class="hljs-title class_">Employee</span>();
 <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(employeeObject.<span class="hljs-property">name</span>);
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
256

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#256-What-happens-if-you-write-constructor-more

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
