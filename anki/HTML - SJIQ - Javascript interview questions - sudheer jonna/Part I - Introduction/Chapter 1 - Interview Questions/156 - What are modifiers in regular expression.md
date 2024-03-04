==================== Question ====================  

### What are modifiers in regular expression  

==================== Answer ====================  

Modifiers can be used to perform case-insensitive and global searches. Let's list down some of the modifiers,

| Modifier | Description                                             |
| -------- | ------------------------------------------------------- |
| i        | Perform case-insensitive matching                       |
| g        | Perform a global match rather than stops at first match |
| m        | Perform multiline matching                              |

Let's take an example of global modifier,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> text = <span class="hljs-string">'Learn JS one by one'</span>;
<span class="hljs-keyword">var</span> pattern = <span class="hljs-regexp">/one/g</span>;
<span class="hljs-keyword">var</span> result = text.<span class="hljs-title function_">match</span>(pattern); <span class="hljs-comment">// one,one</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
156

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#156-What-are-modifiers-in-regular-expression

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
