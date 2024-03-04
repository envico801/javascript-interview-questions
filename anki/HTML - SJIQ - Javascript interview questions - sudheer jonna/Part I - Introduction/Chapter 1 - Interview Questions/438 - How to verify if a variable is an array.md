==================== Question ====================  

### How to verify if a variable is an array?  

==================== Answer ====================  

It is possible to check if a variable is an array instance using 3 different ways,

1. Array.isArray() method:

    The `Array.isArray(value)` utility function is used to determine whether value is an array or not. This function returns a true boolean value if the variable is an array and a false value if it is not.

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
    <span class="hljs-keyword">const</span> numbers = [<span class="hljs-number">1</span>, <span class="hljs-number">2</span>, <span class="hljs-number">3</span>];
    <span class="hljs-keyword">const</span> user = { <span class="hljs-attr">name</span>: <span class="hljs-string">'John'</span> };
    <span class="hljs-title class_">Array</span>.<span class="hljs-title function_">isArray</span>(numbers); <span class="hljs-comment">// true</span>
    <span class="hljs-title class_">Array</span>.<span class="hljs-title function_">isArray</span>(user); <span class="hljs-comment">//false</span>
    </code></pre>
    <!-- codeblock-end -->

2. instanceof operator:

    The instanceof operator is used to check the type of an array at run time. It returns true if the type of a variable is an Array other false for other type.

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
    <span class="hljs-keyword">const</span> numbers = [<span class="hljs-number">1</span>, <span class="hljs-number">2</span>, <span class="hljs-number">3</span>];
    <span class="hljs-keyword">const</span> user = { <span class="hljs-attr">name</span>: <span class="hljs-string">'John'</span> };
    <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(numbers <span class="hljs-keyword">instanceof</span> <span class="hljs-title class_">Array</span>); <span class="hljs-comment">// true</span>
    <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(user <span class="hljs-keyword">instanceof</span> <span class="hljs-title class_">Array</span>); <span class="hljs-comment">// false</span>
    </code></pre>
    <!-- codeblock-end -->

3. Checking constructor type:

    The constructor property of the variable is used to determine whether the variable Array type or not.

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
    <span class="hljs-keyword">const</span> numbers = [<span class="hljs-number">1</span>, <span class="hljs-number">2</span>, <span class="hljs-number">3</span>];
    <span class="hljs-keyword">const</span> user = { <span class="hljs-attr">name</span>: <span class="hljs-string">'John'</span> };
    <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(numbers.<span class="hljs-property">constructor</span> === <span class="hljs-title class_">Array</span>); <span class="hljs-comment">// true</span>
    <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(user.<span class="hljs-property">constructor</span> === <span class="hljs-title class_">Array</span>); <span class="hljs-comment">// false</span>
    </code></pre>
    <!-- codeblock-end -->

==================== Id ====================  
438

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#438-How-to-verify-if-a-variable-is-an-array

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
