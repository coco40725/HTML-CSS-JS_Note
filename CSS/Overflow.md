## overflow
   - visible：預設值，超出區域的內容，仍然可以看得到。
   - hidden：超出區域的內容，就會被遮掉看不到。
   - scroll：超出區域的內容，該元素會出現捲軸，滑動可看到內容；
             在 windows 上，預設即使內容沒有超出區域，仍會出現捲軸區域。
   - auto：跟 scroll 類似，差別在於，如果是在 windows 上，內容沒有超出區域，那就不會出現捲軸區域。

   另有 overflow-x、overflow-y 兩個屬性，是分別只針對⽔平⽅向、垂直⽅向來設定，屬性值的設定都跟 overflow ⼀樣。


## text-overflow
  - clip：預設值，⽂字以裁掉的⽅式處理。
  - ellipsis：內容超出區域的⽂字，以省略符號(...)來出現。
