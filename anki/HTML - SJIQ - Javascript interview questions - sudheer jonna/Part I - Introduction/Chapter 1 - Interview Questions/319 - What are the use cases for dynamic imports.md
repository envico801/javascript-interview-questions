==================== Question ====================  

### What are the use cases for dynamic imports  

==================== Answer ====================  

Below are some of the use cases of using dynamic imports over static imports,

1. Import a module on-demand or conditionally. For example, if you want to load a polyfill on legacy browser

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">if</span> (<span class="hljs-title function_">isLegacyBrowser</span>()) {
     <span class="hljs-keyword">import</span>(···)
     .<span class="hljs-title function_">then</span>(···);
}
</code></pre>
<!-- codeblock-end -->

1. Compute the module specifier at runtime. For example, you can use it for internationalization.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">import</span>(<span class="hljs-string">`messages_<span class="hljs-subst">${getLocale()}</span>.js`</span>).<span class="hljs-title function_">then</span>(···);
</code></pre>
<!-- codeblock-end -->

1. Import a module from within a regular script instead a module.

==================== Id ====================  
319

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#319-What-are-the-use-cases-for-dynamic-imports

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
