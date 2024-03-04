==================== Question ====================  

### How do you combine two or more arrays  

==================== Answer ====================  

The concat() method is used to join two or more arrays by returning a new array containing all the elements. The syntax would be as below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript">array1.<span class="hljs-title function_">concat</span>(array2, array3, ..., arrayX)
</code></pre>
<!-- codeblock-end -->

Let's take an example of array's concatenation with veggies and fruits arrays,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> veggies = [<span class="hljs-string">'Tomato'</span>, <span class="hljs-string">'Carrot'</span>, <span class="hljs-string">'Cabbage'</span>];
<span class="hljs-keyword">var</span> fruits = [<span class="hljs-string">'Apple'</span>, <span class="hljs-string">'Orange'</span>, <span class="hljs-string">'Pears'</span>];
<span class="hljs-keyword">var</span> veggiesAndFruits = veggies.<span class="hljs-title function_">concat</span>(fruits);
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(veggiesAndFruits); <span class="hljs-comment">// Tomato, Carrot, Cabbage, Apple, Orange, Pears</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
344

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#344-How-do-you-combine-two-or-more-arrays

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
