Q: How do you perform form validation using javascript  
A: JavaScript can be used to perform HTML form validation. For example, if the form field is empty, the function needs to notify, and return false, to prevent the form being submitted.  
Lets' perform user login in an html form,
```html
<form name="myForm" onsubmit="return validateForm()" method="post">
  User name: <input type="text" name="uname" />
  <input type="submit" value="Submit" />
</form>
```
And the validation on user login is below,
```javascript
function validateForm() {
  var x = document.forms["myForm"]["uname"].value;
  if (x == "") {
    alert("The username shouldn't be empty");
    return false;
  }
}
```
<!--ID: 1693596698306-->

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