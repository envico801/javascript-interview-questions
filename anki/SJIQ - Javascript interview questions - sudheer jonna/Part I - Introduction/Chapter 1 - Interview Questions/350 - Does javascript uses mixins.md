========== Question ==========  

### Does javascript uses mixins  

========== Answer ==========  

Mixin is a generic object-oriented programming term - is a class containing methods that can be used by other classes without a need to inherit from it. In JavaScript we can only inherit from a single object. ie. There can be only one `[[prototype]]` for an object.

But sometimes we require to extend more than one, to overcome this we can use Mixin which helps to copy methods to the prototype of another class.

Say for instance, we've two classes `User` and `CleanRoom`. Suppose we need to add `CleanRoom` functionality to `User`, so that user can clean the room at demand. Here's where concept called mixins comes into picture.

```javascript
// mixin
let cleanRoomMixin = {
    cleanRoom() {
        alert(`Hello ${this.name}, your room is clean now`);
    },
    sayBye() {
        alert(`Bye ${this.name}`);
    },
};

// usage:
class User {
    constructor(name) {
        this.name = name;
    }
}

// copy the methods
Object.assign(User.prototype, cleanRoomMixin);

// now User can clean the room
new User('Dude').cleanRoom(); // Hello Dude, your room is clean now!
```

========== Id ==========  
350

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#350-Does-javascript-uses-mixins

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
