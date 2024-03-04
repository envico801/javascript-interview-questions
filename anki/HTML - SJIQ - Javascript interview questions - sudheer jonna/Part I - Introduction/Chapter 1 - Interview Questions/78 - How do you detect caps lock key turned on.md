==================== Question ====================  

### How do you detect caps lock key turned on or not  

==================== Answer ====================  

The `mouseEvent getModifierState()` is used to return a boolean value that indicates whether the specified modifier key is activated or not. The modifiers such as CapsLock, ScrollLock and NumLock are activated when they are clicked, and deactivated when they are clicked again.

Let's take an input element to detect the CapsLock on/off behavior with an example,

<!-- codeblock-start -->
<pre><code class="hljs language-html"><span class="hljs-tag">&#x3C;<span class="hljs-name">input</span> <span class="hljs-attr">type</span>=<span class="hljs-string">"password"</span> <span class="hljs-attr">onmousedown</span>=<span class="hljs-string">"enterInput(event)"</span> /></span>
<span class="hljs-tag">&#x3C;<span class="hljs-name">p</span> <span class="hljs-attr">id</span>=<span class="hljs-string">"feedback"</span>></span><span class="hljs-tag">&#x3C;/<span class="hljs-name">p</span>></span>
<span class="hljs-tag">&#x3C;<span class="hljs-name">script</span>></span><span class="javascript">
  <span class="hljs-keyword">function</span> <span class="hljs-title function_">enterInput</span>(<span class="hljs-params">e</span>) {
     <span class="hljs-keyword">var</span> flag = e.<span class="hljs-title function_">getModifierState</span>(<span class="hljs-string">'CapsLock'</span>);
     <span class="hljs-keyword">if</span> (flag) {
       <span class="hljs-variable language_">document</span>.<span class="hljs-title function_">getElementById</span>(<span class="hljs-string">'feedback'</span>).<span class="hljs-property">innerHTML</span> = <span class="hljs-string">'CapsLock activated'</span>;
     } <span class="hljs-keyword">else</span> {
       <span class="hljs-variable language_">document</span>.<span class="hljs-title function_">getElementById</span>(<span class="hljs-string">'feedback'</span>).<span class="hljs-property">innerHTML</span> = <span class="hljs-string">'CapsLock not activated'</span>;
     }
  }
</span><span class="hljs-tag">&#x3C;/<span class="hljs-name">script</span>></span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
78

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#78-How-do-you-detect-caps-lock-key-turned-on

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
