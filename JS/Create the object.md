## Create the object in JavaScript
### Method 1: Using object literal
You can create an object using an object literal. An object literal uses ``{ }`` to create an object directly.
An object is created with a ``key:value`` pair.You can also define functions, arrays and even objects inside of an object. You can access the value of the object using dot . notation.
```javascript
let p = {
    name: "Mary",
    age: 24,
    food: ["Apple", "Cake"]

    greet: function MyFunction(){
        console.log("Hello World!!")
    },

    score: {
        math: 90,
        art: 78
    }
}
```

### Method 2: Using ``new Object()``
```javascript
// 第一種寫法:
let p = new Object()
p.name = "Mary";
p.age = 24;
p.greet = function(){
    console.log("Hello World!!")
}
p.score = {
    math: 90,
    art: 78
}


// 第二種寫法:
let p = new Object(
    {
    name: "Mary",
    age: 24,
    food: ["Apple", "Cake"]

    greet: function MyFunction(){
        console.log("Hello World!!");
     },

    score: {
        math: 90,
        art: 78
        }
    }
)

```

### Method 3: Create Constructor Function
In the following example, the ``Person()`` constructor function is used to create an object using the new keyword.
```javascript
function Person(name, age){
    this.name = name;
    this.age = age;
    this.food =  ["Apple", "Cake"];
    this. greet = function MyFunction(){
        console.log("Hello World!");
    };
    this.score = {
        math: 90,
        art: 78
    }
}

var mary = new Person("Mary", 78);
```

### Method 4: Using ``Object.create()``
Object.create() creates a new object, using an **existing object as the prototype** of the newly created object. This method is mainly used for **implementing inheritance**.
```javascript
Object.create(prototype[, propertiesObject])
```
