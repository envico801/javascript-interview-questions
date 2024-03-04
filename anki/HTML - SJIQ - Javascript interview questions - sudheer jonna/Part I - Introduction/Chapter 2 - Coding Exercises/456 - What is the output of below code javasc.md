==================== Question ====================  

### What is the output of below code

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> myChars = [<span class="hljs-string">'a'</span>, <span class="hljs-string">'b'</span>, <span class="hljs-string">'c'</span>, <span class="hljs-string">'d'</span>];
<span class="hljs-keyword">delete</span> myChars[<span class="hljs-number">0</span>];
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(myChars);
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(myChars[<span class="hljs-number">0</span>]);
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(myChars.<span class="hljs-property">length</span>);
</code></pre>
<!-- codeblock-end -->

- 1: [empty, 'b', 'c', 'd'], empty, 3

- 2: [null, 'b', 'c', 'd'], empty, 3

- 3: [empty, 'b', 'c', 'd'], undefined, 4

- 4: [null, 'b', 'c', 'd'], undefined, 4  

==================== Answer ====================  

Answer: 3

The `delete` operator will delete the object property but it will not reindex the array or change its length. So the number or elements or length of the array won't be changed.

If you try to print myChars then you can observe that it doesn't set an undefined value, rather the property is removed from the array. The newer versions of Chrome use `empty` instead of `undefined` to make the difference a bit clearer.

==================== Id ====================  
456

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#456-What-is-the-output-of-below-code-javasc

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
