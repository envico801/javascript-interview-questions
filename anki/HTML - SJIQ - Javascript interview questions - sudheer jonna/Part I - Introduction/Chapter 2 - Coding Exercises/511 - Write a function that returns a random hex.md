==================== Question ====================  

### Write a function that returns a random HEX color  

==================== Answer ====================  

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> <span class="hljs-variable constant_">HEX_ALPHABET</span> = [<span class="hljs-string">'0'</span>, <span class="hljs-string">'1'</span>, <span class="hljs-string">'2'</span>, <span class="hljs-string">'3'</span>, <span class="hljs-string">'4'</span>, <span class="hljs-string">'5'</span>, <span class="hljs-string">'6'</span>, <span class="hljs-string">'7'</span>, <span class="hljs-string">'8'</span>, <span class="hljs-string">'9'</span>, <span class="hljs-string">'a'</span>, <span class="hljs-string">'b'</span>, <span class="hljs-string">'c'</span>, <span class="hljs-string">'d'</span>, <span class="hljs-string">'e'</span>, <span class="hljs-string">'f'</span>];
<span class="hljs-keyword">const</span> <span class="hljs-variable constant_">HEX_PREFIX</span> = <span class="hljs-string">'#'</span>;
<span class="hljs-keyword">const</span> <span class="hljs-variable constant_">HEX_LENGTH</span> = <span class="hljs-number">6</span>;
<span class="hljs-keyword">function</span> <span class="hljs-title function_">generateRandomHex</span>(<span class="hljs-params"></span>) {
  <span class="hljs-keyword">let</span> randomHex = <span class="hljs-string">''</span>;
  <span class="hljs-keyword">for</span> (<span class="hljs-keyword">let</span> i = <span class="hljs-number">0</span>; i &#x3C; <span class="hljs-variable constant_">HEX_LENGTH</span>; i++) {
     <span class="hljs-keyword">const</span> randomIndex = <span class="hljs-title class_">Math</span>.<span class="hljs-title function_">floor</span>(<span class="hljs-title class_">Math</span>.<span class="hljs-title function_">random</span>() * <span class="hljs-variable constant_">HEX_ALPHABET</span>.<span class="hljs-property">length</span>);
     randomHex += <span class="hljs-variable constant_">HEX_ALPHABET</span>[randomIndex];
  }
  <span class="hljs-keyword">return</span> <span class="hljs-variable constant_">HEX_PREFIX</span> + randomHex;
}
</code></pre>
<!-- codeblock-end -->

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> <span class="hljs-variable constant_">HEX_PREFIX</span> = <span class="hljs-string">'#'</span>;
<span class="hljs-keyword">const</span> <span class="hljs-variable constant_">HEX_RADIX</span> = <span class="hljs-number">16</span>;
<span class="hljs-keyword">const</span> <span class="hljs-variable constant_">HEX_LENGTH</span> = <span class="hljs-number">6</span>;
<span class="hljs-keyword">function</span> <span class="hljs-title function_">generateRandomHex</span>(<span class="hljs-params"></span>) {
  <span class="hljs-keyword">return</span> (
     <span class="hljs-variable constant_">HEX_PREFIX</span> +
     <span class="hljs-title class_">Math</span>.<span class="hljs-title function_">floor</span>(<span class="hljs-title class_">Math</span>.<span class="hljs-title function_">random</span>() * <span class="hljs-number">0xffffff</span>)
       .<span class="hljs-title function_">toString</span>(<span class="hljs-variable constant_">HEX_RADIX</span>)
       .<span class="hljs-title function_">padStart</span>(<span class="hljs-variable constant_">HEX_LENGTH</span>, <span class="hljs-string">'0'</span>)
  );
}
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
511

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#511-Write-a-function-that-returns-a-random-hex

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
