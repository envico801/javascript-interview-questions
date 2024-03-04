==================== Question ====================  

### How do you load CSS and JS files dynamically  

==================== Answer ====================  

You can create both link and script elements in the DOM and append them as child to head tag. Let's create a function to add script and style resources as below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">loadAssets</span>(<span class="hljs-params">filename, filetype</span>) {
  <span class="hljs-keyword">if</span> (filetype == <span class="hljs-string">'css'</span>) {
     <span class="hljs-comment">// External CSS file</span>
     <span class="hljs-keyword">var</span> fileReference = <span class="hljs-variable language_">document</span>.<span class="hljs-title function_">createElement</span>(<span class="hljs-string">'link'</span>);
     fileReference.<span class="hljs-title function_">setAttribute</span>(<span class="hljs-string">'rel'</span>, <span class="hljs-string">'stylesheet'</span>);
     fileReference.<span class="hljs-title function_">setAttribute</span>(<span class="hljs-string">'type'</span>, <span class="hljs-string">'text/css'</span>);
     fileReference.<span class="hljs-title function_">setAttribute</span>(<span class="hljs-string">'href'</span>, filename);
  } <span class="hljs-keyword">else</span> <span class="hljs-keyword">if</span> (filetype == <span class="hljs-string">'js'</span>) {
     <span class="hljs-comment">// External JavaScript file</span>
     <span class="hljs-keyword">var</span> fileReference = <span class="hljs-variable language_">document</span>.<span class="hljs-title function_">createElement</span>(<span class="hljs-string">'script'</span>);
     fileReference.<span class="hljs-title function_">setAttribute</span>(<span class="hljs-string">'type'</span>, <span class="hljs-string">'text/javascript'</span>);
     fileReference.<span class="hljs-title function_">setAttribute</span>(<span class="hljs-string">'src'</span>, filename);
  }
  <span class="hljs-keyword">if</span> (<span class="hljs-keyword">typeof</span> fileReference != <span class="hljs-string">'undefined'</span>) <span class="hljs-variable language_">document</span>.<span class="hljs-title function_">getElementsByTagName</span>(<span class="hljs-string">'head'</span>)[<span class="hljs-number">0</span>].<span class="hljs-title function_">appendChild</span>(fileReference);
}
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
294

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#294-How-do-you-load-css-and-js-files-dynamical

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
