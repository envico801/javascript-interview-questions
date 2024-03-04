==================== Question ====================  

### What is the difference between let and var  

==================== Answer ====================  

You can list out the differences in a tabular format

| var                                                         | let                                           |
| ----------------------------------------------------------- | --------------------------------------------- |
| It has been available from the beginning of JavaScript      | Introduced as part of ES6                     |
| It has function scope                                       | It has block scope                            |
| Variable declaration will be hoisted                        | Hoisted but not initialized                   |
| It is possible to re-declare the variable in the same scope | It is not possible to re-declare the variable |

Let's take an example to see the difference,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">userDetails</span>(<span class="hljs-params">username</span>) {
  <span class="hljs-keyword">if</span> (username) {
     <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(salary); <span class="hljs-comment">// undefined due to hoisting</span>
     <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(age); <span class="hljs-comment">// ReferenceError: Cannot access 'age' before initialization</span>
     <span class="hljs-keyword">let</span> age = <span class="hljs-number">30</span>;
     <span class="hljs-keyword">var</span> salary = <span class="hljs-number">10000</span>;
  }
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(salary); <span class="hljs-comment">//10000 (accessible due to function scope)</span>
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(age); <span class="hljs-comment">//error: age is not defined(due to block scope)</span>
}
<span class="hljs-title function_">userDetails</span>(<span class="hljs-string">'John'</span>);
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
18

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#18-What-is-the-difference-between-let-and-var

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
