```javascript
class Vehicle {  
 #color // private class field property  
 _sunroof = false // protected class field property  
  
 constructor(model, year, color) {  
  this.model = model // public property  
  this.year = year // public property  
  this.#color = color // private property  
  this._isEngineOn = false // protected property  
 }  
  
 // Private method  
 #startEngine() {  
  console.log(`Engine is started`)  
  this._isEngineOn = true  
 }  
  
 // Private method  
 #stopEngine() {  
  console.log(`Engine is stopped`)  
  this._isEngineOn = false  
 }  
  
 // Public method  
 turnOn() {  
  this.#startEngine()  
 }  
  
 // Public method  
 turnOff() {  
  this.#stopEngine()  
 }  
  
 // Static method  
 static honk() {  
  console.log(`Honk honk!`)  
 }  
  
 // Getter for private property  
 get color() {  
  return this.#color  
 }  
  
 // Setter for private property  
 set color(color) {  
  this.#color = color  
 }  
  
 // Getter for protected property  
 get isEngineOn() {  
  return this._isEngineOn  
 }  
  
 // Protected method  
 _openSunroof() {  
  console.log(`Opening sunroof`)  
  this._sunroof = true  
 }  
  
 // Protected method  
 _closeSunroof() {  
  console.log(`Closing sunroof`)  
  this._sunroof = false  
 }  
}
```

```javascript

class Car extends Vehicle {  
 constructor(model, year, color, doors, sunroof) {  
  super(model, year, color)  
  this._doors = doors // protected property  
  this._hasSunroof = sunroof  
 }  
  
 // Public method  
 openDoors() {  
  console.log(`Opening ${this._doors} doors`)  
 }  
  
 // Public method  
 closeDoors() {  
  console.log(`Closing ${this._doors} doors`)  
 }  
  
 // Overriding protected method  
 _openSunroof() {  
  if (this._hasSunroof) {  
   super._openSunroof()  
  } else {  
   console.log(  
    `The sunroof cannot be opened as this car does not have one`  
   )  
  }  
 }  
  
 // Overriding protected method  
 _closeSunroof() {  
  if (this._hasSunroof) {  
   super._closeSunroof()  
  } else {  
   console.log(  
    `The sunroof cannot be closed as this car does not have one`  
   )  
  }  
 }  
  
 // Public method accessing the protected method in the parent Vehicle class  
 toggleSunroof() {  
  if (!this._sunroof) {  
   this._openSunroof()  
  } else {  
   this._closeSunroof()  
  }  
 }  
}

```

```javascript
Car.honk() // Honk honk!  
  
// BMW  
const bmw = new Car("BMW", 2023, "black", 4, true)  
  
console.log(bmw)  
bmw.turnOn() // Engine is started  
console.log(bmw.isEngineOn) // true  
  
bmw.toggleSunroof() // Opening sunroof  
  
bmw.openDoors() // Opening 4 doors  
  
console.log(bmw.color) // black  
bmw.color = "white"  
console.log(bmw.color) // white  
  
bmw.turnOff() // Engine is stopped  
  
  
  
// LEXUS  
const lexus = new Car("Lexus", 1999, "yellow", 2, false)  
  
console.log(lexus)  
lexus.turnOn()  
console.log(lexus.isEngineOn) // true  
  
lexus.toggleSunroof() // The sunroof cannot be opened as this car does not have one  
  
lexus.openDoors() // Opening 2 doors  
  
console.log(lexus.color) // yellow  
lexus.color = "blue"  
console.log(lexus.color) // blue  
  
lexus.turnOff() // Engine is stopped
```
#js #class #examples 