==================== Question ====================  

### What is the purpose of the array slice method  

==================== Answer ====================  

The **slice()** method returns the selected elements in an array as a new array object. It selects the elements starting at the given start argument, and ends at the given optional end argument without including the last element. If you omit the second argument then it selects till the end of the array.

Some of the examples of this method are,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">let</span> arrayIntegers = [<span class="hljs-number">1</span>, <span class="hljs-number">2</span>, <span class="hljs-number">3</span>, <span class="hljs-number">4</span>, <span class="hljs-number">5</span>];
<span class="hljs-keyword">let</span> arrayIntegers1 = arrayIntegers.<span class="hljs-title function_">slice</span>(<span class="hljs-number">0</span>, <span class="hljs-number">2</span>); <span class="hljs-comment">// returns [1,2]</span>
<span class="hljs-keyword">let</span> arrayIntegers2 = arrayIntegers.<span class="hljs-title function_">slice</span>(<span class="hljs-number">2</span>, <span class="hljs-number">3</span>); <span class="hljs-comment">// returns [3]</span>
<span class="hljs-keyword">let</span> arrayIntegers3 = arrayIntegers.<span class="hljs-title function_">slice</span>(<span class="hljs-number">4</span>); <span class="hljs-comment">//returns [5]</span>
</code></pre>
<!-- codeblock-end -->

**Note:** Slice method doesn't mutate the original array but it returns the subset as a new array.

==================== Id ====================  
5

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#5-What-is-the-purpose-of-the-array-slice-met

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
