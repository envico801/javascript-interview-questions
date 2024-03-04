==================== Question ====================  

### What are the differences between for...of and for...in statements  

==================== Answer ====================  

Both for...in and for...of statements iterate over js data structures. The only difference is over what they iterate:

1. for..in iterates over all enumerable property keys of an object

2. for..of iterates over the values of an iterable object.

Let's explain this difference with an example,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">let</span> arr = [<span class="hljs-string">'a'</span>, <span class="hljs-string">'b'</span>, <span class="hljs-string">'c'</span>];
arr.<span class="hljs-property">newProp</span> = <span class="hljs-string">'newVlue'</span>;
<span class="hljs-comment">// key are the property keys</span>
<span class="hljs-keyword">for</span> (<span class="hljs-keyword">let</span> key <span class="hljs-keyword">in</span> arr) {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(key); <span class="hljs-comment">// 0, 1, 2 &#x26; newValue</span>
}
<span class="hljs-comment">// value are the property values</span>
<span class="hljs-keyword">for</span> (<span class="hljs-keyword">let</span> value <span class="hljs-keyword">of</span> arr) {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(value); <span class="hljs-comment">// a, b, c</span>
}
</code></pre>
<!-- codeblock-end -->

Since for..in loop iterates over the keys of the object, the first loop logs 0, 1, 2 and newProp while iterating over the array object. The for..of loop iterates over the values of a arr data structure and logs a, b, c in the console.

==================== Id ====================  
418

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#418-What-are-the-differences-between-for-of

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
