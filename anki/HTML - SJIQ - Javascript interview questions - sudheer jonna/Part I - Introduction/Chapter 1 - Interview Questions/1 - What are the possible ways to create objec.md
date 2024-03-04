==================== Question ====================  

### What are the possible ways to create objects in JavaScript  

==================== Answer ====================  

There are many ways to create objects in javascript as mentioned below:

1. **Object literal syntax:**

    The object literal syntax (or object initializer), is a comma-separated set of name-value pairs wrapped in curly braces.

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
    <span class="hljs-keyword">var</span> object = {
      <span class="hljs-attr">name</span>: <span class="hljs-string">'Sudheer'</span>,
      <span class="hljs-attr">age</span>: <span class="hljs-number">34</span>,
    };
    </code></pre>
    <!-- codeblock-end -->

    Object literal property values can be of any data type, including array, function, and nested object.

    **Note:** This is one of the easiest ways to create an object.

2. **Object constructor:**

    The simplest way to create an empty object is using the `Object` constructor. Currently this approach is not recommended.

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
    <span class="hljs-keyword">var</span> object = <span class="hljs-keyword">new</span> <span class="hljs-title class_">Object</span>();
    </code></pre>
    <!-- codeblock-end -->

    The `Object()` is a built-in constructor function so "new" keyword is not required. The above code snippet can be re-written as:

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
    <span class="hljs-keyword">var</span> object = <span class="hljs-title class_">Object</span>();
    </code></pre>
    <!-- codeblock-end -->

3. **Object's create method:**

    The `create` method of Object is used to create a new object by passing the specificied prototype object and properties as arguments, i.e., this pattern is helpful to create new objects based on existing objects.

    The second argument is optional and it is used to create properties on a newly created object.

    The following code creates a new empty object whose prototype is null.

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
    <span class="hljs-keyword">var</span> object = <span class="hljs-title class_">Object</span>.<span class="hljs-title function_">create</span>(<span class="hljs-literal">null</span>);
    </code></pre>
    <!-- codeblock-end -->

    The following example creates an object along with additional new properties.

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
    <span class="hljs-keyword">let</span> vehicle = {
      <span class="hljs-attr">wheels</span>: <span class="hljs-string">'4'</span>,
      <span class="hljs-attr">fuelType</span>: <span class="hljs-string">'Gasoline'</span>,
      <span class="hljs-attr">color</span>: <span class="hljs-string">'Green'</span>,
    };
    <span class="hljs-keyword">let</span> carProps = {
      <span class="hljs-attr">type</span>: {
        <span class="hljs-attr">value</span>: <span class="hljs-string">'Volkswagen'</span>,
      },
      <span class="hljs-attr">model</span>: {
        <span class="hljs-attr">value</span>: <span class="hljs-string">'Golf'</span>,
      },
    };
    <span class="hljs-keyword">var</span> car = <span class="hljs-title class_">Object</span>.<span class="hljs-title function_">create</span>(vehicle, carProps);
    <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(car);
    </code></pre>
    <!-- codeblock-end -->

4. **Function constructor:**

    In this approach, create any function and apply the new operator to create object instances.

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
    <span class="hljs-keyword">function</span> <span class="hljs-title function_">Person</span>(<span class="hljs-params">name</span>) {
      <span class="hljs-variable language_">this</span>.<span class="hljs-property">name</span> = name;
      <span class="hljs-variable language_">this</span>.<span class="hljs-property">age</span> = <span class="hljs-number">21</span>;
    }
    <span class="hljs-keyword">var</span> object = <span class="hljs-keyword">new</span> <span class="hljs-title class_">Person</span>(<span class="hljs-string">'Sudheer'</span>);
    </code></pre>
    <!-- codeblock-end -->

5. **Function constructor with prototype:**

    This is similar to function constructor but it uses prototype for their properties and methods,

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
    <span class="hljs-keyword">function</span> <span class="hljs-title function_">Person</span>(<span class="hljs-params"></span>) {}
    <span class="hljs-title class_">Person</span>.<span class="hljs-property"><span class="hljs-keyword">prototype</span></span>.<span class="hljs-property">name</span> = <span class="hljs-string">'Sudheer'</span>;
    <span class="hljs-keyword">var</span> object = <span class="hljs-keyword">new</span> <span class="hljs-title class_">Person</span>();
    </code></pre>
    <!-- codeblock-end -->

    This is equivalent to creating an instance with Object.create method with a function prototype and then calling that function with an instance and parameters as arguments.

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
    <span class="hljs-keyword">function</span> <span class="hljs-title function_">func</span>(<span class="hljs-params"></span>) {}
    <span class="hljs-keyword">new</span> <span class="hljs-title function_">func</span>(x, y, z);
    </code></pre>
    <!-- codeblock-end -->

    **(OR)**

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
    <span class="hljs-comment">// Create a new instance using function prototype.</span>
    <span class="hljs-keyword">var</span> newInstance = <span class="hljs-title class_">Object</span>.<span class="hljs-title function_">create</span>(func.<span class="hljs-property"><span class="hljs-keyword">prototype</span></span>)
    <span class="hljs-comment">// Call the function</span>
    <span class="hljs-keyword">var</span> result = func.<span class="hljs-title function_">call</span>(newInstance, x, y, z),
    <span class="hljs-comment">// If the result is a non-null object then use it otherwise just use the new instance.</span>
    <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(result &#x26;&#x26; <span class="hljs-keyword">typeof</span> result === <span class="hljs-string">'object'</span> ? result : newInstance);
    </code></pre>
    <!-- codeblock-end -->

6. **Object's assign method:**

    The `Object.assign` method is used to copy all the properties from one or more source objects and stores them into a target object.

    The following code creates a new staff object by copying properties of his working company and the car he owns.

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
    <span class="hljs-keyword">const</span> orgObject = { <span class="hljs-attr">company</span>: <span class="hljs-string">'XYZ Corp'</span> };
    <span class="hljs-keyword">const</span> carObject = { <span class="hljs-attr">name</span>: <span class="hljs-string">'Toyota'</span> };
    <span class="hljs-keyword">const</span> staff = <span class="hljs-title class_">Object</span>.<span class="hljs-title function_">assign</span>({}, orgObject, carObject);
    </code></pre>
    <!-- codeblock-end -->

7. **ES6 Class syntax:**

    ES6 introduces class feature to create objects.

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
    <span class="hljs-keyword">class</span> <span class="hljs-title class_">Person</span> {
      <span class="hljs-title function_">constructor</span>(<span class="hljs-params">name</span>) {
        <span class="hljs-variable language_">this</span>.<span class="hljs-property">name</span> = name;
      }
    }
    <span class="hljs-keyword">var</span> object = <span class="hljs-keyword">new</span> <span class="hljs-title class_">Person</span>(<span class="hljs-string">'Sudheer'</span>);
    </code></pre>
    <!-- codeblock-end -->

8. **Singleton pattern:**

    A Singleton is an object which can only be instantiated one time. Repeated calls to its constructor return the same instance. This way one can ensure that they don't accidentally create multiple instances.

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
    <span class="hljs-keyword">var</span> object = <span class="hljs-keyword">new</span> (<span class="hljs-keyword">function</span> (<span class="hljs-params"></span>) {
      <span class="hljs-variable language_">this</span>.<span class="hljs-property">name</span> = <span class="hljs-string">'Sudheer'</span>;
    })();
    </code></pre>
    <!-- codeblock-end -->

==================== Id ====================  
1

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#1-What-are-the-possible-ways-to-create-objec

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
