Q: How do you create self string using special characters  
A: The self string can be formed with the combination of `[]()!+` characters. You need to remember the below conventions to achieve this pattern.
1. Since Arrays are truthful values, negating the arrays will produce false: ![] === false
2. As per JavaScript coercion rules, the addition of arrays together will toString them: [] + [] === ""
3. Prepend an array with + operator will convert an array to false, the negation will make it true and finally converting the result will produce value '1': +(!(+[])) === 1
   By applying the above rules, we can derive below conditions
```javascript
(![] + [] === "false" + !+[]) === 1;
```
Now the character pattern would be created as below,
```javascript
s               e               l               f
^^^^^^^^^^^^^   ^^^^^^^^^^^^^   ^^^^^^^^^^^^^   ^^^^^^^^^^^^^
(![] + [])[3] + (![] + [])[4] + (![] + [])[2] + (![] + [])[0]
^^^^^^^^^^^^^   ^^^^^^^^^^^^^   ^^^^^^^^^^^^^   ^^^^^^^^^^^^^
(![] + [])[+!+[]+!+[]+!+[]] +
(![] + [])[+!+[]+!+[]+!+[]+!+[]] +
(![] + [])[+!+[]+!+[]] +
(![] + [])[+[]]
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
(![]+[])[+!+[]+!+[]+!+[]]+(![]+[])[+!+[]+!+[]+!+[]+!+[]]+(![]+[])[+!+[]+!+[]]+(![]+[])[+[]]
```
<!--ID: 1693596689904-->

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript #Interview

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store