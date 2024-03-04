==================== Question ====================  

### How do you reversing an array  

==================== Answer ====================  

You can use the reverse() method to reverse the elements in an array. This method is useful to sort an array in descending order. Let's see the usage of reverse() method in an example,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">let</span> numbers = [<span class="hljs-number">1</span>, <span class="hljs-number">2</span>, <span class="hljs-number">5</span>, <span class="hljs-number">3</span>, <span class="hljs-number">4</span>];
numbers.<span class="hljs-title function_">sort</span>(<span class="hljs-function">(<span class="hljs-params">a, b</span>) =></span> b - a);
numbers.<span class="hljs-title function_">reverse</span>();
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(numbers); <span class="hljs-comment">// [1, 2, 3, 4 ,5]</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
244

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#244-How-do-you-reversing-an-array

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
