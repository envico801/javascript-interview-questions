==================== Question ====================  

### What is the difference between Shallow and Deep copy  

==================== Answer ====================  

There are two ways to copy an object,

**Shallow Copy:**

Shallow copy is a bitwise copy of an object. A new object is created that has an exact copy of the values in the original object. If any of the fields of the object are references to other objects, just the reference addresses are copied i.e., only the memory address is copied.

**Example**

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> empDetails = {
  <span class="hljs-attr">name</span>: <span class="hljs-string">'John'</span>,
  <span class="hljs-attr">age</span>: <span class="hljs-number">25</span>,
  <span class="hljs-attr">expertise</span>: <span class="hljs-string">'Software Developer'</span>,
};
</code></pre>
<!-- codeblock-end -->

to create a duplicate

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> empDetailsShallowCopy = empDetails; <span class="hljs-comment">//Shallow copying!</span>
</code></pre>
<!-- codeblock-end -->

if we change some property value in the duplicate one like this:

<!-- codeblock-start -->
<pre><code class="hljs language-javascript">empDetailsShallowCopy.<span class="hljs-property">name</span> = <span class="hljs-string">'Johnson'</span>;
</code></pre>
<!-- codeblock-end -->

The above statement will also change the name of `empDetails`, since we have a shallow copy. That means we're losing the original data as well.

**Deep copy:**

A deep copy copies all fields, and makes copies of dynamically allocated memory pointed to by the fields. A deep copy occurs when an object is copied along with the objects to which it refers.

**Example**

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> empDetails = {
  <span class="hljs-attr">name</span>: <span class="hljs-string">'John'</span>,
  <span class="hljs-attr">age</span>: <span class="hljs-number">25</span>,
  <span class="hljs-attr">expertise</span>: <span class="hljs-string">'Software Developer'</span>,
};
</code></pre>
<!-- codeblock-end -->

Create a deep copy by using the properties from the original object into new variable

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> empDetailsDeepCopy = {
  <span class="hljs-attr">name</span>: empDetails.<span class="hljs-property">name</span>,
  <span class="hljs-attr">age</span>: empDetails.<span class="hljs-property">age</span>,
  <span class="hljs-attr">expertise</span>: empDetails.<span class="hljs-property">expertise</span>,
};
</code></pre>
<!-- codeblock-end -->

Now if you change `empDetailsDeepCopy.name`, it will only affect `empDetailsDeepCopy` & not `empDetails`

==================== Id ====================  
345

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#345-What-is-the-difference-between-shallow-and

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
