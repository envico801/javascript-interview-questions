==================== Question ====================  

### How do you remove falsy values from an array  

==================== Answer ====================  

You can apply the filter method on the array by passing Boolean as a parameter. This way it removes all falsy values(0, undefined, null, false and "") from the array.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> myArray = [<span class="hljs-literal">false</span>, <span class="hljs-literal">null</span>, <span class="hljs-number">1</span>, <span class="hljs-number">5</span>, <span class="hljs-literal">undefined</span>];
myArray.<span class="hljs-title function_">filter</span>(<span class="hljs-title class_">Boolean</span>); <span class="hljs-comment">// [1, 5] // is same as myArray.filter(x => x);</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
360

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#360-How-do-you-remove-falsy-values-from-an-arr

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
