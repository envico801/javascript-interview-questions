==================== Question ====================  

### What is the output of below code

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> myGenerator = (<span class="hljs-keyword">function</span>* () {
  <span class="hljs-keyword">yield</span> <span class="hljs-number">1</span>;
  <span class="hljs-keyword">yield</span> <span class="hljs-number">2</span>;
  <span class="hljs-keyword">yield</span> <span class="hljs-number">3</span>;
})();
<span class="hljs-keyword">for</span> (<span class="hljs-keyword">const</span> value <span class="hljs-keyword">of</span> myGenerator) {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(value);
  <span class="hljs-keyword">break</span>;
}
<span class="hljs-keyword">for</span> (<span class="hljs-keyword">const</span> value <span class="hljs-keyword">of</span> myGenerator) {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(value);
}
</code></pre>
<!-- codeblock-end -->

- 1: 1,2,3 and 1,2,3

- 2: 1,2,3 and 4,5,6

- 3: 1 and 1

- 4: 1  

==================== Answer ====================  

Answer: 4

The generator should not be re-used once the iterator is closed. i.e, Upon exiting a loop(on completion or using break & return), the generator is closed and trying to iterate over it again does not yield any more results. Hence, the second loop doesn't print any value.

==================== Id ====================  
495

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#495-What-is-the-output-of-below-code-javasc

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
