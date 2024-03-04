==================== Question ====================  

### How do you reverse an array without modifying original array?  

==================== Answer ====================  

The `reverse()` method reverses the order of the elements in an array but it mutates the original array. Let's take a simple example to demonistrate this case,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> originalArray = [<span class="hljs-number">1</span>, <span class="hljs-number">2</span>, <span class="hljs-number">3</span>, <span class="hljs-number">4</span>, <span class="hljs-number">5</span>];
<span class="hljs-keyword">const</span> newArray = originalArray.<span class="hljs-title function_">reverse</span>();
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(newArray); <span class="hljs-comment">// [ 5, 4, 3, 2, 1]</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(originalArray); <span class="hljs-comment">// [ 5, 4, 3, 2, 1]</span>
</code></pre>
<!-- codeblock-end -->

There are few solutions that won't mutate the original array. Let's take a look.

1. **Using slice and reverse methods:**

    In this case, just invoke the `slice()` method on the array to create a shallow copy followed by `reverse()` method call on the copy.

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
    <span class="hljs-keyword">const</span> originalArray = [<span class="hljs-number">1</span>, <span class="hljs-number">2</span>, <span class="hljs-number">3</span>, <span class="hljs-number">4</span>, <span class="hljs-number">5</span>];
    <span class="hljs-keyword">const</span> newArray = originalArray.<span class="hljs-title function_">slice</span>().<span class="hljs-title function_">reverse</span>(); <span class="hljs-comment">//Slice an array gives a new copy</span>
    <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(originalArray); <span class="hljs-comment">// [1, 2, 3, 4, 5]</span>
    <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(newArray); <span class="hljs-comment">// [ 5, 4, 3, 2, 1]</span>
    </code></pre>
    <!-- codeblock-end -->

2. **Using spread and reverse methods:**

    In this case, let's use the spread syntax (...) to create a copy of the array followed by `reverse()` method call on the copy.

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
    <span class="hljs-keyword">const</span> originalArray = [<span class="hljs-number">1</span>, <span class="hljs-number">2</span>, <span class="hljs-number">3</span>, <span class="hljs-number">4</span>, <span class="hljs-number">5</span>];
    <span class="hljs-keyword">const</span> newArray = [...originalArray].<span class="hljs-title function_">reverse</span>();
    <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(originalArray); <span class="hljs-comment">// [1, 2, 3, 4, 5]</span>
    <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(newArray); <span class="hljs-comment">// [ 5, 4, 3, 2, 1]</span>
    </code></pre>
    <!-- codeblock-end -->

3. **Using reduce and spread methods:**

    Here execute a reducer function on an array elements and append the accumulated array on right side using spread syntax

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
    <span class="hljs-keyword">const</span> originalArray = [<span class="hljs-number">1</span>, <span class="hljs-number">2</span>, <span class="hljs-number">3</span>, <span class="hljs-number">4</span>, <span class="hljs-number">5</span>];
    <span class="hljs-keyword">const</span> newArray = originalArray.<span class="hljs-title function_">reduce</span>(<span class="hljs-function">(<span class="hljs-params">accumulator, value</span>) =></span> {
      <span class="hljs-keyword">return</span> [value, ...accumulator];
    }, []);
    <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(originalArray); <span class="hljs-comment">// [1, 2, 3, 4, 5]</span>
    <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(newArray); <span class="hljs-comment">// [ 5, 4, 3, 2, 1]</span>
    </code></pre>
    <!-- codeblock-end -->

4. **Using reduceRight and spread methods:**

    Here execute a right reducer function(i.e. opposite direction of reduce method) on an array elements and append the accumulated array on left side using spread syntax

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
    <span class="hljs-keyword">const</span> originalArray = [<span class="hljs-number">1</span>, <span class="hljs-number">2</span>, <span class="hljs-number">3</span>, <span class="hljs-number">4</span>, <span class="hljs-number">5</span>];
    <span class="hljs-keyword">const</span> newArray = originalArray.<span class="hljs-title function_">reduceRight</span>(<span class="hljs-function">(<span class="hljs-params">accumulator, value</span>) =></span> {
      <span class="hljs-keyword">return</span> [...accumulator, value];
    }, []);
    <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(originalArray); <span class="hljs-comment">// [1, 2, 3, 4, 5]</span>
    <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(newArray); <span class="hljs-comment">// [ 5, 4, 3, 2, 1]</span>
    </code></pre>
    <!-- codeblock-end -->

5. **Using reduceRight and push methods:**

    Here execute a right reducer function(i.e. opposite direction of reduce method) on an array elements and push the iterated value to the accumulator

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
    <span class="hljs-keyword">const</span> originalArray = [<span class="hljs-number">1</span>, <span class="hljs-number">2</span>, <span class="hljs-number">3</span>, <span class="hljs-number">4</span>, <span class="hljs-number">5</span>];
    <span class="hljs-keyword">const</span> newArray = originalArray.<span class="hljs-title function_">reduceRight</span>(<span class="hljs-function">(<span class="hljs-params">accumulator, value</span>) =></span> {
      accumulator.<span class="hljs-title function_">push</span>(value);
      <span class="hljs-keyword">return</span> accumulator;
    }, []);
    <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(originalArray); <span class="hljs-comment">// [1, 2, 3, 4, 5]</span>
    <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(newArray); <span class="hljs-comment">// [ 5, 4, 3, 2, 1]</span>
    </code></pre>
    <!-- codeblock-end -->

==================== Id ====================  
430

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#430-How-do-you-reverse-an-array-without-modify

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
