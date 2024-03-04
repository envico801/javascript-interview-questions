==================== Question ====================  

### How do you create custom HTML element?  

==================== Answer ====================  

The creation of custom HTML elements involves two main steps,

1. **Define your custom HTML element:** First you need to define some custom class by extending HTMLElement class.

    After that define your component properties (styles,text etc) using `connectedCallback` method.

    **Note:** The browser exposes a function called `customElements.define` inorder to reuse the element.

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
    <span class="hljs-keyword">class</span> <span class="hljs-title class_">CustomElement</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">HTMLElement</span> {
      <span class="hljs-title function_">connectedCallback</span>(<span class="hljs-params"></span>) {
        <span class="hljs-variable language_">this</span>.<span class="hljs-property">innerHTML</span> = <span class="hljs-string">'This is a custom element'</span>;
      }
    }
    customElements.<span class="hljs-title function_">define</span>(<span class="hljs-string">'custom-element'</span>, <span class="hljs-title class_">CustomElement</span>);
    </code></pre>
    <!-- codeblock-end -->

2. **Use custome element just like other HTML element:** Declare your custom element as a HTML tag.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript">   &#x3C;body>
         &#x3C;custom-element>
    &#x3C;/body>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
431

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#431-How-do-you-create-custom-html-element

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
