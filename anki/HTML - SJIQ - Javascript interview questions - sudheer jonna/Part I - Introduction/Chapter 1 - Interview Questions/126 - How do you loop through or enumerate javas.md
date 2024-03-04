==================== Question ====================  

### How do you loop through or enumerate javascript object  

==================== Answer ====================  

You can use the `for-in` loop to loop through javascript object. You can also make sure that the key you get is an actual property of an object, and doesn't come from the prototype using `hasOwnProperty` method.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> object = {
  <span class="hljs-attr">k1</span>: <span class="hljs-string">'value1'</span>,
  <span class="hljs-attr">k2</span>: <span class="hljs-string">'value2'</span>,
  <span class="hljs-attr">k3</span>: <span class="hljs-string">'value3'</span>,
};
<span class="hljs-keyword">for</span> (<span class="hljs-keyword">var</span> key <span class="hljs-keyword">in</span> object) {
  <span class="hljs-keyword">if</span> (object.<span class="hljs-title function_">hasOwnProperty</span>(key)) {
     <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(key + <span class="hljs-string">' -> '</span> + object[key]); <span class="hljs-comment">// k1 -> value1 ...</span>
  }
}
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
126

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#126-How-do-you-loop-through-or-enumerate-javas

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
