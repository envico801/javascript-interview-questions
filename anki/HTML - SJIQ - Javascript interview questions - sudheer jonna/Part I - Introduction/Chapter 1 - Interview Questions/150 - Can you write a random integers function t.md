==================== Question ====================  

### Can you write a random integers function to print integers with in a range  

==================== Answer ====================  

Yes, you can create a proper random function to return a random number between min and max (both included)

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">randomInteger</span>(<span class="hljs-params">min, max</span>) {
  <span class="hljs-keyword">return</span> <span class="hljs-title class_">Math</span>.<span class="hljs-title function_">floor</span>(<span class="hljs-title class_">Math</span>.<span class="hljs-title function_">random</span>() * (max - min + <span class="hljs-number">1</span>)) + min;
}
<span class="hljs-title function_">randomInteger</span>(<span class="hljs-number">1</span>, <span class="hljs-number">100</span>); <span class="hljs-comment">// returns a random integer from 1 to 100</span>
<span class="hljs-title function_">randomInteger</span>(<span class="hljs-number">1</span>, <span class="hljs-number">1000</span>); <span class="hljs-comment">// returns a random integer from 1 to 1000</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
150

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#150-Can-you-write-a-random-integers-function-t

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
