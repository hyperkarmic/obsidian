# fetch
![[fetch.png]]
***

![[api-call-cheatsheet.webp]]
***
![[fetch.jpg]]
***
using "GET"
```javascript
fetch('https://api.example.com/data') .then(response => response.json()) .then(data => console.log(data));
```
***
using "POST"

```javascript
fetch('https://api.example.com/data', { method: 'POST', headers: { 'Content-Type': 'application/json' }, body: JSON.stringify({ name: 'John', age: 25 }) }) .then(response => response.json()) .then(data => console.log(data));
```

***
using "PUT"

```javascript
fetch('https://api.example.com/data/123', { method: 'PUT', headers: { 'Content-Type': 'application/json' }, body: JSON.stringify({ name: 'John', age: 26 }) }) .then(response => response.json()) .then(data => console.log(data));
```
#fetch #js #javascript 
***
using "DELETE"

```javascript
fetch('https://api.example.com/data/123', { method: 'DELETE' }) .then(response => console.log('Data deleted'));
```