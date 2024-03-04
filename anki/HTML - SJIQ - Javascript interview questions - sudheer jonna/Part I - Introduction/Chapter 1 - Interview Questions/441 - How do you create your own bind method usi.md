==================== Question ====================  

### How do you create your own bind method using either call or apply method?  

==================== Answer ====================  

The custom bind function needs to be created on Function prototype inorder to use it as other builtin functions. This custom function should return a function similar to original bind method and the implementation of inner function needs to use apply method call.

The function which is going to bind using custom `myOwnBind` method act as the attached function(`boundTargetFunction`) and argument as the object for `apply` method call.

<!-- codeblock-start -->
<pre><code class="hljs language-js"><span class="hljs-title class_">Function</span>.<span class="hljs-property"><span class="hljs-keyword">prototype</span></span>.<span class="hljs-property">myOwnBind</span> = <span class="hljs-keyword">function</span> (<span class="hljs-params">whoIsCallingMe</span>) {
  <span class="hljs-keyword">if</span> (<span class="hljs-keyword">typeof</span> <span class="hljs-variable language_">this</span> !== <span class="hljs-string">'function'</span>) {
     <span class="hljs-keyword">throw</span> <span class="hljs-keyword">new</span> <span class="hljs-title class_">Error</span>(<span class="hljs-variable language_">this</span> + <span class="hljs-string">"cannot be bound as it's not callable"</span>);
  }
  <span class="hljs-keyword">const</span> boundTargetFunction = <span class="hljs-variable language_">this</span>;
  <span class="hljs-keyword">return</span> <span class="hljs-keyword">function</span> (<span class="hljs-params"></span>) {
     boundTargetFunction.<span class="hljs-title function_">apply</span>(whoIsCallingMe, <span class="hljs-variable language_">arguments</span>);
  };
};
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
441

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#441-How-do-you-create-your-own-bind-method-usi

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
