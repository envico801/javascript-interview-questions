Q: How do you detect caps lock key turned on or not  
A: The `mouseEvent getModifierState()` is used to return a boolean value that indicates whether the specified modifier key is activated or not. The modifiers such as CapsLock, ScrollLock and NumLock are activated when they are clicked, and deactivated when they are clicked again.  
Let's take an input element to detect the CapsLock on/off behavior with an example,
```html
<input type="password" onmousedown="enterInput(event)" />
<p id="feedback"></p>
<script>
  function enterInput(e) {
    var flag = e.getModifierState("CapsLock");
    if (flag) {
      document.getElementById("feedback").innerHTML = "CapsLock activated";
    } else {
      document.getElementById("feedback").innerHTML = "CapsLock not activated";
    }
  }
</script>
```
<!--ID: 1693596716011-->

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