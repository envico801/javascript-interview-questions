Q: How do you check if a key exists in an object  
A: You can check whether a key exists in an object or not using three approaches,
1. **Using in operator:** You can use the in operator whether a key exists in an object or not
```javascript
"key" in obj;
```
and If you want to check if a key doesn't exist, remember to use parenthesis,
```javascript
!("key" in obj);
```
1. **Using hasOwnProperty method:** You can use `hasOwnProperty` to particularly test for properties of the object instance (and not inherited properties)
```javascript
obj.hasOwnProperty("key"); // true
```
1. **Using undefined comparison:** If you access a non-existing property from an object, the result is undefined. Let’s compare the properties against undefined to determine the existence of the property.
```javascript
const user = {
  name: "John",
};
console.log(user.name !== undefined); // true
console.log(user.nickName !== undefined); // false
```
<!--ID: 1693596712344-->

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