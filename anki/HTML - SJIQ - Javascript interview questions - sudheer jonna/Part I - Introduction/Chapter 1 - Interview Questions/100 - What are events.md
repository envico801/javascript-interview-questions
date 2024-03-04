==================== Question ====================  

### What are events  

==================== Answer ====================  

Events are "things" that happen to HTML elements. When JavaScript is used in HTML pages, JavaScript can `react` on these events. Some of the examples of HTML events are,

1. Web page has finished loading

2. Input field was changed

3. Button was clicked

Let's describe the behavior of click event for button element,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript">&#x3C;!doctype html>
<span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">html</span>></span>
 <span class="hljs-tag">&#x3C;<span class="hljs-name">head</span>></span>
    <span class="hljs-tag">&#x3C;<span class="hljs-name">script</span>></span><span class="javascript">
      <span class="hljs-keyword">function</span> <span class="hljs-title function_">greeting</span>(<span class="hljs-params"></span>) {
        <span class="hljs-title function_">alert</span>(<span class="hljs-string">'Hello! Good morning'</span>);
      }
    </span><span class="hljs-tag">&#x3C;/<span class="hljs-name">script</span>></span>
 <span class="hljs-tag">&#x3C;/<span class="hljs-name">head</span>></span>
 <span class="hljs-tag">&#x3C;<span class="hljs-name">body</span>></span>
    <span class="hljs-tag">&#x3C;<span class="hljs-name">button</span> <span class="hljs-attr">type</span>=<span class="hljs-string">"button"</span> <span class="hljs-attr">onclick</span>=<span class="hljs-string">"greeting()"</span>></span>Click me<span class="hljs-tag">&#x3C;/<span class="hljs-name">button</span>></span>
 <span class="hljs-tag">&#x3C;/<span class="hljs-name">body</span>></span>
<span class="hljs-tag">&#x3C;/<span class="hljs-name">html</span>></span></span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
100

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#100-What-are-events

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
