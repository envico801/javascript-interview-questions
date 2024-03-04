==================== Question ====================  

### How do you copy properties from one object to other  

==================== Answer ====================  

You can use the Object.assign() method which is used to copy the values and properties from one or more source objects to a target object. It returns the target object which has properties and values copied from the source objects. The syntax would be as below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-title class_">Object</span>.<span class="hljs-title function_">assign</span>(target, ...sources);
</code></pre>
<!-- codeblock-end -->

Let's take example with one source and one target object,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> target = { <span class="hljs-attr">a</span>: <span class="hljs-number">1</span>, <span class="hljs-attr">b</span>: <span class="hljs-number">2</span> };
<span class="hljs-keyword">const</span> source = { <span class="hljs-attr">b</span>: <span class="hljs-number">3</span>, <span class="hljs-attr">c</span>: <span class="hljs-number">4</span> };
<span class="hljs-keyword">const</span> returnedTarget = <span class="hljs-title class_">Object</span>.<span class="hljs-title function_">assign</span>(target, source);
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(target); <span class="hljs-comment">// { a: 1, b: 3, c: 4 }</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(returnedTarget); <span class="hljs-comment">// { a: 1, b: 3, c: 4 }</span>
</code></pre>
<!-- codeblock-end -->

As observed in the above code, there is a common property(`b`) from source to target so it's value has been overwritten.

==================== Id ====================  
192

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#192-How-do-you-copy-properties-from-one-object

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
