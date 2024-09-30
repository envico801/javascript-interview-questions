========== Question ==========  

### How do you make an object iterable in javascript  

========== Answer ==========  

By default, plain objects are not iterable. But you can make the object iterable by defining a `Symbol.iterator` property on it.

Let's demonstrate this with an example,

```javascript
const collection = {
    one: 1,
    two: 2,
    three: 3,
    [Symbol.iterator]() {
        const values = Object.keys(this);
        let i = 0;
        return {
            next: () => {
                return {
                    value: this[values[i++]],
                    done: i > values.length,
                };
            },
        };
    },
};
const iterator = collection[Symbol.iterator]();
console.log(iterator.next()); // → {value: 1, done: false}
console.log(iterator.next()); // → {value: 2, done: false}
console.log(iterator.next()); // → {value: 3, done: false}
console.log(iterator.next()); // → {value: undefined, done: true}
```

The above process can be simplified using a generator function,

```javascript
const collection = {
    one: 1,
    two: 2,
    three: 3,
    [Symbol.iterator]: function* () {
        for (let key in this) {
            yield this[key];
        }
    },
};
const iterator = collection[Symbol.iterator]();
console.log(iterator.next()); // {value: 1, done: false}
console.log(iterator.next()); // {value: 2, done: false}
console.log(iterator.next()); // {value: 3, done: false}
console.log(iterator.next()); // {value: undefined, done: true}
```

========== Id ==========  
410

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#410-How-do-you-make-an-object-iterable-in-java

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
