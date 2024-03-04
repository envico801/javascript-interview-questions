==================== Question ====================  

### What is an event delegation  

==================== Answer ====================  

Event delegation is a technique for listening to events where you delegate a parent element as the listener for all of the events that happen inside it.

For example, if you wanted to detect field changes in inside a specific form, you can use event delegation technique,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> form = <span class="hljs-variable language_">document</span>.<span class="hljs-title function_">querySelector</span>(<span class="hljs-string">'#registration-form'</span>);
<span class="hljs-comment">// Listen for changes to fields inside the form</span>
form.<span class="hljs-title function_">addEventListener</span>(
  <span class="hljs-string">'input'</span>,
  <span class="hljs-keyword">function</span> (<span class="hljs-params">event</span>) {
     <span class="hljs-comment">// Log the field that was changed</span>
     <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(event.<span class="hljs-property">target</span>);
  },
  <span class="hljs-literal">false</span>,
);
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
109

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#109-What-is-an-event-delegation

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
