# constructor - keyword
***
A constructor is required for every class. You may either declare it directly, like in the example above, or you can avoid explicit specification and JavaScript will add an empty and invisible constructor for you. When you explicitly specify a constructor, you may provide it zero or more parameters to use to initialize the member variables. You used an explicit class declaration in the previous class declaration. In some circumstances, a default initialization is quite acceptable. You may set a default value by putting a value in the constructor’s arguments, as demonstrated below:

``` javascript
class User {  
       constructor(firstName, lastName, email = “test@test.com”) {  
            this.firstName = firstName;  
            this.lastName = lastName;  
            this.email = email;  
       }  
       getFullName() {  
            return `${this.firstName} ${this.lastName}`;;  
       }  
       updateName(firstName, lastName) {  
           this.firstName = firstName;  
           this.lastName = lastName;  
       }  
}user = new User("Brendan", "Eich");   
console.log( user.getFullName());
```

#constructor #classes  #javascript #js 