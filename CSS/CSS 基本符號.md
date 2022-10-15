## CSS 符號
### 1. A,B : A標籤和標籤
```css
p,div{
  color: rgb(226, 43, 43);
}
```
### 2. A空格B : A標籤"內層"的所有B標籤
```css
div p{
  color: rgb(0, 13, 255);
}
```

### 3. A > B : A標籤內，其"第一層B"標籤 
```css
div > p{
      color: rgb(0, 13, 255);
}
```
### 4. A + B : A 標籤後的 (同層) 一個B標籤
```css
div + p{
  color: rgb(0, 13, 255);
}
```

### 5. * : 所有標籤
```css
*{
  color: rgb(0, 13, 255);
}
```

### 6. A ~ B :  A 標籤後的 (同層) 所有B標籤
```css
div~p{
  color: rgb(0, 13, 255);
} 
```
