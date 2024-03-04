==================== Question ====================  

### Does javascript uses mixins  

==================== Answer ====================  

Mixin is a generic object-oriented programming term - is a class containing methods that can be used by other classes without a need to inherit from it. In JavaScript we can only inherit from a single object. ie. There can be only one `[[prototype]]` for an object.

But sometimes we require to extend more than one, to overcome this we can use Mixin which helps to copy methods to the prototype of another class.

Say for instance, we've two classes `User` and `CleanRoom`. Suppose we need to add `CleanRoom` functionality to `User`, so that user can clean the room at demand. Here's where concept called mixins comes into picture.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-comment">// mixin</span>
<span class="hljs-keyword">let</span> cleanRoomMixin = {
  <span class="hljs-title function_">cleanRoom</span>(<span class="hljs-params"></span>) {
     <span class="hljs-title function_">alert</span>(<span class="hljs-string">`Hello <span class="hljs-subst">${<span class="hljs-variable language_">this</span>.name}</span>, your room is clean now`</span>);
  },
  <span class="hljs-title function_">sayBye</span>(<span class="hljs-params"></span>) {
     <span class="hljs-title function_">alert</span>(<span class="hljs-string">`Bye <span class="hljs-subst">${<span class="hljs-variable language_">this</span>.name}</span>`</span>);
  },
};
<span class="hljs-comment">// usage:</span>
<span class="hljs-keyword">class</span> <span class="hljs-title class_">User</span> {
  <span class="hljs-title function_">constructor</span>(<span class="hljs-params">name</span>) {
     <span class="hljs-variable language_">this</span>.<span class="hljs-property">name</span> = name;
  }
}
<span class="hljs-comment">// copy the methods</span>
<span class="hljs-title class_">Object</span>.<span class="hljs-title function_">assign</span>(<span class="hljs-title class_">User</span>.<span class="hljs-property"><span class="hljs-keyword">prototype</span></span>, cleanRoomMixin);
<span class="hljs-comment">// now User can clean the room</span>
<span class="hljs-keyword">new</span> <span class="hljs-title class_">User</span>(<span class="hljs-string">'Dude'</span>).<span class="hljs-title function_">cleanRoom</span>(); <span class="hljs-comment">// Hello Dude, your room is clean now!</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
350

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#350-Does-javascript-uses-mixins

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
