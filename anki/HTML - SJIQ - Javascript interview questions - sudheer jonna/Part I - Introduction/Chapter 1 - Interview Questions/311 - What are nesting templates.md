==================== Question ====================  

### What are nesting templates  

==================== Answer ====================  

The nesting template is a feature supported within template literals syntax to allow inner backticks inside a placeholder ${ } within the template. For example, the below nesting template is used to display the icons based on user permissions whereas outer template checks for platform type,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> iconStyles = <span class="hljs-string">`icon <span class="hljs-subst">${isMobilePlatform() ? <span class="hljs-string">''</span> : <span class="hljs-string">`icon-<span class="hljs-subst">${user.isAuthorized ? <span class="hljs-string">'submit'</span> : <span class="hljs-string">'disabled'</span>}</span>`</span>}</span>`</span>;
</code></pre>
<!-- codeblock-end -->

You can write the above use case without nesting template features as well. However, the nesting template feature is more compact and readable.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-comment">//Without nesting templates</span>
<span class="hljs-keyword">const</span> iconStyles = <span class="hljs-string">`icon <span class="hljs-subst">${
  isMobilePlatform() ? <span class="hljs-string">''</span>
  : user.isAuthorized ? <span class="hljs-string">'icon-submit'</span>
  : <span class="hljs-string">'icon-disabled'</span>
}</span>`</span>;
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
311

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#311-What-are-nesting-templates

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
