==================== Question ====================  

### How do you receive server-sent event notifications  

==================== Answer ====================  

The EventSource object is used to receive server-sent event notifications. For example, you can receive messages from server as below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">if</span> (<span class="hljs-keyword">typeof</span> <span class="hljs-title class_">EventSource</span> !== <span class="hljs-string">'undefined'</span>) {
  <span class="hljs-keyword">var</span> source = <span class="hljs-keyword">new</span> <span class="hljs-title class_">EventSource</span>(<span class="hljs-string">'sse_generator.js'</span>);
  source.<span class="hljs-property">onmessage</span> = <span class="hljs-keyword">function</span> (<span class="hljs-params">event</span>) {
     <span class="hljs-variable language_">document</span>.<span class="hljs-title function_">getElementById</span>(<span class="hljs-string">'output'</span>).<span class="hljs-property">innerHTML</span> += event.<span class="hljs-property">data</span> + <span class="hljs-string">'&#x3C;br>'</span>;
  };
}
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
58

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#58-How-do-you-receive-server-sent-event-notif

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
