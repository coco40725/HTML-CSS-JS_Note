## This in JS
This 的情況:
1. 在 constructor 中， this 為新創建的對象
2. 當以函數的形式調用時，例如: fun(); this 就是 ``window``. ``window`` is the object of browser. Not the object of browser.

> Is the ``window`` equal to "global" object ? Not exactly, if you excutate the JS in the browser, then the root scope is the window. In that case, you can access the global object by using ``window.ObjectName``. 
However, if you execute the JS in Node.js, then the root scope would the ``global``. Thus, you should use ``global.ObjectName`` to access the global object. [ref](https://stackoverflow.com/questions/40043727/what-are-global-variables-and-window-variables-in-javascript)

3. 在方法中調用，例如: obj.fun() ， 誰調用此方法，誰就是 this

```javascript
// 情況 1 : Constructor
function Person(name, age, food){
    this.name = name;
    this.age = age;
    this.food = food;
    this.sayMyName = function (){
    alert("Tight Tight Tight!!");
    }
}

function Dog(name, home){
    this.name = name;
    this.home = home;
}

let p = new Person("Lily", 24, "cake");
let dog = new Dog("Jojo","New Taipei City");
alert(p instanceof Person);
alert(dog instanceof Person);

// 情況 2: 函數的形式調用
var value_var = 8;
let value_let = 9;
function showValue(){
    alert(this.value_var); // 等同於 alert(window.value); window 存著全域物件
    alert(this.value_let);
}
showValue(); //  return 8 and undefined

// 情況 3 : 調用方法
let name = "let變數";
function showName(){
    alert(this.name);
}
function Fruit(name){
    this.name = name;
    this.sayName = showName;
}

let fruit = new Fruit("Apple");
fruit.sayName(); // return Apple
```
