==================== Question ====================  

### What is a storage event and its event handler  

==================== Answer ====================  

The StorageEvent is an event that fires when a storage area has been changed in the context of another document. Whereas onstorage property is an EventHandler for processing storage events.

The syntax would be as below

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-variable language_">window</span>.<span class="hljs-property">onstorage</span> = functionRef;
</code></pre>
<!-- codeblock-end -->

Let's take the example usage of onstorage event handler which logs the storage key and it's values

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-variable language_">window</span>.<span class="hljs-property">onstorage</span> = <span class="hljs-keyword">function</span> (<span class="hljs-params">e</span>) {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'The '</span> + e.<span class="hljs-property">key</span> + <span class="hljs-string">' key has been changed from '</span> + e.<span class="hljs-property">oldValue</span> + <span class="hljs-string">' to '</span> + e.<span class="hljs-property">newValue</span> + <span class="hljs-string">'.'</span>);
};
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
45

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#45-What-is-a-storage-event-and-its-event-hand

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
