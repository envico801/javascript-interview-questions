==================== Question ====================  

### List down the collection of methods available on WeakSet  

==================== Answer ====================  

Below are the list of methods available on WeakSet,

1. add(value): A new object is appended with the given value to the weakset

2. delete(value): Deletes the value from the WeakSet collection.

3. has(value): It returns true if the value is present in the WeakSet Collection, otherwise it returns false.

Let's see the functionality of all the above methods in an example,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> weakSetObject = <span class="hljs-keyword">new</span> <span class="hljs-title class_">WeakSet</span>();
<span class="hljs-keyword">var</span> firstObject = {};
<span class="hljs-keyword">var</span> secondObject = {};
<span class="hljs-comment">// add(value)</span>
weakSetObject.<span class="hljs-title function_">add</span>(firstObject);
weakSetObject.<span class="hljs-title function_">add</span>(secondObject);
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(weakSetObject.<span class="hljs-title function_">has</span>(firstObject)); <span class="hljs-comment">//true</span>
weakSetObject.<span class="hljs-title function_">delete</span>(secondObject);
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
205

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#205-List-down-the-collection-of-methods-availa

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
