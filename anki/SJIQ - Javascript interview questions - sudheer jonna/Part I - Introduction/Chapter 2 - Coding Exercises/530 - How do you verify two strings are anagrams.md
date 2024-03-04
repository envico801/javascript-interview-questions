========== Question ==========  

### How do you verify two strings are anagrams?  

========== Answer ==========  

An anagram is a word or phrase formed by rearranging all the letters of a
different word or phrase exactly once. For example, the anagrams of "eat" word
are "tea" and "ate".

You can split each word into characters, followed by sort action and later join
them back. After that you can compare those two words to verify whether those
two words are anagrams or not.

```javascript
function verifyAnagrams(word1, word2) {
  return word1.split('').sort().join('') === word2.split('').sort().join('');
}
console.log(verifyAnagrams('eat', 'ate'));
```

========== Id ==========  
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
