==================== Question ====================  

### What are template literals  

==================== Answer ====================  

Template literals or template strings are string literals allowing embedded expressions. These are enclosed by the back-tick (`) character instead of double or single quotes.

In ES6, this feature enables using dynamic expressions as below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> greeting = <span class="hljs-string">`Welcome to JS World, Mr. <span class="hljs-subst">${firstName}</span> <span class="hljs-subst">${lastName}</span>.`</span>;
</code></pre>
<!-- codeblock-end -->

In ES5, you need break string like below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> greeting = <span class="hljs-string">'Welcome to JS World, Mr. '</span> + firstName + <span class="hljs-string">' '</span> + lastName.<span class="hljs-string">`

</span></code></pre>
<!-- codeblock-end -->

**Note:** You can use multi-line strings and string interpolation features with template literals.

==================== Id ====================  
309

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#309-What-are-template-literals

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
