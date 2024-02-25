==================== Question ====================  

### How do you delete a cookie  

==================== Answer ====================  

You can delete a cookie by setting the expiry date as a passed date. You don't
need to specify a cookie value in this case.  
For example, you can delete a username cookie in the current page as below.

```javascript
document.cookie = 'username=; expires=Fri, 07 Jun 2019 00:00:00 UTC; path=/;';
```

**Note:** You should define the cookie path option to ensure that you delete the
right cookie. Some browsers doesn't allow to delete a cookie unless you specify
a path parameter.

==================== Id ====================  
40

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#40-How-do-you-delete-a-cookie

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
