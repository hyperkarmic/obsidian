![[getter&setter.jpg]]


***
![[getter-setter-summary.jpg]]

***
Getters and setters are essential when working with classes to ensure proper encapsulation and control over access to class properties. ES6 provides a simple way to define them using the `get` and `set` keywords.
***
```javascript
class Rectangle { constructor(width, height) { this._width = width; this._height = height; } get width() { return this._width; } set width(value) { this._width = value; } get height() { return this._height; } set height(value) { this._height = value; } get area() { return this._width * this._height; } } const rect = new Rectangle(5, 10); console.log(rect.width); // Output: 5 console.log(rect.height); // Output: 10 console.log(rect.area); // Output: 50 rect.width = 7; rect.height = 14; console.log(rect.area); // Output: 98
```
***

#OOP #Encapsulation