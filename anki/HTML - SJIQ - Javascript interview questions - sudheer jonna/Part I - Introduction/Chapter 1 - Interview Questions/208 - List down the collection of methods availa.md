==================== Question ====================  

### List down the collection of methods available on WeakMap  

==================== Answer ====================  

Below are the list of methods available on WeakMap,

1. set(key, value): Sets the value for the key in the WeakMap object. Returns the WeakMap object.

2. delete(key): Removes any value associated to the key.

3. has(key): Returns a Boolean asserting whether a value has been associated to the key in the WeakMap object or not.

4. get(key): Returns the value associated to the key, or undefined if there is none.

    Let's see the functionality of all the above methods in an example,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> weakMapObject = <span class="hljs-keyword">new</span> <span class="hljs-title class_">WeakMap</span>();
<span class="hljs-keyword">var</span> firstObject = {};
<span class="hljs-keyword">var</span> secondObject = {};
<span class="hljs-comment">// set(key, value)</span>
weakMapObject.<span class="hljs-title function_">set</span>(firstObject, <span class="hljs-string">'John'</span>);
weakMapObject.<span class="hljs-title function_">set</span>(secondObject, <span class="hljs-number">100</span>);
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(weakMapObject.<span class="hljs-title function_">has</span>(firstObject)); <span class="hljs-comment">//true</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(weakMapObject.<span class="hljs-title function_">get</span>(firstObject)); <span class="hljs-comment">// John</span>
weakMapObject.<span class="hljs-title function_">delete</span>(secondObject);
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
208

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#208-List-down-the-collection-of-methods-availa

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
