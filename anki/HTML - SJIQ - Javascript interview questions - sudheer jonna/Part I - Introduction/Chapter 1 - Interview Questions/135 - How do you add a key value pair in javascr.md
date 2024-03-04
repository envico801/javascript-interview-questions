==================== Question ====================  

### How do you add a key value pair in javascript  

==================== Answer ====================  

There are two possible solutions to add new properties to an object. Let's take a simple object to explain these solutions.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> object = {
  <span class="hljs-attr">key1</span>: value1,
  <span class="hljs-attr">key2</span>: value2,
};
</code></pre>
<!-- codeblock-end -->

1. **Using dot notation:** This solution is useful when you know the name of the property

<!-- codeblock-start -->
<pre><code class="hljs language-javascript">object.<span class="hljs-property">key3</span> = <span class="hljs-string">'value3'</span>;
</code></pre>
<!-- codeblock-end -->

1. **Using square bracket notation:** This solution is useful when the name of the property is dynamically determined.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript">obj[<span class="hljs-string">'key3'</span>] = <span class="hljs-string">'value3'</span>;
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
135

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#135-How-do-you-add-a-key-value-pair-in-javascr

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
