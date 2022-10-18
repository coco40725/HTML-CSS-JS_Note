## Prototype 原型
### 1. explicit prototype property (顯示原型) : prototype 
我們每創建一個 function 時，會同時內建一個屬性:  "prototype"。
- 若 function 是作為一般的 function，則調用 ``prototype`` 沒有什麼特別作用；
- 但若是作為 constructor，``prototype``  相當於是一個公共區域，可以定義共用的 method 與 attribute 等等，所有同一個類的 instance皆可以訪問到期對應的 prototype。
> Every object created by a constructor has an implicit reference (called the object’s prototype) to the value of its constructor’s “prototype” ----ECMAScript Language Specification

### 2. implicit prototype property (隱式原型) :  __ proto__
與 prototype 類似，``__ proto__`` 是屬於 "instance" 的屬性，而 ``prototype`` 是屬於 "function or constructor" 的屬性。 而instance.__ proto__ 所指向的對象正是 Function.prototype。

```javascript
function Person(name){
    this.name = name;
}
let p = new Person("Milk");
console.log(p.__proto__ === Person.prototype) // true
```

### 3. 流程解釋
請看以下程式碼:
```javascript
function Person(name){
    this.name = name;
}
let p = new Person("Milk");
p.toString();
```
p 本身並沒有定義 toString()，因此JS 會從 
1. p__proto__ 找，而 p.__ proto__ 會指向 Person.prototype，

    但是 Person.prototype 也沒定義 toString()，

2. 於是又會再往上找 p.__ proto__ .__ proto__ 也就是指向 Object.prototype，而在  Object.prototype 有預定義好許多方法，包含 toString(), valueOf() 等等。找到 toString() 方法。
(若在 Object.prototype 仍沒有找到方法，則會回傳 undefined，因為 Object prototype 沒有再更上層)

3. 此時就會調用 Object.prototype.toString().call(p).
> p.toString() 等價於 p.toString().call(p).

### 4. 常用method
* in 
使用 in 時檢查對象是否含有特定屬性時，若本身沒有但prototype有，依然會返回true。
```javascript
function Person(name){
    this.name = name;
}
Person.prototype.Country = "Taiwan";
let p = new Person("Milk");

console.log(p in "Country") // true
```

* hasOwnProperty()
檢查自身是否含有此屬性。
```javascript
function Person(name){
    this.name = name;
}
Person.prototype.Country = "Taiwan";
let p = new Person("Milk");

console.log(p.hasOwnProperty("Country")) // false
```
#### Reference
https://www.zhihu.com/question/34183746 
