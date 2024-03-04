==================== Question ====================  

### How do you avoid receiving postMessages from attackers  

==================== Answer ====================  

Since the listener listens for any message, an attacker can trick the application by sending a message from the attacker’s origin, which gives an impression that the receiver received the message from the actual sender’s window. You can avoid this issue by validating the origin of the message on the receiver's end using the “message.origin” attribute. For examples, let's check the sender's origin [http://www.some-sender.com](http://www.some-sender.com) on receiver side [www.some-receiver.com](www.some-receiver.com),

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-comment">//Listener on http://www.some-receiver.com/</span>
<span class="hljs-variable language_">window</span>.<span class="hljs-title function_">addEventListener</span>(<span class="hljs-string">"message"</span>, <span class="hljs-keyword">function</span>(<span class="hljs-params">message</span>){
     <span class="hljs-keyword">if</span>(<span class="hljs-regexp">/^http:/</span><span class="hljs-regexp">/www\.some-sender\.com$/</span>.<span class="hljs-title function_">test</span>(message.<span class="hljs-property">origin</span>)){
          <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'You received the data from valid sender'</span>, message.<span class="hljs-property">data</span>);
    }
});
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
327

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#327-How-do-you-avoid-receiving-postmessages-fr

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
