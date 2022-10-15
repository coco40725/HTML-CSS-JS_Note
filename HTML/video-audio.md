## video, audio 載入影片的標籤 < video>, < audio>
### 1. 常用屬性:
 1. **control**: 放入影片撥放鈕
 2. **poste**r: 預覽圖
 3. **autopla**y: 自動撥放，因為瀏覽器的規範，所以要多加 muted 才會執行
 4. **loop**: 重播
 5. **disablePictureInPicture**: 關閉子母畫面
 6. **controlsList="nodownload"** : 關閉下載按鈕
 7. **playsinline**: 手機撥放時，不進入全螢幕
 8. **muted**: 靜音
 9. **src**: 影音或影片來源
 
 ### 2. 加入< video>, < audio> 方式
 * 方式1: 直接利用src 屬性
 ```html
<video src="https://alldata.sgp1.digitaloceanspaces.com/videos/small.mp4"> </video>
<audio src="https://www.w3schools.com/jsref/horse.mp3"></audio>
```

 * 方式2. 於< video>, < audio> 兩個tag下，加入<>
 ```HTML
<video controls poster="https://picsum.photos/id/406/500/300" autoplay muted loop disablePictureInPicture playsinline>
    <source src="https://alldata.sgp1.digitaloceanspaces.com/videos/small.mp4" type="video/mp4">
    <source src="https://alldata.sgp1.digitaloceanspaces.com/videos/small.ogv" type="video/ogg">
    如果瀏覽器不支援 HTML5 video 標籤，就出現這裡的文字
</video>
<br>
<audio controls autoplay loop muted>
    <source src="https://www.w3schools.com/jsref/horse.mp3" type="audio/mpeg">
    <source src="https://www.w3schools.com/jsref/horse.ogg" type="audio/ogg">
    如果瀏覽器不支援 HTML5 audio 標籤，就出現這裡的文字
</audio>
```
