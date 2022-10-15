## flex item

### 1. align-self 屬性其實跟 align-items ⼀模⼀樣，差別在於 align-self 是只設定 item⾃⼰本⾝，所有的屬性值設定，都跟 align-items 是⼀樣的。
總共有以下六個屬性值可以設定，分別如下：
 - auto：預設值，表⽰跟 align-items 設定的屬性值⼀樣。
 - stretch：以⾃⼰所在的那排為基準，Items 會沿著交錯軸延展。
 - flex-start：以⾃⼰所在的那排為基準，將 Items 置於交錯軸的最⼀開始處。
 - flex-end：以⾃⼰所在的那排為基準，將 Items 置於交錯軸最後的地⽅。
 - center：以⾃⼰所在的那排為基準，將 Items 置於交錯軸的中間。
 - baseline：以⾃⼰所在的那排為基準，依據 baseline 基準線來做對⿑。

### 2. order
  - a、order 屬性設定在 Items 上，主要是⽤來設定 Items 沿著主軸出現的
  先後順序，預設值是 0，所以預設是按照所寫的 html 先後順序來出現。
  - b、可以將 order 設定其它的整數，那麼 Items 就會按照 order 所設定的值，
  由⼩到⼤來出現。

### 3. flex-grow
  - a、flex-grow 屬性設定在 Items 上，主要是⽤來設定當 container 在主軸上，還有多餘空間時，可以將多餘的空間，依比例分配給 flex-grow 設定正整數的 Items。
  - b、flex-grow 的預設值是 0，也就是預設上，此⾃動擴展的效果是關閉的。

### 4. flex-shrink
  - a、flex-shrink 屬性設定在 Items 上，主要是⽤來設定當 container 的空間，沿著主軸的⽅向，不夠容納 Items 時，那這些 Items 都預設上會平均地被壓縮。
  - b、flex-shrink 的預設值是 1，也就是預設上，此⾃動壓縮的效果是開啟的。當然可以設定其它的數值，來調⾼某些 Items 的壓縮比，例如
     flex-shrink = 6 代表壓縮到只剩原來的0.6倍

### 5. flex-basis
  - a、flex-basis 屬性設定在 Items 上，主要是⽤來設定寬度或⾼度，⽽這個寬度或⾼度，
  是依據主軸的⽅向來決定。
  - b、也就是當主軸在⽔平⽅向的時候，那 flex-basis 就是⽤來設定寬度；反之，當主軸是
  在垂直⽅向的時候，那 flex-basis 就是⽤來設定⾼度。
