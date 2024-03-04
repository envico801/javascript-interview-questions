==================== Question ====================  

### How to cancel a fetch request  

==================== Answer ====================  

Until a few days back, One shortcoming of native promises is no direct way to cancel a fetch request. But the new `AbortController` from js specification allows you to use a signal to abort one or multiple fetch calls.

The basic flow of cancelling a fetch request would be as below,

1. Create an `AbortController` instance

2. Get the signal property of an instance and pass the signal as a fetch option for signal

3. Call the AbortController's abort property to cancel all fetches that use that signal

    For example, let's pass the same signal to multiple fetch calls will cancel all requests with that signal,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> controller = <span class="hljs-keyword">new</span> <span class="hljs-title class_">AbortController</span>();
<span class="hljs-keyword">const</span> { signal } = controller;
<span class="hljs-title function_">fetch</span>(<span class="hljs-string">'http://localhost:8000'</span>, { signal })
  .<span class="hljs-title function_">then</span>(<span class="hljs-function">(<span class="hljs-params">response</span>) =></span> {
     <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">`Request 1 is complete!`</span>);
  })
  .<span class="hljs-title function_">catch</span>(<span class="hljs-function">(<span class="hljs-params">e</span>) =></span> {
     <span class="hljs-keyword">if</span> (e.<span class="hljs-property">name</span> === <span class="hljs-string">'AbortError'</span>) {
       <span class="hljs-comment">// We know it's been canceled!</span>
     }
  });
<span class="hljs-title function_">fetch</span>(<span class="hljs-string">'http://localhost:8000'</span>, { signal })
  .<span class="hljs-title function_">then</span>(<span class="hljs-function">(<span class="hljs-params">response</span>) =></span> {
     <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">`Request 2 is complete!`</span>);
  })
  .<span class="hljs-title function_">catch</span>(<span class="hljs-function">(<span class="hljs-params">e</span>) =></span> {
     <span class="hljs-keyword">if</span> (e.<span class="hljs-property">name</span> === <span class="hljs-string">'AbortError'</span>) {
       <span class="hljs-comment">// We know it's been canceled!</span>
     }
  });
<span class="hljs-comment">// Wait 2 seconds to abort both requests</span>
<span class="hljs-built_in">setTimeout</span>(<span class="hljs-function">() =></span> controller.<span class="hljs-title function_">abort</span>(), <span class="hljs-number">2000</span>);
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
383

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#383-How-to-cancel-a-fetch-request

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
