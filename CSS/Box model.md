## Box model
1. **margin**: 距離，border往外的距離；衍生屬性: margin-top/margin-left/margin-bottom/margin-right
2. **border**: 邊框厚度；衍生屬性: border-top/border-left/border-bottom/border-right
3. **padding**: 距離，content與 border之間的距離；衍生屬性: padding-top/padding-left/padding-bottom/padding-right
4. **content**: 內容物

<img src="https://codesource.io/static/fcbb43524320ed9c5e46a1966ff51659/box-sizing.png">

### 長度設定方式:
1. [margin/border/padding] : 上 右 下  左
2. [margin/border/padding] : 上下 左右
3. [margin/border/padding] : 上 左右 下

## box-sizing
box-sizing
  - 屬性值 border-box:  設定width與height時，針對 border + padding + content
  - 屬性值 content-box: 設定width與height時，僅針對content
