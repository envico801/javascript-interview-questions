==================== Question ====================  

### How do you generate random integers  

==================== Answer ====================  

You can use Math.random() with Math.floor() to return random integers. For example, if you want generate random integers between 1 to 10, the multiplication factor should be 10,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-title class_">Math</span>.<span class="hljs-title function_">floor</span>(<span class="hljs-title class_">Math</span>.<span class="hljs-title function_">random</span>() * <span class="hljs-number">10</span>) + <span class="hljs-number">1</span>; <span class="hljs-comment">// returns a random integer from 1 to 10</span>
<span class="hljs-title class_">Math</span>.<span class="hljs-title function_">floor</span>(<span class="hljs-title class_">Math</span>.<span class="hljs-title function_">random</span>() * <span class="hljs-number">100</span>) + <span class="hljs-number">1</span>; <span class="hljs-comment">// returns a random integer from 1 to 100</span>
</code></pre>
<!-- codeblock-end -->

**Note:** Math.random() returns a random number between 0 (inclusive), and 1 (exclusive)

==================== Id ====================  
149

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#149-How-do-you-generate-random-integers

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
