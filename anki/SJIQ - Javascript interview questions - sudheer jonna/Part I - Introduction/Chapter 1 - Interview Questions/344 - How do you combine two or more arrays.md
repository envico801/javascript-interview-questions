========== Question ==========  

### How do you combine two or more arrays  

========== Answer ==========  

The concat() method is used to join two or more arrays by returning a new array containing all the elements. The syntax would be as below,

```javascript
array1.concat(array2, array3, ..., arrayX)
```

Let's take an example of array's concatenation with veggies and fruits arrays,

```javascript
var veggies = ['Tomato', 'Carrot', 'Cabbage'];
var fruits = ['Apple', 'Orange', 'Pears'];
var veggiesAndFruits = veggies.concat(fruits);
console.log(veggiesAndFruits); // Tomato, Carrot, Cabbage, Apple, Orange, Pears
```

========== Id ==========  
344

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#344-How-do-you-combine-two-or-more-arrays

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
