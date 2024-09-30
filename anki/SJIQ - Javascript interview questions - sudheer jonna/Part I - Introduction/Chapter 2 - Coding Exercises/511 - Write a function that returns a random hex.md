========== Question ==========  

### Write a function that returns a random HEX color  

========== Answer ==========  

```javascript
const HEX_ALPHABET = [
    '0',
    '1',
    '2',
    '3',
    '4',
    '5',
    '6',
    '7',
    '8',
    '9',
    'a',
    'b',
    'c',
    'd',
    'e',
    'f',
];
const HEX_PREFIX = '#';
const HEX_LENGTH = 6;
function generateRandomHex() {
    let randomHex = '';
    for (let i = 0; i < HEX_LENGTH; i++) {
        const randomIndex = Math.floor(Math.random() * HEX_ALPHABET.length);
        randomHex += HEX_ALPHABET[randomIndex];
    }
    return HEX_PREFIX + randomHex;
}
```

```javascript
const HEX_PREFIX = '#';
const HEX_RADIX = 16;
const HEX_LENGTH = 6;
function generateRandomHex() {
    return (
        HEX_PREFIX +
        Math.floor(Math.random() * 0xffffff)
            .toString(HEX_RADIX)
            .padStart(HEX_LENGTH, '0')
    );
}
```

========== Id ==========  
511

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#511-Write-a-function-that-returns-a-random-hex

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
