==================== Question ====================  

### How do you capture browser back button  

==================== Answer ====================  

The `beforeunload` event is triggered when the window, the document and its
resources are about to be unloaded. This event is helpful to warn users about
losing the current data and detect back button event.

```javascript
window.addEventListener('beforeunload', () => {
  console.log('Clicked browser back button');
});
```

You can also use `popstate` event to detect the browser back button.  
**Note:** The history entry has been activated using `history.pushState` method.

```javascript
window.addEventListener('popstate', () => {
  console.log('Clicked browser back button');
  box.style.backgroundColor = 'white';
});
const box = document.getElementById('div');
box.addEventListener('click', () => {
  box.style.backgroundColor = 'blue';
  window.history.pushState({}, null, null);
});
```

In the preceeding code, When the box element clicked, its background color
appears in blue color and changed to while color upon clicking the browser back
button using `popstate` event handler. The `state` property of `popstate`
contains the copy of history entry's state object.

==================== Id ====================  
378
<!--ID: 1707879807848-->

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#378-How-do-you-capture-browser-back-button

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
