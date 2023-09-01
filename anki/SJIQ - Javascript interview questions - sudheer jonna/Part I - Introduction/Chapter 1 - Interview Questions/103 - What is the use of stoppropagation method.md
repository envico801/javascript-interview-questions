Q: What is the use of stopPropagation method  
A: The stopPropagation method is used to stop the event from bubbling up the event chain. For example, the below nested divs with stopPropagation method prevents default event propagation when clicking on nested div(Div1)
```javascript
<p>Click DIV1 Element</p>
<div onclick="secondFunc()">DIV 2
<div onclick="firstFunc(event)">DIV 1</div>
</div>
<script>
function firstFunc(event) {
alert("DIV 1");
event.stopPropagation();
}
function secondFunc() {
alert("DIV 2");
}
</script>
```
<!--ID: 1693596723569-->

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