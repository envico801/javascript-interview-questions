==================== Question ====================  

### What are the different ways to create sparse arrays?  

==================== Answer ====================  

There are 4 different ways to create sparse arrays in JavaScript

1. **Array literal:** Omit a value when using the array literal

    <!-- codeblock-start -->
    <pre><code class="hljs language-js">
    <span class="hljs-keyword">const</span> justiceLeague = [<span class="hljs-string">'Superman'</span>, <span class="hljs-string">'Aquaman'</span>, , <span class="hljs-string">'Batman'</span>];
    <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(justiceLeague); <span class="hljs-comment">// ['Superman', 'Aquaman', empty ,'Batman']</span>
    </code></pre>
    <!-- codeblock-end -->

2. **Array() constructor:** Invoking Array(length) or new Array(length)

    <!-- codeblock-start -->
    <pre><code class="hljs language-js">
    <span class="hljs-keyword">const</span> array = <span class="hljs-title class_">Array</span>(<span class="hljs-number">3</span>);
    <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(array); <span class="hljs-comment">// [empty, empty ,empty]</span>
    </code></pre>
    <!-- codeblock-end -->

3. **Delete operator:** Using delete array[index] operator on the array

    <!-- codeblock-start -->
    <pre><code class="hljs language-js">
    <span class="hljs-keyword">const</span> justiceLeague = [<span class="hljs-string">'Superman'</span>, <span class="hljs-string">'Aquaman'</span>, <span class="hljs-string">'Batman'</span>];
    <span class="hljs-keyword">delete</span> justiceLeague[<span class="hljs-number">1</span>];
    <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(justiceLeague); <span class="hljs-comment">// ['Superman', empty, ,'Batman']</span>
    </code></pre>
    <!-- codeblock-end -->

4. **Increase length property:** Increasing length property of an array

    <!-- codeblock-start -->
    <pre><code class="hljs language-js">
    <span class="hljs-keyword">const</span> justiceLeague = [<span class="hljs-string">'Superman'</span>, <span class="hljs-string">'Aquaman'</span>, <span class="hljs-string">'Batman'</span>];
    justiceLeague.<span class="hljs-property">length</span> = <span class="hljs-number">5</span>;
    <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(justiceLeague); <span class="hljs-comment">// ['Superman', 'Aquaman', 'Batman', empty, empty]</span>
    </code></pre>
    <!-- codeblock-end -->

==================== Id ====================  
428

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#428-What-are-the-different-ways-to-create-spar

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
