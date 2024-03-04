==================== Question ====================  

### What is module pattern?  

==================== Answer ====================  

Module pattern is a designed pattern used to wrap a set of variables and functions together in a single scope returned as an object. JavaScript doesn't have access specifiers similar to other languages(Java, Python, etc) to provide private scope. It uses IIFE (Immediately invoked function expression) to allow for private scopes. i.e., a closure that protect variables and methods.

The module pattern looks like below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript">(<span class="hljs-keyword">function</span> (<span class="hljs-params"></span>) {
  <span class="hljs-comment">// Private variables or functions goes here.</span>
  <span class="hljs-keyword">return</span> {
     <span class="hljs-comment">// Return public variables or functions here.</span>
  };
})();
</code></pre>
<!-- codeblock-end -->

Let's see an example of a module pattern for an employee with private and public access,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> createEmployee = (<span class="hljs-keyword">function</span> (<span class="hljs-params"></span>) {
  <span class="hljs-comment">// Private</span>
  <span class="hljs-keyword">const</span> name = <span class="hljs-string">'John'</span>;
  <span class="hljs-keyword">const</span> department = <span class="hljs-string">'Sales'</span>;
  <span class="hljs-keyword">const</span> <span class="hljs-title function_">getEmployeeName</span> = (<span class="hljs-params"></span>) => name;
  <span class="hljs-keyword">const</span> <span class="hljs-title function_">getDepartmentName</span> = (<span class="hljs-params"></span>) => department;
  <span class="hljs-comment">// Public</span>
  <span class="hljs-keyword">return</span> {
     name,
     department,
     <span class="hljs-attr">getName</span>: <span class="hljs-function">() =></span> <span class="hljs-title function_">getEmployeeName</span>(),
     <span class="hljs-attr">getDepartment</span>: <span class="hljs-function">() =></span> <span class="hljs-title function_">getDepartmentName</span>(),
  };
})();
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(createEmployee.<span class="hljs-property">name</span>);
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(createEmployee.<span class="hljs-property">department</span>);
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(createEmployee.<span class="hljs-title function_">getName</span>());
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(createEmployee.<span class="hljs-title function_">getDepartment</span>());
</code></pre>
<!-- codeblock-end -->

**Note:** It mimic the concepts of classes with private variables and methods.

==================== Id ====================  
446

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#446-What-is-module-pattern

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
