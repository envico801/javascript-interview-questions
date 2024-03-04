==================== Question ====================  

### What is the output of below code?

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">let</span> user1 = {
  <span class="hljs-attr">name</span>: <span class="hljs-string">'Jacob'</span>,
  <span class="hljs-attr">age</span>: <span class="hljs-number">28</span>,
};
<span class="hljs-keyword">let</span> user2 = {
  <span class="hljs-attr">name</span>: <span class="hljs-string">'Jacob'</span>,
  <span class="hljs-attr">age</span>: <span class="hljs-number">28</span>,
};
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(user1 === user2);
</code></pre>
<!-- codeblock-end -->

- 1: True

- 2: False

- 3: Compile time error  

==================== Answer ====================  

Answer: 2

In JavaScript, the variables such as objects, arrays and functions comes under pass by reference. When you try to compare two objects with same content, it is going to compare memory address or reference of those variables. These variables always create separate memory blocks hence the comparison is always going to return false value.

==================== Id ====================  
522

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#522-What-is-the-output-of-below-code-javas

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
