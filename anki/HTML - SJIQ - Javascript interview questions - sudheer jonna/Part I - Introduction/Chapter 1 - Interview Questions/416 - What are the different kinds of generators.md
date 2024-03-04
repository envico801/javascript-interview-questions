==================== Question ====================  

### What are the different kinds of generators  

==================== Answer ====================  

There are five kinds of generators,

1. **Generator function declaration:**

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
    <span class="hljs-keyword">function</span>* <span class="hljs-title function_">myGenFunc</span>(<span class="hljs-params"></span>) {
      <span class="hljs-keyword">yield</span> <span class="hljs-number">1</span>;
      <span class="hljs-keyword">yield</span> <span class="hljs-number">2</span>;
      <span class="hljs-keyword">yield</span> <span class="hljs-number">3</span>;
    }
    <span class="hljs-keyword">const</span> genObj = <span class="hljs-title function_">myGenFunc</span>();
    </code></pre>
    <!-- codeblock-end -->

2. **Generator function expressions:**

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
    <span class="hljs-keyword">const</span> myGenFunc = <span class="hljs-keyword">function</span>* () {
      <span class="hljs-keyword">yield</span> <span class="hljs-number">1</span>;
      <span class="hljs-keyword">yield</span> <span class="hljs-number">2</span>;
      <span class="hljs-keyword">yield</span> <span class="hljs-number">3</span>;
    };
    <span class="hljs-keyword">const</span> genObj = <span class="hljs-title function_">myGenFunc</span>();
    </code></pre>
    <!-- codeblock-end -->

3. **Generator method definitions in object literals:**

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
    <span class="hljs-keyword">const</span> myObj = {
      *<span class="hljs-title function_">myGeneratorMethod</span>(<span class="hljs-params"></span>) {
        <span class="hljs-keyword">yield</span> <span class="hljs-number">1</span>;
        <span class="hljs-keyword">yield</span> <span class="hljs-number">2</span>;
        <span class="hljs-keyword">yield</span> <span class="hljs-number">3</span>;
      },
    };
    <span class="hljs-keyword">const</span> genObj = myObj.<span class="hljs-title function_">myGeneratorMethod</span>();
    </code></pre>
    <!-- codeblock-end -->

4. **Generator method definitions in class:**

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
    <span class="hljs-keyword">class</span> <span class="hljs-title class_">MyClass</span> {
      *<span class="hljs-title function_">myGeneratorMethod</span>(<span class="hljs-params"></span>) {
        <span class="hljs-keyword">yield</span> <span class="hljs-number">1</span>;
        <span class="hljs-keyword">yield</span> <span class="hljs-number">2</span>;
        <span class="hljs-keyword">yield</span> <span class="hljs-number">3</span>;
      }
    }
    <span class="hljs-keyword">const</span> myObject = <span class="hljs-keyword">new</span> <span class="hljs-title class_">MyClass</span>();
    <span class="hljs-keyword">const</span> genObj = myObject.<span class="hljs-title function_">myGeneratorMethod</span>();
    </code></pre>
    <!-- codeblock-end -->

5. **Generator as a computed property:**

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
    <span class="hljs-keyword">const</span> <span class="hljs-title class_">SomeObj</span> = {
      *[<span class="hljs-title class_">Symbol</span>.<span class="hljs-property">iterator</span>]() {
        <span class="hljs-keyword">yield</span> <span class="hljs-number">1</span>;
        <span class="hljs-keyword">yield</span> <span class="hljs-number">2</span>;
        <span class="hljs-keyword">yield</span> <span class="hljs-number">3</span>;
      },
    };
    <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-title class_">Array</span>.<span class="hljs-title function_">from</span>(<span class="hljs-title class_">SomeObj</span>)); <span class="hljs-comment">// [ 1, 2, 3 ]</span>
    </code></pre>
    <!-- codeblock-end -->

==================== Id ====================  
416

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#416-What-are-the-different-kinds-of-generators

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
