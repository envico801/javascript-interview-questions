==================== Question ====================  

### How do you check whether a string contains a substring  

==================== Answer ====================  

There are 3 possible ways to check whether a string contains a substring or not,

1. **Using includes:** ES6 provided `String.prototype.includes` method to test a string contains a substring

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> mainString = <span class="hljs-string">'hello'</span>,
  subString = <span class="hljs-string">'hell'</span>;
mainString.<span class="hljs-title function_">includes</span>(subString);
</code></pre>
<!-- codeblock-end -->

1. **Using indexOf:** In an ES5 or older environment, you can use `String.prototype.indexOf` which returns the index of a substring. If the index value is not equal to -1 then it means the substring exists in the main string.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> mainString = <span class="hljs-string">'hello'</span>,
  subString = <span class="hljs-string">'hell'</span>;
mainString.<span class="hljs-title function_">indexOf</span>(subString) !== -<span class="hljs-number">1</span>;
</code></pre>
<!-- codeblock-end -->

1. **Using RegEx:** The advanced solution is using Regular expression's test method(`RegExp.test`), which allows for testing for against regular expressions

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> mainString = <span class="hljs-string">'hello'</span>,
  regex = <span class="hljs-regexp">/hell/</span>;
regex.<span class="hljs-title function_">test</span>(mainString);
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
120

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#120-How-do-you-check-whether-a-string-contains

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
