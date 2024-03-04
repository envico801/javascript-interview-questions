========== Question ==========  

### How do you detect javascript disabled in the page  

========== Answer ==========  

You can use the `<noscript>` tag to detect javascript disabled or not. The code
block inside `<noscript>` gets executed when JavaScript is disabled, and is
typically used to display alternative content when the page generated in
JavaScript.

```javascript
<script type="javascript">
     // JS related code goes here
</script>
<noscript>
     <a href="next_page.html?noJS=true">JavaScript is disabled in the page. Please click Next Page</a>
</noscript>
```

========== Id ==========  
183

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#183-How-do-you-detect-javascript-disabled-in-t

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
