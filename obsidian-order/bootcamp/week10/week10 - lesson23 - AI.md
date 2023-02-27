This is an exercise in object-oriented programming (OOP) using JavaScript. The main objective is to create a Store class that allows for different interactions within the store. Multiple classes are used with different purposes to practice the OOP paradigm. The exercise includes creating a Toy class with the Name, Price, and Count properties, a Store class with the Name, Stock, and Revenue properties, and two methods to handle the interactions of the store, replenishing the stock of a given toy, and processing the product sale.

The exercise also includes a package.json file, which includes Jest for testing, and an index.js file, which instantiates the objects.

The steps required to complete the exercise are detailed in plan.md, and the tests are detailed in store.test.js.

Key code snippets with explanations:

1.  Constructing the Toy class:

```javascript
class Toy {
  constructor(name, price, count) {
    this.name = name;
    this.price = price;
    this.count = count;
  }
}

```

Here, the Toy class is constructed with the Name, Price, and Count properties.

2.  Creating an array of toys:

```javascript
const toys = [
  new Toy("Action Figure", 14.99, 5),
  new Toy("Rare Toy", 17.99, 1),
];

```

An array of toys is created using the Toy class, with two toy objects with the given properties.

3.  Constructing the Store class:

```javascript
class Store {
  constructor(name, stock) {
    this.name = name;
    this.stock = stock;
    this.revenue = 0;
  }

```

The Store class is constructed with the Name, Stock, and Revenue properties.

4.  Creating a processProductSale method:

```javascript
processProductSale(productName) {
    const processItem = (toy) => {
      if (toy.name === productName) {
        if (toy.count > 0) {
          const price = toy.price;
          this.revenue += price;
          toy.count -= 1;
          console.log(`Name: ${productName} | Stock Remaining: ${toy.count}`);
        } else {
          console.log(`${productName} is not in stock!!`);
        }
      }
    };
    this.stock.forEach(processItem);
  }

```

The processProductSale method takes in the product's name as a parameter. If the toy is in stock, the method increases the store's revenue by the price of the toy and decreases the toy's count by one. If there is no more stock of the given toy, a message is displayed in the console and the toy's count is not decreased.

5.  Creating a replenishStock method:

```javascript
replenishStock(productName, count) {
    const processItem = (toy) => {
      if (toy.name === productName) {
        toy.count += count;
      }
    };
    this.stock.forEach(processItem);
  }

```

The replenishStock method takes in two parameters, the toy's name and the number of toys to be replenished. It increases the stock on a toy by the provided count parameter.

6.  Instantiating the objects:

```javascript
const Store = require("./store");
const { toys } = require("./toy");

const store = new Store("Big Al's Toy Barn", toys);

store.welcome();
store.processProductSale("Action Figure");
store.processProductSale("Action Figure");
store.processProductSale("Rare Toy");
store.processProductSale("Action Figure");

store.processProductSale("Rare Toy");

store.replenishStock("Rare Toy", 2);
store.processProductSale("Rare Toy");

store.printRevenue();

```

Here, the Store and Toy classes are imported, and the store object is instantiated with the given name and