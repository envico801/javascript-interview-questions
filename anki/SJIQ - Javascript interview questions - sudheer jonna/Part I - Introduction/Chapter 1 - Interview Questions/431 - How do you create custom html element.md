========== Question ==========  

### How do you create custom HTML element?  

========== Answer ==========  

The creation of custom HTML elements involves two main steps,

1. **Define your custom HTML element:** First you need to define some custom
    class by extending HTMLElement class.

    After that define your component properties (styles,text etc) using
    `connectedCallback` method.

    **Note:** The browser exposes a function called `customElements.define`
    inorder to reuse the element.

    ```javascript
    class CustomElement extends HTMLElement {
      connectedCallback() {
        this.innerHTML = 'This is a custom element';
      }
    }
    customElements.define('custom-element', CustomElement);
    ```

2. **Use custome element just like other HTML element:** Declare your custom
    element as a HTML tag.

```javascript
    <body>
         <custom-element>
    </body>
```

========== Id ==========  
431

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#431-How-do-you-create-custom-html-element

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
