==================== Question ====================  

### How do you declare namespace  

==================== Answer ====================  

Even though JavaScript lacks namespaces, we can use Objects , IIFE to create namespaces.

1. **Using Object Literal Notation:** Let's wrap variables and functions inside an Object literal which acts as a namespace. After that you can access them using object notation

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> namespaceOne = {
    <span class="hljs-keyword">function</span> <span class="hljs-title function_">func1</span>(<span class="hljs-params"></span>) {
        <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">"This is a first definition"</span>);
    }
}
<span class="hljs-keyword">var</span> namespaceTwo = {
      <span class="hljs-keyword">function</span> <span class="hljs-title function_">func1</span>(<span class="hljs-params"></span>) {
          <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">"This is a second definition"</span>);
      }
 }
namespaceOne.<span class="hljs-title function_">func1</span>(); <span class="hljs-comment">// This is a first definition</span>
namespaceTwo.<span class="hljs-title function_">func1</span>(); <span class="hljs-comment">// This is a second definition</span>
</code></pre>
<!-- codeblock-end -->

1. **Using IIFE (Immediately invoked function expression):** The outer pair of parentheses of IIFE creates a local scope for all the code inside of it and makes the anonymous function a function expression. Due to that, you can create the same function in two different function expressions to act as a namespace.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript">(<span class="hljs-keyword">function</span> (<span class="hljs-params"></span>) {
  <span class="hljs-keyword">function</span> <span class="hljs-title function_">fun1</span>(<span class="hljs-params"></span>) {
     <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'This is a first definition'</span>);
  }
  <span class="hljs-title function_">fun1</span>();
})();
(<span class="hljs-keyword">function</span> (<span class="hljs-params"></span>) {
  <span class="hljs-keyword">function</span> <span class="hljs-title function_">fun1</span>(<span class="hljs-params"></span>) {
     <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'This is a second definition'</span>);
  }
  <span class="hljs-title function_">fun1</span>();
})();
</code></pre>
<!-- codeblock-end -->

1. **Using a block and a let/const declaration:** In ECMAScript 6, you can simply use a block and a let declaration to restrict the scope of a variable to a block.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript">{
  <span class="hljs-keyword">let</span> myFunction = <span class="hljs-keyword">function</span> <span class="hljs-title function_">fun1</span>(<span class="hljs-params"></span>) {
     <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'This is a first definition'</span>);
  };
  <span class="hljs-title function_">myFunction</span>();
}
<span class="hljs-comment">//myFunction(): ReferenceError: myFunction is not defined.</span>
{
  <span class="hljs-keyword">let</span> myFunction = <span class="hljs-keyword">function</span> <span class="hljs-title function_">fun1</span>(<span class="hljs-params"></span>) {
     <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'This is a second definition'</span>);
  };
  <span class="hljs-title function_">myFunction</span>();
}
<span class="hljs-comment">//myFunction(): ReferenceError: myFunction is not defined.</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
291

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#291-How-do-you-declare-namespace

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
