## class 
html 的標籤屬性，表示"**樣式表名稱**"，故可以填複數個 class 名稱，以空格區隔開，格式如下:
```html
<標籤 class="a b c"> ... </標籤>
```
css 指定此classes，若要同時符合複數class，則以.區隔，格式如下:
```css
[標籤名，省略即不指定標籤].[class1].[class2]...[classk]{
    css內容
}

h1.title1{
   color: blueviolet !important;
}
```

## id
html 的標籤屬性，表示此元素的 "**唯一名稱**"，故只能有一個id名稱，格式如下:
```html
<標籤 id="a"> ... </標籤>
 ```
css 指定此id，格式如下:
```css
[標籤名，省略即不指定標籤]#[id1]{
    css內容
}

p#the_para{
   color: cornflowerblue;
}
```      

## css 優先權:
1. 後寫的會優先前寫的
2. 寫在html的style 會優先 寫在css的style
3. css當中，有!important，優先度最高
        
