Q: How do you avoid receiving postMessages from attackers  
A: Since the listener listens for any message, an attacker can trick the application by sending a message from the attacker’s origin, which gives an impression that the receiver received the message from the actual sender’s window. You can avoid this issue by validating the origin of the message on the receiver's end using the “message.origin” attribute. For examples, let's check the sender's origin [http://www.some-sender.com](http://www.some-sender.com) on receiver side [www.some-receiver.com](www.some-receiver.com),
```javascript
//Listener on http://www.some-receiver.com/
window.addEventListener("message", function(message){
if(/^http://www\.some-sender\.com$/.test(message.origin)){
console.log('You received the data from valid sender', message.data);
}
});
```
<!--ID: 1693596692892-->

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