## background-image

### 1. 背景圖:
background-image: url()

### 2. 背景圖重複 background-repeat:
  - no-repeat : 不重複
  - repeat: 預設值，水平垂直方向重複出現
  - repeat-x: 水平重複
  - repeat-y: 垂直重複
  - space: 重複出現，但圖片之間有間隔
  - round : 重複出現，但圖片之間無間隔，會導致圖片扭曲

### 3. 背景圖大小 background-size
  - 80% : 圖片寬度 = 元素寬度*0.8; 圖片高度 = 圖片原來比例
  - 80% 50% : 圖片寬度 = 元素寬度*0.8; 圖片高度 = 元素高度*0.5
  - contain: 高度與寬度有一個變成100%，使圖片可以"完整呈現不被遮蔽
  - cover: 高度與寬度有一個變成100%，使圖片可以"占滿"元素，有可能圖片會超出去，這部分就看不到

### 4. 背景圖位置 background-position
  - 可控制的方向: 
      -  水平方向 : left center right
      -  垂直方向 : top center bottom
  - 50px 100px: 距離左側50px 上方100px
  - right 50px bottom 100px: 距離右側50px 下方100px
  - right center: 水平方向為右側底，垂直方向為中間


### 5. 背景圖固定模式 background-attachement
  - scroll : 背景圖隨著頁面滾動，元素內則不會
  - local : 元素區域內滾動的話，背景圖亦會滾動
  - fixed : 不會滾動，留意手機尚未必支援

### 6. 背景圖的顯示區域 background-origin
  - padding-box: 預設值，從padding開始顯示
  - border-box: 從border開始顯示
  - content-box: 從content開始顯示

### 7. 背景圖裁切 background-clip:
  - padding-box: padding以外的會切掉
  - border-box: 預設值，border以外的會切掉
  - content-box: content以外的會切掉

### 8. 背景線性漸層 linear-gradient，設定在background-image上
  - linear-gradient (to top|bottom|left|right, color1, color2,...)
  - linear-gradient (度數180deg, color1, color2,....)
      - 上 = 0deg; 右 = 90deg; 下 = 180deg; 左 = 270deg
  - linear-gradient(135deg, color1 50%, color2 50%)

同區域多背景設定，以逗號區開，寫在後面的會疊在後面
