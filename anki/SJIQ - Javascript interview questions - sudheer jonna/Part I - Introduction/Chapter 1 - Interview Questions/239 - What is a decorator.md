==================== Question ====================  

### What is a decorator  

==================== Answer ====================  

A decorator is an expression that evaluates to a function and that takes the
target, name, and decorator descriptor as arguments. Also, it optionally returns
a decorator descriptor to install on the target object. Let's define admin
decorator for user class at design time,

```javascript
function admin(isAdmin) {
   return function(target) {
       target.isAdmin = isAdmin;
   }
}
@admin(true)
class User() {
}
console.log(User.isAdmin); //true
 @admin(false)
 class User() {
 }
 console.log(User.isAdmin); //false
```

==================== Id ====================  
239

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#239-What-is-a-decorator

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
