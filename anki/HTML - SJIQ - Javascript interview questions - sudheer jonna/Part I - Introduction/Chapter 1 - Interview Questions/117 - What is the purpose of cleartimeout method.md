==================== Question ====================  

### What is the purpose of clearTimeout method  

==================== Answer ====================  

The clearTimeout() function is used in javascript to clear the timeout which has been set by setTimeout()function before that. i.e, The return value of setTimeout() function is stored in a variable and it’s passed into the clearTimeout() function to clear the timer.

For example, the below setTimeout method is used to display the message after 3 seconds. This timeout can be cleared by the clearTimeout() method.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript">&#x3C;script>
<span class="hljs-keyword">var</span> msg;
<span class="hljs-keyword">function</span> <span class="hljs-title function_">greeting</span>(<span class="hljs-params"></span>) {
    <span class="hljs-title function_">alert</span>(<span class="hljs-string">'Good morning'</span>);
}
<span class="hljs-keyword">function</span> <span class="hljs-title function_">start</span>(<span class="hljs-params"></span>) {
  msg =<span class="hljs-built_in">setTimeout</span>(greeting, <span class="hljs-number">3000</span>);
}
<span class="hljs-keyword">function</span> <span class="hljs-title function_">stop</span>(<span class="hljs-params"></span>) {
     <span class="hljs-built_in">clearTimeout</span>(msg);
}
&#x3C;/script>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
117

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#117-What-is-the-purpose-of-cleartimeout-method

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
