==================== Question ====================  

### What is a decorator  

==================== Answer ====================  

A decorator is an expression that evaluates to a function and that takes the target, name, and decorator descriptor as arguments. Also, it optionally returns a decorator descriptor to install on the target object. Let's define admin decorator for user class at design time,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">admin</span>(<span class="hljs-params">isAdmin</span>) {
    <span class="hljs-keyword">return</span> <span class="hljs-keyword">function</span>(<span class="hljs-params">target</span>) {
        target.<span class="hljs-property">isAdmin</span> = isAdmin;
    }
}
@<span class="hljs-title function_">admin</span>(<span class="hljs-literal">true</span>)
<span class="hljs-keyword">class</span> <span class="hljs-title class_">User</span>() {
}
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-title class_">User</span>.<span class="hljs-property">isAdmin</span>); <span class="hljs-comment">//true</span>
 @<span class="hljs-title function_">admin</span>(<span class="hljs-literal">false</span>)
 <span class="hljs-keyword">class</span> <span class="hljs-title class_">User</span>() {
 }
 <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-title class_">User</span>.<span class="hljs-property">isAdmin</span>); <span class="hljs-comment">//false</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
239

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#239-What-is-a-decorator

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
