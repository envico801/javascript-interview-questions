==================== Question ====================  

### What is the purpose of clearInterval method  

==================== Answer ====================  

The clearInterval() function is used in javascript to clear the interval which has been set by setInterval() function. i.e, The return value returned by setInterval() function is stored in a variable and it’s passed into the clearInterval() function to clear the interval.

For example, the below setInterval method is used to display the message for every 3 seconds. This interval can be cleared by the clearInterval() method.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript">&#x3C;script>
<span class="hljs-keyword">var</span> msg;
<span class="hljs-keyword">function</span> <span class="hljs-title function_">greeting</span>(<span class="hljs-params"></span>) {
    <span class="hljs-title function_">alert</span>(<span class="hljs-string">'Good morning'</span>);
}
<span class="hljs-keyword">function</span> <span class="hljs-title function_">start</span>(<span class="hljs-params"></span>) {
  msg = <span class="hljs-built_in">setInterval</span>(greeting, <span class="hljs-number">3000</span>);
}
<span class="hljs-keyword">function</span> <span class="hljs-title function_">stop</span>(<span class="hljs-params"></span>) {
     <span class="hljs-built_in">clearInterval</span>(msg);
}
&#x3C;/script>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
118

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#118-What-is-the-purpose-of-clearinterval-metho

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
