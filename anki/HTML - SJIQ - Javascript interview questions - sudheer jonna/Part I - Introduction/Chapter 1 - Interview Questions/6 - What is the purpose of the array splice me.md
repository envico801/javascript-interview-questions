==================== Question ====================  

### What is the purpose of the array splice method  

==================== Answer ====================  

The **splice()** method adds/removes items to/from an array, and then returns the removed item. The first argument specifies the array position/index for insertion or deletion whereas the optional second argument indicates the number of elements to be deleted. Each additional argument is added to the array.

Some of the examples of this method are:

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">let</span> arrayIntegersOriginal1 = [<span class="hljs-number">1</span>, <span class="hljs-number">2</span>, <span class="hljs-number">3</span>, <span class="hljs-number">4</span>, <span class="hljs-number">5</span>];
<span class="hljs-keyword">let</span> arrayIntegersOriginal2 = [<span class="hljs-number">1</span>, <span class="hljs-number">2</span>, <span class="hljs-number">3</span>, <span class="hljs-number">4</span>, <span class="hljs-number">5</span>];
<span class="hljs-keyword">let</span> arrayIntegersOriginal3 = [<span class="hljs-number">1</span>, <span class="hljs-number">2</span>, <span class="hljs-number">3</span>, <span class="hljs-number">4</span>, <span class="hljs-number">5</span>];
<span class="hljs-keyword">let</span> arrayIntegers1 = arrayIntegersOriginal1.<span class="hljs-title function_">splice</span>(<span class="hljs-number">0</span>, <span class="hljs-number">2</span>); <span class="hljs-comment">// returns [1, 2]; original array: [3, 4, 5]</span>
<span class="hljs-keyword">let</span> arrayIntegers2 = arrayIntegersOriginal2.<span class="hljs-title function_">splice</span>(<span class="hljs-number">3</span>); <span class="hljs-comment">// returns [4, 5]; original array: [1, 2, 3]</span>
<span class="hljs-keyword">let</span> arrayIntegers3 = arrayIntegersOriginal3.<span class="hljs-title function_">splice</span>(<span class="hljs-number">3</span>, <span class="hljs-number">1</span>, <span class="hljs-string">'a'</span>, <span class="hljs-string">'b'</span>, <span class="hljs-string">'c'</span>); <span class="hljs-comment">//returns [4]; original array: [1, 2, 3, "a", "b", "c", 5]</span>
</code></pre>
<!-- codeblock-end -->

**Note:** Splice method modifies the original array and returns the deleted array.

==================== Id ====================  
6

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#6-What-is-the-purpose-of-the-array-splice-me

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
