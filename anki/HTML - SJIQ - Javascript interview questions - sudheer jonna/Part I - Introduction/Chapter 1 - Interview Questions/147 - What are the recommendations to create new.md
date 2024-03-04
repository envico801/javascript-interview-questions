==================== Question ====================  

### What are the recommendations to create new object  

==================== Answer ====================  

It is recommended to avoid creating new objects using `new Object()`. Instead you can initialize values based on it's type to create the objects.

1. Assign {} instead of new Object()

2. Assign "" instead of new String()

3. Assign 0 instead of new Number()

4. Assign false instead of new Boolean()

5. Assign [] instead of new Array()

6. Assign /()/ instead of new RegExp()

7. Assign function (){} instead of new Function()

You can define them as an example,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> v1 = {};
<span class="hljs-keyword">var</span> v2 = <span class="hljs-string">''</span>;
<span class="hljs-keyword">var</span> v3 = <span class="hljs-number">0</span>;
<span class="hljs-keyword">var</span> v4 = <span class="hljs-literal">false</span>;
<span class="hljs-keyword">var</span> v5 = [];
<span class="hljs-keyword">var</span> v6 = <span class="hljs-regexp">/()/</span>;
<span class="hljs-keyword">var</span> v7 = <span class="hljs-keyword">function</span> (<span class="hljs-params"></span>) {};
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
147

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#147-What-are-the-recommendations-to-create-new

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
