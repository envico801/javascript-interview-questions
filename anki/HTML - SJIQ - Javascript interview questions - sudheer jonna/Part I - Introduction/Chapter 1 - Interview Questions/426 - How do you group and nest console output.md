==================== Question ====================  

### How do you group and nest console output?  

==================== Answer ====================  

The `console.group()` can be used to group related log messages to be able to easily read the logs and use console.groupEnd()to close the group. Along with this, you can also nest groups which allows to output message in hierarchical manner.

For example, if you’re logging a user’s details:

<!-- codeblock-start -->
<pre><code class="hljs language-js"><span class="hljs-variable language_">console</span>.<span class="hljs-title function_">group</span>(<span class="hljs-string">'User Details'</span>);
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'name: Sudheer Jonna'</span>);
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'job: Software Developer'</span>);
<span class="hljs-comment">// Nested Group</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">group</span>(<span class="hljs-string">'Address'</span>);
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'Street: Commonwealth'</span>);
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'City: Los Angeles'</span>);
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'State: California'</span>);
<span class="hljs-comment">// Close nested group</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">groupEnd</span>();
<span class="hljs-comment">// Close outer group</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">groupEnd</span>();
</code></pre>
<!-- codeblock-end -->

You can also use `console.groupCollapsed()` instead of `console.group()` if you want the groups to be collapsed by default.

==================== Id ====================  
426

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#426-How-do-you-group-and-nest-console-output

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
