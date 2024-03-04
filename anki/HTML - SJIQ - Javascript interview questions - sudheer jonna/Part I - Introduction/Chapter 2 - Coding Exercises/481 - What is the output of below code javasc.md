==================== Question ====================  

### What is the output of below code

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-title class_">JSON</span>.<span class="hljs-title function_">stringify</span>({ <span class="hljs-attr">myArray</span>: [<span class="hljs-string">'one'</span>, <span class="hljs-literal">undefined</span>, <span class="hljs-keyword">function</span> (<span class="hljs-params"></span>) {}, <span class="hljs-title class_">Symbol</span>(<span class="hljs-string">''</span>)] }));
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-title class_">JSON</span>.<span class="hljs-title function_">stringify</span>({ [<span class="hljs-title class_">Symbol</span>.<span class="hljs-title function_">for</span>(<span class="hljs-string">'one'</span>)]: <span class="hljs-string">'one'</span> }, [<span class="hljs-title class_">Symbol</span>.<span class="hljs-title function_">for</span>(<span class="hljs-string">'one'</span>)]));
</code></pre>
<!-- codeblock-end -->

- 1: {"myArray":['one', undefined, {}, Symbol]}, {}

- 2: {"myArray":['one', null,null,null]}, {}

- 3: {"myArray":['one', null,null,null]}, "{ [Symbol.for('one')]: 'one' }, [Symbol.for('one')]"

- 4: {"myArray":['one', undefined, function(){}, Symbol('')]}, {}  

==================== Answer ====================  

Answer: 2

The symbols has below constraints,

1. The undefined, Functions, and Symbols are not valid JSON values. So those values are either omitted (in an object) or changed to null (in an array). Hence, it returns null values for the value array.

2. All Symbol-keyed properties will be completely ignored. Hence it returns an empty object({}).

==================== Id ====================  
481

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#481-What-is-the-output-of-below-code-javasc

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
