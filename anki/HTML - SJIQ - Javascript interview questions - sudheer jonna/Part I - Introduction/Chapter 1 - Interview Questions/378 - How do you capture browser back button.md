==================== Question ====================  

### How do you capture browser back button  

==================== Answer ====================  

The `beforeunload` event is triggered when the window, the document and its resources are about to be unloaded. This event is helpful to warn users about losing the current data and detect back button event.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-variable language_">window</span>.<span class="hljs-title function_">addEventListener</span>(<span class="hljs-string">'beforeunload'</span>, <span class="hljs-function">() =></span> {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'Clicked browser back button'</span>);
});
</code></pre>
<!-- codeblock-end -->

You can also use `popstate` event to detect the browser back button.

**Note:** The history entry has been activated using `history.pushState` method.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-variable language_">window</span>.<span class="hljs-title function_">addEventListener</span>(<span class="hljs-string">'popstate'</span>, <span class="hljs-function">() =></span> {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'Clicked browser back button'</span>);
  box.<span class="hljs-property">style</span>.<span class="hljs-property">backgroundColor</span> = <span class="hljs-string">'white'</span>;
});
<span class="hljs-keyword">const</span> box = <span class="hljs-variable language_">document</span>.<span class="hljs-title function_">getElementById</span>(<span class="hljs-string">'div'</span>);
box.<span class="hljs-title function_">addEventListener</span>(<span class="hljs-string">'click'</span>, <span class="hljs-function">() =></span> {
  box.<span class="hljs-property">style</span>.<span class="hljs-property">backgroundColor</span> = <span class="hljs-string">'blue'</span>;
  <span class="hljs-variable language_">window</span>.<span class="hljs-property">history</span>.<span class="hljs-title function_">pushState</span>({}, <span class="hljs-literal">null</span>, <span class="hljs-literal">null</span>);
});
</code></pre>
<!-- codeblock-end -->

In the preceeding code, When the box element clicked, its background color appears in blue color and changed to while color upon clicking the browser back button using `popstate` event handler. The `state` property of `popstate` contains the copy of history entry's state object.

==================== Id ====================  
378

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#378-How-do-you-capture-browser-back-button

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
