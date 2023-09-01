Q: How do you access web storage  
A: The Window object implements the `WindowLocalStorage` and `WindowSessionStorage` objects which has `localStorage`(window.localStorage) and `sessionStorage`(window.sessionStorage) properties respectively. These properties create an instance of the Storage object, through which data items can be set, retrieved and removed for a specific domain and storage type (session or local).  
For example, you can read and write on local storage objects as below
```javascript
localStorage.setItem("logo", document.getElementById("logo").value);
localStorage.getItem("logo");
```
<!--ID: 1693596719426-->

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