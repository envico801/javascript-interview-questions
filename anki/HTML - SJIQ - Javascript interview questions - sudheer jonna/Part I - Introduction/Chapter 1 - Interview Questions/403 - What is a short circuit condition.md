==================== Question ====================  

### What is a Short circuit condition  

==================== Answer ====================  

Short circuit conditions are meant for condensed way of writing simple if statements. Let's demonstrate the scenario using an example. If you would like to login to a portal with an authentication condition, the expression would be as below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">if</span> (authenticate) {
  <span class="hljs-title function_">loginToPorta</span>();
}
</code></pre>
<!-- codeblock-end -->

Since the javascript logical operators evaluated from left to right, the above expression can be simplified using && logical operator

<!-- codeblock-start -->
<pre><code class="hljs language-javascript">authenticate &#x26;&#x26; <span class="hljs-title function_">loginToPorta</span>();
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
403

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#403-What-is-a-short-circuit-condition

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
