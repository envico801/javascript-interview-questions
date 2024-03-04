==================== Question ====================  

### How do you extend classes  

==================== Answer ====================  

The `extends` keyword is used in class declarations/expressions to create a class which is a child of another class. It can be used to subclass custom classes as well as built-in objects. The syntax would be as below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">class</span> <span class="hljs-title class_">ChildClass</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">ParentClass</span> { ... }
</code></pre>
<!-- codeblock-end -->

Let's take an example of Square subclass from Polygon parent class,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">class</span> <span class="hljs-title class_">Square</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">Rectangle</span> {
  <span class="hljs-title function_">constructor</span>(<span class="hljs-params">length</span>) {
     <span class="hljs-variable language_">super</span>(length, length);
     <span class="hljs-variable language_">this</span>.<span class="hljs-property">name</span> = <span class="hljs-string">'Square'</span>;
  }
  <span class="hljs-keyword">get</span> <span class="hljs-title function_">area</span>() {
     <span class="hljs-keyword">return</span> <span class="hljs-variable language_">this</span>.<span class="hljs-property">width</span> * <span class="hljs-variable language_">this</span>.<span class="hljs-property">height</span>;
  }
  <span class="hljs-keyword">set</span> <span class="hljs-title function_">area</span>(<span class="hljs-params">value</span>) {
     <span class="hljs-variable language_">this</span>.<span class="hljs-property">area</span> = value;
  }
}
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
283

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#283-How-do-you-extend-classes

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
