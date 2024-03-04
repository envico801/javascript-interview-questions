==================== Question ====================  

### Give an example of a web worker  

==================== Answer ====================  

You need to follow below steps to start using web workers for counting example

1. Create a Web Worker File: You need to write a script to increment the count value. Let's name it as counter.js

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">let</span> i = <span class="hljs-number">0</span>;
<span class="hljs-keyword">function</span> <span class="hljs-title function_">timedCount</span>(<span class="hljs-params"></span>) {
  i = i + <span class="hljs-number">1</span>;
  <span class="hljs-title function_">postMessage</span>(i);
  <span class="hljs-built_in">setTimeout</span>(<span class="hljs-string">'timedCount()'</span>, <span class="hljs-number">500</span>);
}
<span class="hljs-title function_">timedCount</span>();
</code></pre>
<!-- codeblock-end -->

Here postMessage() method is used to post a message back to the HTML page

1. Create a Web Worker Object: You can create a web worker object by checking for browser support. Let's name this file as web_worker_example.js

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">if</span> (<span class="hljs-keyword">typeof</span> w == <span class="hljs-string">'undefined'</span>) {
  w = <span class="hljs-keyword">new</span> <span class="hljs-title class_">Worker</span>(<span class="hljs-string">'counter.js'</span>);
}
</code></pre>
<!-- codeblock-end -->

and we can receive messages from web worker

<!-- codeblock-start -->
<pre><code class="hljs language-javascript">w.<span class="hljs-property">onmessage</span> = <span class="hljs-keyword">function</span> (<span class="hljs-params">event</span>) {
  <span class="hljs-variable language_">document</span>.<span class="hljs-title function_">getElementById</span>(<span class="hljs-string">'message'</span>).<span class="hljs-property">innerHTML</span> = event.<span class="hljs-property">data</span>;
};
</code></pre>
<!-- codeblock-end -->

1. Terminate a Web Worker:

    Web workers will continue to listen for messages (even after the external script is finished) until it is terminated. You can use the terminate() method to terminate listening to the messages.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript">w.<span class="hljs-title function_">terminate</span>();
</code></pre>
<!-- codeblock-end -->

1. Reuse the Web Worker: If you set the worker variable to undefined you can reuse the code

<!-- codeblock-start -->
<pre><code class="hljs language-javascript">w = <span class="hljs-literal">undefined</span>;
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
49

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#49-Give-an-example-of-a-web-worker

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
