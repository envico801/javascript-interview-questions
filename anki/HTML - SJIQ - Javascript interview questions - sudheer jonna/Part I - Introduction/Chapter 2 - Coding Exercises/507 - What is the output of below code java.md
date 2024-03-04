==================== Question ====================  

### What is the output of below code ?

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">let</span> arr = [<span class="hljs-number">1</span>, <span class="hljs-number">2</span>, <span class="hljs-number">3</span>];
<span class="hljs-keyword">let</span> str = <span class="hljs-string">'1,2,3'</span>;
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(arr == str);
</code></pre>
<!-- codeblock-end -->

- 1: false

- 2: Error

- 3: true  

==================== Answer ====================  

Answer: 3

Arrays have their own implementation of `toString` method that returns a comma-separated list of elements. So the above code snippet returns true. In order to avoid conversion of array type, we should use === for comparison.

==================== Id ====================  
507

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#507-What-is-the-output-of-below-code-java

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
