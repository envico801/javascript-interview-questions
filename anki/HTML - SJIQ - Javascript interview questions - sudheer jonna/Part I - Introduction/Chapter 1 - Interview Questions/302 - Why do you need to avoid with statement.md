==================== Question ====================  

### Why do you need to avoid with statement  

==================== Answer ====================  

JavaScript's with statement was intended to provide a shorthand for writing recurring accesses to objects. So it can help reduce file size by reducing the need to repeat a lengthy object reference without performance penalty. Let's take an example where it is used to avoid redundancy when accessing an object several times.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript">a.<span class="hljs-property">b</span>.<span class="hljs-property">c</span>.<span class="hljs-property">greeting</span> = <span class="hljs-string">'welcome'</span>;
a.<span class="hljs-property">b</span>.<span class="hljs-property">c</span>.<span class="hljs-property">age</span> = <span class="hljs-number">32</span>;
</code></pre>
<!-- codeblock-end -->

Using `with` it turns this into:

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">with</span> (a.<span class="hljs-property">b</span>.<span class="hljs-property">c</span>) {
  greeting = <span class="hljs-string">'welcome'</span>;
  age = <span class="hljs-number">32</span>;
}
</code></pre>
<!-- codeblock-end -->

But this `with` statement creates performance problems since one cannot predict whether an argument will refer to a real variable or to a property inside the with argument.

==================== Id ====================  
302

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#302-Why-do-you-need-to-avoid-with-statement

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
