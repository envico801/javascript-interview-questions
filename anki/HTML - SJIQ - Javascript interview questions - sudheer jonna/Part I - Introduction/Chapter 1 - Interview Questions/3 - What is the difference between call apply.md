==================== Question ====================  

### What is the difference between Call, Apply and Bind  

==================== Answer ====================  

The difference between Call, Apply and Bind can be explained with below examples,

**Call:** The call() method invokes a function with a given `this` value and arguments provided one by one

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> employee1 = { <span class="hljs-attr">firstName</span>: <span class="hljs-string">'John'</span>, <span class="hljs-attr">lastName</span>: <span class="hljs-string">'Rodson'</span> };
<span class="hljs-keyword">var</span> employee2 = { <span class="hljs-attr">firstName</span>: <span class="hljs-string">'Jimmy'</span>, <span class="hljs-attr">lastName</span>: <span class="hljs-string">'Baily'</span> };
<span class="hljs-keyword">function</span> <span class="hljs-title function_">invite</span>(<span class="hljs-params">greeting1, greeting2</span>) {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(greeting1 + <span class="hljs-string">' '</span> + <span class="hljs-variable language_">this</span>.<span class="hljs-property">firstName</span> + <span class="hljs-string">' '</span> + <span class="hljs-variable language_">this</span>.<span class="hljs-property">lastName</span> + <span class="hljs-string">', '</span> + greeting2);
}
invite.<span class="hljs-title function_">call</span>(employee1, <span class="hljs-string">'Hello'</span>, <span class="hljs-string">'How are you?'</span>); <span class="hljs-comment">// Hello John Rodson, How are you?</span>
invite.<span class="hljs-title function_">call</span>(employee2, <span class="hljs-string">'Hello'</span>, <span class="hljs-string">'How are you?'</span>); <span class="hljs-comment">// Hello Jimmy Baily, How are you?</span>
</code></pre>
<!-- codeblock-end -->

**Apply:** Invokes the function with a given `this` value and allows you to pass in arguments as an array

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> employee1 = { <span class="hljs-attr">firstName</span>: <span class="hljs-string">'John'</span>, <span class="hljs-attr">lastName</span>: <span class="hljs-string">'Rodson'</span> };
<span class="hljs-keyword">var</span> employee2 = { <span class="hljs-attr">firstName</span>: <span class="hljs-string">'Jimmy'</span>, <span class="hljs-attr">lastName</span>: <span class="hljs-string">'Baily'</span> };
<span class="hljs-keyword">function</span> <span class="hljs-title function_">invite</span>(<span class="hljs-params">greeting1, greeting2</span>) {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(greeting1 + <span class="hljs-string">' '</span> + <span class="hljs-variable language_">this</span>.<span class="hljs-property">firstName</span> + <span class="hljs-string">' '</span> + <span class="hljs-variable language_">this</span>.<span class="hljs-property">lastName</span> + <span class="hljs-string">', '</span> + greeting2);
}
invite.<span class="hljs-title function_">apply</span>(employee1, [<span class="hljs-string">'Hello'</span>, <span class="hljs-string">'How are you?'</span>]); <span class="hljs-comment">// Hello John Rodson, How are you?</span>
invite.<span class="hljs-title function_">apply</span>(employee2, [<span class="hljs-string">'Hello'</span>, <span class="hljs-string">'How are you?'</span>]); <span class="hljs-comment">// Hello Jimmy Baily, How are you?</span>
</code></pre>
<!-- codeblock-end -->

**Bind:** returns a new function, allowing you to pass any number of arguments

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> employee1 = { <span class="hljs-attr">firstName</span>: <span class="hljs-string">'John'</span>, <span class="hljs-attr">lastName</span>: <span class="hljs-string">'Rodson'</span> };
<span class="hljs-keyword">var</span> employee2 = { <span class="hljs-attr">firstName</span>: <span class="hljs-string">'Jimmy'</span>, <span class="hljs-attr">lastName</span>: <span class="hljs-string">'Baily'</span> };
<span class="hljs-keyword">function</span> <span class="hljs-title function_">invite</span>(<span class="hljs-params">greeting1, greeting2</span>) {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(greeting1 + <span class="hljs-string">' '</span> + <span class="hljs-variable language_">this</span>.<span class="hljs-property">firstName</span> + <span class="hljs-string">' '</span> + <span class="hljs-variable language_">this</span>.<span class="hljs-property">lastName</span> + <span class="hljs-string">', '</span> + greeting2);
}
<span class="hljs-keyword">var</span> inviteEmployee1 = invite.<span class="hljs-title function_">bind</span>(employee1);
<span class="hljs-keyword">var</span> inviteEmployee2 = invite.<span class="hljs-title function_">bind</span>(employee2);
<span class="hljs-title function_">inviteEmployee1</span>(<span class="hljs-string">'Hello'</span>, <span class="hljs-string">'How are you?'</span>); <span class="hljs-comment">// Hello John Rodson, How are you?</span>
<span class="hljs-title function_">inviteEmployee2</span>(<span class="hljs-string">'Hello'</span>, <span class="hljs-string">'How are you?'</span>); <span class="hljs-comment">// Hello Jimmy Baily, How are you?</span>
</code></pre>
<!-- codeblock-end -->

Call and Apply are pretty much interchangeable. Both execute the current function immediately. You need to decide whether it’s easier to send in an array or a comma separated list of arguments. You can remember by treating Call is for **comma** (separated list) and Apply is for **Array**.

Bind creates a new function that will have `this` set to the first parameter passed to bind().

==================== Id ====================  
3

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#3-What-is-the-difference-between-call-apply

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
