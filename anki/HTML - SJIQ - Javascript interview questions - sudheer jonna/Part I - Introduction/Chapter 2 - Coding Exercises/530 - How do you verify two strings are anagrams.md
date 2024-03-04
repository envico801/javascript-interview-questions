==================== Question ====================  

### How do you verify two strings are anagrams?  

==================== Answer ====================  

An anagram is a word or phrase formed by rearranging all the letters of a different word or phrase exactly once. For example, the anagrams of "eat" word are "tea" and "ate".

You can split each word into characters, followed by sort action and later join them back. After that you can compare those two words to verify whether those two words are anagrams or not.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">verifyAnagrams</span>(<span class="hljs-params">word1, word2</span>) {
  <span class="hljs-keyword">return</span> word1.<span class="hljs-title function_">split</span>(<span class="hljs-string">''</span>).<span class="hljs-title function_">sort</span>().<span class="hljs-title function_">join</span>(<span class="hljs-string">''</span>) === word2.<span class="hljs-title function_">split</span>(<span class="hljs-string">''</span>).<span class="hljs-title function_">sort</span>().<span class="hljs-title function_">join</span>(<span class="hljs-string">''</span>);
}
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-title function_">verifyAnagrams</span>(<span class="hljs-string">'eat'</span>, <span class="hljs-string">'ate'</span>));
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
530

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#530-How-do-you-verify-two-strings-are-anagrams

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
