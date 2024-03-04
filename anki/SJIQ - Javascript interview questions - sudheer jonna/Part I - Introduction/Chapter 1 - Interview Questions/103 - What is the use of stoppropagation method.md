========== Question ==========  

### What is the use of stopPropagation method  

========== Answer ==========  

The stopPropagation method is used to stop the event from bubbling up the event
chain. For example, the below nested divs with stopPropagation method prevents
default event propagation when clicking on nested div(Div1)

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

========== Id ==========  
103

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#103-What-is-the-use-of-stoppropagation-method

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
