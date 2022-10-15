## Position
### 1. static
預設值，即該元素出現在文檔的常規位置，不會重新定位。

### 2. fixed 
以目前瀏覽器視窗定位，固定在瀏覽視窗的固定位置，不隨滾動捲軸拉動。
也就是很多廣告或彈出視窗的作法。

接著可以設定要固定在瀏覽器視窗的哪裡:
  - top: 距離上方
  - right:  距離右方
  - left:  距離左方
  - bottom: 距離下方

### 3. relative
元素與 static 位置相同，但可移動元素本身，一樣搭配top/ right/ left/ bottom，不會擠壓其他元素


### 4.absoulte
當此元素的positoin被定義成absoulte，此元素會從資料流中抽離，自己獨立一個層，
並且會去尋找 其 父元素且position不等於static 的元素作為其"參考元素" 來定義位置。若找不到非static父元素，則以整個視窗來參考位置
一樣可搭配top/ right/ left/ bottom。
           
### 5. sticky
當視窗捲動到該物件位置時，會依據對該物件所設定的 top 值來讓該物件呈現 fixed 在視窗的效果，有效範圍僅在父層空間

