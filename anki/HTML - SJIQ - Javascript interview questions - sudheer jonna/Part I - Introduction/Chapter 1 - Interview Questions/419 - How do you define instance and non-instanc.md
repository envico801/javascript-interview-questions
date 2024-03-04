==================== Question ====================  

### How do you define instance and non-instance properties  

==================== Answer ====================  

The Instance properties must be defined inside of class methods. For example, name and age properties defined inside constructor as below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">class</span> <span class="hljs-title class_">Person</span> {
  <span class="hljs-title function_">constructor</span>(<span class="hljs-params">name, age</span>) {
     <span class="hljs-variable language_">this</span>.<span class="hljs-property">name</span> = name;
     <span class="hljs-variable language_">this</span>.<span class="hljs-property">age</span> = age;
  }
}
</code></pre>
<!-- codeblock-end -->

But Static(class) and prototype data properties must be defined outside of the ClassBody declaration. Let's assign the age value for Person class as below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-title class_">Person</span>.<span class="hljs-property">staticAge</span> = <span class="hljs-number">30</span>;
<span class="hljs-title class_">Person</span>.<span class="hljs-property"><span class="hljs-keyword">prototype</span></span>.<span class="hljs-property">prototypeAge</span> = <span class="hljs-number">40</span>;
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
419

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#419-How-do-you-define-instance-and-non-instanc

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
