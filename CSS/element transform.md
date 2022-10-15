## Transform
對元素進行旋轉 縮放 偏移 傾斜 變形等效果

### 1. rotate: 
  - a、透過 transform 屬性的預設值是 none，可以設定 rotate 來將元素旋轉。例：transform: rotate(20deg);
  - b、透過 transform-origin 屬性，可以移動形變效果的中⼼點，預設是在中間， 寫法分別是⽔平⽅向和垂直⽅向，形式如下：transform-origin: 50% 50%;

### 2. scale:
  - a、透過 transform 屬性的預設值是 none，可以設定 scale 來將元素縮放。例：
      transform: scale(1.5);
      transform: scaleX(1.5); 這是只針對⽔平⽅向來縮放
      transform: scaleY(1.5); 這是只針對垂直⽅向來縮放
  - b、透過 transform-origin 屬性，可以移動形變效果的中⼼點，預設是在中間，寫法分別是⽔平⽅向和垂直⽅向，形式如下：transform-origin: 50% 50%;

### 3. translate:
  - a、透過 transform 屬性的預設值是 none，可以設定 translate 來將元素偏移。例：
      transform: translate(10px, 20px); 向右移動 10px、向下移動 20px。
      transform: translate(-50%, -50%); 向左移動⾃⼰寬度的⼀半、向上移動⾃⼰⾼度的⼀半。
      transform: translateX(10px);
      transform: translateY(10px);
  - b、可以透過 transform: translate(-50%, -50%); 來將元素移動到⽗元素的⽔平⽅向中間、垂直⽅向中間。

### 4. skew:
  - a、透過 transform 屬性的預設值是 none，可以設定 skew 來將元素傾斜。例：
          transform: skew(10deg, 20deg);
          transform: skewX(10deg);
          transform: skewY(20deg);
  - b、透過 transform-origin 屬性，可以移動形變效果的中⼼點，預設是在中間，寫法分別是⽔平⽅向和垂直⽅向，形式如下：transform-origin: 50% 50%;

### 5. 多種transform寫法: 
  如果想在⼀個元素上套⽤多種形變效果的話，直接以空格做區隔即可。寫法如下：
  ```CSS
  transform: scale(1.5) rotate(20deg);
  ```
  錯誤的寫法:
  ```CSS
      transform: scale(1.5)
      transform: rotate(20deg)
    /*scale(1.5) 會被rotate(20deg)覆蓋*/
  ```
     
