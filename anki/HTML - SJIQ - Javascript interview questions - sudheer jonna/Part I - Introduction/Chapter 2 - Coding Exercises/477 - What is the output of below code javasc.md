==================== Question ====================  

### What is the output of below code

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> set = <span class="hljs-keyword">new</span> <span class="hljs-title class_">Set</span>();
set.<span class="hljs-title function_">add</span>(<span class="hljs-string">'+0'</span>).<span class="hljs-title function_">add</span>(<span class="hljs-string">'-0'</span>).<span class="hljs-title function_">add</span>(<span class="hljs-title class_">NaN</span>).<span class="hljs-title function_">add</span>(<span class="hljs-literal">undefined</span>).<span class="hljs-title function_">add</span>(<span class="hljs-title class_">NaN</span>);
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(set);
</code></pre>
<!-- codeblock-end -->

- 1: Set(4) {"+0", "-0", NaN, undefined}

- 2: Set(3) {"+0", NaN, undefined}

- 3: Set(5) {"+0", "-0", NaN, undefined, NaN}

- 4: Set(4) {"+0", NaN, undefined, NaN}  

==================== Answer ====================  

Answer: 1

Set has few exceptions from equality check,

1. All NaN values are equal

2. Both +0 and -0 considered as different values

==================== Id ====================  
477

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#477-What-is-the-output-of-below-code-javasc

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
