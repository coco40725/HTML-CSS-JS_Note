## 區別 var, let 與 const
Here we will give the brief for var, let, and const:
**var**: 聲明且賦值後，不一定會更改。
**let**: 聲明且賦值後，其值會再更改。
**const**: 聲明且賦值後，其值不再更改，即視為常數。

以下根據不同角度去看這三個關鍵字的差異:
### 1. Scope
* **var**: Variables declared with var are in the function scope.
* **let**: Variables declared as let are in the block scope.
* **const**: Variables declared as const are in the block scope.

**Function Scope**: When a variable is declared inside a function, it is only accessible within that function and cannot be used outside that function.

```javascript
showFun function(){
    var a = 9;
}

console.log(a); // this will return error!
```

**Block Scope**: A variable when declared inside the 

(1) if 

(2) switch conditions 

(3) for loop 

(4) while loops, 

are accessible within that particular condition or loop. To be consise the variables declared inside the curly braces are called as within block scope.

### 2. Hoisting
Hoisting means that you can define a variable before its declaration.

* **var**: Allowed
* **let**: Not allowed.
* **const**: Not allowed.

```javascript
// var
console.log(a); // Pass and return "undefined"
var a = 5;

// let
console.log(b); // ERROR!
let b = 0;

// const
console.log(c); //  ERROR!
const c = 0;
```

### 3. Redeclare the variable
* **var**: Allowed，但是會有 local variable 與 global variable 數值互相覆蓋的問題。

```javascript
// var
var a = 0;
var a = 9; // pass

/*
以下例子可以看出 由於 var沒有限制 redeclare 的scope，
導致 global variable "word"  
可以被 local variable "word" 取代。
*/

var word = "global";
if (true){
    var word = "local_instead";
}
console.log(wrod); // return "local_instead"
```

* **let**: Only allowed in different blocks or scopes，解決 var 的數值覆蓋與重複聲明的問題，let 會判定

(1) 聲明在不同blocks或scopes，且

(2) 相同變數名的變數 

是 **不同的** 變數。

```javascript
// let
let a = 0;
let a = 9; // ERROR!

/*
let 會判定 global variable "word"  與
local variable "word" 是兩個不同的值。
*/
let word = "global";
if (true){
    let word = "local_instead";
}
console.log(wrod); // return "global"
```


* **const**: Only allowed in different blocks or scopes。
```javascript
const c = 0;
const c = 10; // ERROR

const word = "global";
if (true){
    const word = "local_instead";
}
console.log(wrod); // return "global"
```


### 4. Reasign the value
* **var**: Allowed。
* **let**: Allowed。
* **const**: Not allowed。

