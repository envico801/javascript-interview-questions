==================== Question ====================  

### What is a higher order function  

==================== Answer ====================  

A higher-order function is a function that accepts another function as an argument or returns a function as a return value or both.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> <span class="hljs-title function_">firstOrderFunc</span> = (<span class="hljs-params"></span>) => <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'Hello, I am a First order function'</span>);
<span class="hljs-keyword">const</span> <span class="hljs-title function_">higherOrder</span> = (<span class="hljs-params">ReturnFirstOrderFunc</span>) => <span class="hljs-title class_">ReturnFirstOrderFunc</span>();
<span class="hljs-title function_">higherOrder</span>(firstOrderFunc);
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
13

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#13-What-is-a-higher-order-function

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
