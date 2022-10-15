## CSS的 display 四個屬性值
1. block: 區塊元素，例如< div>< p>，會開始於新的一行，可設定width, height
2. none: 元素消失，但仍存在於程式碼
3. inline-block: 行內區塊元素，接著該行排序，可設定width, height
4. inline: 接著該行排序，不可設定width, height
5. flex 

不同的display 可以使用的屬性不相同，例如: display: block 可設定width, height；但 display: inline 不可以，
因此在調用屬性前可以先確認該屬性應用在哪些element上。
https://www.w3.org/TR/2011/REC-CSS2-20110607/propidx.html

### 其他相關屬性
1. float: 用來定義元素的浮動，可以設定為靠左浮動或靠右浮動，通常需要搭配clear來將解決父層的高度低於浮動元素的高度
2. clear: 使元素的左/右/左右 沒有浮動元素
