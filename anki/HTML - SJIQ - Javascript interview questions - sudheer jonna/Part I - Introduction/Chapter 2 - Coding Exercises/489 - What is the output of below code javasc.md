==================== Question ====================  

### What is the output of below code

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">greet</span>(<span class="hljs-params">greeting, name, message = greeting + <span class="hljs-string">' '</span> + name</span>) {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>([greeting, name, message]);
}
<span class="hljs-title function_">greet</span>(<span class="hljs-string">'Hello'</span>, <span class="hljs-string">'John'</span>);
<span class="hljs-title function_">greet</span>(<span class="hljs-string">'Hello'</span>, <span class="hljs-string">'John'</span>, <span class="hljs-string">'Good morning!'</span>);
</code></pre>
<!-- codeblock-end -->

- 1: SyntaxError

- 2: ['Hello', 'John', 'Hello John'], ['Hello', 'John', 'Good morning!']  

==================== Answer ====================  

Answer: 2

Since parameters defined earlier are available to later default parameters, this code snippet doesn't throw any error.

==================== Id ====================  
489

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#489-What-is-the-output-of-below-code-javasc

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
