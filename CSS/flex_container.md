## flex的相關功能 主要針對 container
### 1. flex-direction 
決定 Items 該如何排列
  - row：預設值。(參考圖⼀)
  - row-reverse：Items 會沿著主軸的反⽅向排列。(參考圖⼀)
  - column：主軸和交錯軸對調。(參考圖⼆)
  - column-reverse：主軸和交錯軸對調，Items 會沿著主軸的反⽅向排列。(參考圖⼆)

### 2. flex-wrap 
決定 Items 是否可以斷⾏
  - nowrap：預設值。代表即使 Items 數量過多，依然不會斷⾏，Container都會試圖去容納這些 Items 在同⼀個軸。
  - wrap：代表當 Items 數量過多，多到 Container 裝不下的時候，會斷⾏，斷⾏會延著交錯軸(Cross Axis)。
  - wrap-reverse：代表當 Items 數量過多，多到 Container 裝不下的時候，會斷⾏，斷⾏會延著交錯軸(Cross Axis)的反向。

### 3.justify-content 
屬性⽤來決定 Items 在沿著"主軸"的⽅向，該如何排列，總共有以下五個屬性值可以設定，分別如下：
 - flex-start：預設值，將 Items 置於主軸的最⼀開始處。
 - flex-end：將 Items 置於主軸最後的地⽅。
 - center：將 Items 置於主軸的中間。
 - space-between：Items 第⼀個要在主軸最⼀開始處，最後⼀個要在主軸的最後地⽅，然後平均分佈，每個 Item 之間，距離都⼀樣。
 - space-around：由以下的⽰意圖，來表⽰分佈的結果(以主軸在⽔平⽅向為例)：

  注意: justify-content - 控制主轴 上所有 flex 项目的对齐。 align-items - 控制交叉轴 上所有 flex 项目的对齐。

### 4. align-content
  - a、align-content 預設上不會有效，因為 flex-wrap 的預設值是 nowrap，即不允許斷⾏，所以
     Items 無法沿著交錯軸來排列。所以若要有效，要將 flex-wrap 改成 wrap 或 wrap-reverse。
  - b、align-content 屬性⽤來決定 Items 在沿著交錯軸的⽅向，該如何排列，總共有以下六個屬性值可以設定，分別如下：
     - stretch：預設值，Items 會沿著交錯軸延展。
     - flex-start：將 Items 置於交錯軸的最⼀開始處。
     - flex-end：將 Items 置於交錯軸最後的地⽅。
     - center：將 Items 置於交錯軸的中間。
     - space-between：Items 第⼀排要在交錯軸最⼀開始處，最後⼀排要在交錯軸的最後地⽅，然後各排 Items 之間平均分佈，距離都⼀樣。
     - space-around：沿著交錯軸，各排 Items 的周圍距離是⼀樣的，也就是各排 Items 的距離，會是最⼀開始和最後⾯的距離的兩倍⼤。

### 5. align-items
  align-items 屬性⽤來決定各 Items 之間，在沿著交錯軸的⽅向，該如何排列，總共有以下五個屬性值可以設定，分別如下：
  - stretch：預設值，以⾃⼰所在的那排為基準，Items 會沿著交錯軸延展。
  - flex-start：以⾃⼰所在的那排為基準，將 Items 置於交錯軸的最⼀開始處。
  - flex-end：以⾃⼰所在的那排為基準，將 Items 置於交錯軸最後的地⽅。
  - center：以⾃⼰所在的那排為基準，將 Items 置於交錯軸的中間。
  - baseline：以⾃⼰所在的那排為基準，依據 baseline 基準線來做對⿑，參考下圖：

