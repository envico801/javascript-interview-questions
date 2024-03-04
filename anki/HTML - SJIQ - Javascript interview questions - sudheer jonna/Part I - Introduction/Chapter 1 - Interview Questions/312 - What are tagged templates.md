==================== Question ====================  

### What are tagged templates  

==================== Answer ====================  

Tagged templates are the advanced form of templates in which tags allow you to parse template literals with a function. The tag function accepts the first parameter as an array of strings and remaining parameters as expressions. This function can also return manipulated strings based on parameters. Let's see the usage of this tagged template behavior of an IT professional skill set in an organization,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> user1 = <span class="hljs-string">'John'</span>;
<span class="hljs-keyword">var</span> skill1 = <span class="hljs-string">'JavaScript'</span>;
<span class="hljs-keyword">var</span> experience1 = <span class="hljs-number">15</span>;
<span class="hljs-keyword">var</span> user2 = <span class="hljs-string">'Kane'</span>;
<span class="hljs-keyword">var</span> skill2 = <span class="hljs-string">'JavaScript'</span>;
<span class="hljs-keyword">var</span> experience2 = <span class="hljs-number">5</span>;
<span class="hljs-keyword">function</span> <span class="hljs-title function_">myInfoTag</span>(<span class="hljs-params">strings, userExp, experienceExp, skillExp</span>) {
  <span class="hljs-keyword">var</span> str0 = strings[<span class="hljs-number">0</span>]; <span class="hljs-comment">// "Mr/Ms. "</span>
  <span class="hljs-keyword">var</span> str1 = strings[<span class="hljs-number">1</span>]; <span class="hljs-comment">// " is a/an "</span>
  <span class="hljs-keyword">var</span> str2 = strings[<span class="hljs-number">2</span>]; <span class="hljs-comment">// "in"</span>
  <span class="hljs-keyword">var</span> expertiseStr;
  <span class="hljs-keyword">if</span> (experienceExp > <span class="hljs-number">10</span>) {
     expertiseStr = <span class="hljs-string">'expert developer'</span>;
  } <span class="hljs-keyword">else</span> <span class="hljs-keyword">if</span> (skillExp > <span class="hljs-number">5</span> &#x26;&#x26; skillExp &#x3C;= <span class="hljs-number">10</span>) {
     expertiseStr = <span class="hljs-string">'senior developer'</span>;
  } <span class="hljs-keyword">else</span> {
     expertiseStr = <span class="hljs-string">'junior developer'</span>;
  }
  <span class="hljs-keyword">return</span> <span class="hljs-string">`<span class="hljs-subst">${str0}</span><span class="hljs-subst">${userExp}</span><span class="hljs-subst">${str1}</span><span class="hljs-subst">${expertiseStr}</span><span class="hljs-subst">${str2}</span><span class="hljs-subst">${skillExp}</span>`</span>;
}
<span class="hljs-keyword">var</span> output1 = myInfoTag<span class="hljs-string">`Mr/Ms. <span class="hljs-subst">${user1}</span> is a/an <span class="hljs-subst">${experience1}</span> in <span class="hljs-subst">${skill1}</span>`</span>;
<span class="hljs-keyword">var</span> output2 = myInfoTag<span class="hljs-string">`Mr/Ms. <span class="hljs-subst">${user2}</span> is a/an <span class="hljs-subst">${experience2}</span> in <span class="hljs-subst">${skill2}</span>`</span>;
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(output1); <span class="hljs-comment">// Mr/Ms. John is a/an expert developer in JavaScript</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(output2); <span class="hljs-comment">// Mr/Ms. Kane is a/an junior developer in JavaScript</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
312

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#312-What-are-tagged-templates

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
