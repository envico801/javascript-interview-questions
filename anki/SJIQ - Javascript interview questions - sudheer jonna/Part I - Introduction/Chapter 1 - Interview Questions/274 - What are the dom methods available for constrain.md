Q: What are the DOM methods available for constraint validation  
A: The below DOM methods are available for constraint validation on an invalid input,
1. checkValidity(): It returns true if an input element contains valid data.
2. setCustomValidity(): It is used to set the validationMessage property of an input element.
   Let's take an user login form with DOM validations
```javascript
function myFunction() {
  var userName = document.getElementById("uname");
  if (!userName.checkValidity()) {
    document.getElementById("message").innerHTML = userName.validationMessage;
  } else {
    document.getElementById("message").innerHTML = "Entered a valid username";
  }
}
```
<!--ID: 1693596698125-->

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