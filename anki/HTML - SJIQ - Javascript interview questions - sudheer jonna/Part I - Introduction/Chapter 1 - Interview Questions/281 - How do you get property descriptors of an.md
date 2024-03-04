==================== Question ====================  

### How do you get property descriptors of an object  

==================== Answer ====================  

You can use the `Object.getOwnPropertyDescriptors()` method which returns all own property descriptors of a given object. The example usage of this method is below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> newObject = {
  <span class="hljs-attr">a</span>: <span class="hljs-number">1</span>,
  <span class="hljs-attr">b</span>: <span class="hljs-number">2</span>,
  <span class="hljs-attr">c</span>: <span class="hljs-number">3</span>,
};
<span class="hljs-keyword">const</span> descriptorsObject = <span class="hljs-title class_">Object</span>.<span class="hljs-title function_">getOwnPropertyDescriptors</span>(newObject);
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(descriptorsObject.<span class="hljs-property">a</span>.<span class="hljs-property">writable</span>); <span class="hljs-comment">//true</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(descriptorsObject.<span class="hljs-property">a</span>.<span class="hljs-property">configurable</span>); <span class="hljs-comment">//true</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(descriptorsObject.<span class="hljs-property">a</span>.<span class="hljs-property">enumerable</span>); <span class="hljs-comment">//true</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(descriptorsObject.<span class="hljs-property">a</span>.<span class="hljs-property">value</span>); <span class="hljs-comment">// 1</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
281

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#281-How-do-you-get-property-descriptors-of-an

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
