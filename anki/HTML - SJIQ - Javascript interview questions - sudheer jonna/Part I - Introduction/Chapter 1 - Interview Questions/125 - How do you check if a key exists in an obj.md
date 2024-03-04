==================== Question ====================  

### How do you check if a key exists in an object  

==================== Answer ====================  

You can check whether a key exists in an object or not using three approaches,

1. **Using in operator:** You can use the in operator whether a key exists in an object or not

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-string">'key'</span> <span class="hljs-keyword">in</span> obj;
</code></pre>
<!-- codeblock-end -->

and If you want to check if a key doesn't exist, remember to use parenthesis,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript">!(<span class="hljs-string">'key'</span> <span class="hljs-keyword">in</span> obj);
</code></pre>
<!-- codeblock-end -->

1. **Using hasOwnProperty method:** You can use `hasOwnProperty` to particularly test for properties of the object instance (and not inherited properties)

<!-- codeblock-start -->
<pre><code class="hljs language-javascript">obj.<span class="hljs-title function_">hasOwnProperty</span>(<span class="hljs-string">'key'</span>); <span class="hljs-comment">// true</span>
</code></pre>
<!-- codeblock-end -->

1. **Using undefined comparison:** If you access a non-existing property from an object, the result is undefined. Let’s compare the properties against undefined to determine the existence of the property.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> user = {
  <span class="hljs-attr">name</span>: <span class="hljs-string">'John'</span>,
};
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(user.<span class="hljs-property">name</span> !== <span class="hljs-literal">undefined</span>); <span class="hljs-comment">// true</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(user.<span class="hljs-property">nickName</span> !== <span class="hljs-literal">undefined</span>); <span class="hljs-comment">// false</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
125

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#125-How-do-you-check-if-a-key-exists-in-an-obj

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
