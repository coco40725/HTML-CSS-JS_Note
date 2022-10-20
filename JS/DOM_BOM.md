 ## BOM vs DOM
 前端是透過 Javascript 去呼叫 BOM 和 DOM 提供的 API 來控制瀏覽器的行為跟網頁的內容。
 
 在瀏覽器上的 JavaScript 包含了：

* JavaScript 核心 (以 ECMAScript 標準為基礎)

* BOM (Browser Object Model，瀏覽器物件模型)

* DOM (Document Object Model，文件物件模型)

 ### BOM (Browser Object Model)

<img src="https://i.imgur.com/ipN8SI1.png" >
BOM

- 瀏覽器對象模型
- BOM可以使我們通過JS來操作瀏覽器
- 在BOM中為我們提供了一組對象，用來完成對瀏覽器的操作

BOM 對象:
1. **Window**: 代表的是整個瀏覽器的窗口，同時window也是網頁中的全局對象
2. **Navigator**: 代表的當前瀏覽器的信息，通過該對象可以來識別不同的瀏覽器
    * **火狐的userAgent**: Mozilla/5.0 (Windows NT 6.1; WOW64; rv:50.0) Gecko/20100101 Firefox/50.0
    * **Chrome的userAgent**: Mozilla/5.0 (Windows NT 6.1; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/52.0.2743.82 Safari/537.36
    * **IE8**: Mozilla/4.0 (compatible; MSIE 8.0; Windows NT 6.1; WOW64; Trident/7.0; SLCC2; .NET CLR 2.0.50727; .NET CLR 3.5.30729; .NET CLR 3.0.30729; Media Center PC 6.0; .NET4.0C; .NET4.0E)
    * **IE9**: Mozilla/5.0 (compatible; MSIE 9.0; Windows NT 6.1; WOW64; Trident/7.0; SLCC2; .NET CLR 2.0.50727; .NET CLR 3.5.30729; .NET CLR 3.0.30729; Media Center PC 6.0; .NET4.0C; .NET4.0E)
    * **IE10**: Mozilla/5.0 (compatible; MSIE 10.0; Windows NT 6.1; WOW64; Trident/7.0; SLCC2; .NET CLR 2.0.50727; .NET CLR 3.5.30729; .NET CLR 3.0.30729; Media Center PC 6.0; .NET4.0C; .NET4.0E)
    * **IE11**: Mozilla/5.0 (Windows NT 6.1; WOW64; Trident/7.0; SLCC2; .NET CLR 2.0.50727; .NET CLR 3.5.30729; .NET CLR 3.0.30729; Media Center PC 6.0; .NET4.0C; .NET4.0E; rv:11.0) like Gecko
    (在IE11中已經將微軟和IE相關的標識都已經去除了，所以我們基本已經不能通過UserAgent來識別一個瀏覽器是否是IE了)

3. **Location**: 代表當前瀏覽器的地址欄信息，通過Location可以獲取地址欄信息，或者操作瀏覽器跳轉頁面
4. **History**: 代表瀏覽器的歷史記錄，可以通過該對象來操作瀏覽器的歷史記錄 (由於隱私原因，該對象不能獲取到具體的歷史記錄，只能操作瀏覽器向前或向後翻頁，而且該操作只在當次訪問時有效)
5. **Screen**: 代表用戶的屏幕的信息，通過該對象可以獲取到用戶的顯示器的相關的信息

 ### DOM (Document Object Model)
 把一份 HTML 文件內的各個標籤，包括文字、圖片等等都定義成物件，而這些物件最終會形成一個樹狀結構，下面有一張示意圖可以參考。
 
 <img src="https://www.w3schools.com/js/pic_htmltree.gif">

1. **Document**: Document 就是指這份文件，也就是這份 HTML 檔的開端，所有的一切都會從 Document 開始往下進行。
2. **Element**: Element 就是指文件內的各個標籤，因此像是 ``<div>、<p>`` 等等各種 HTML Tag 都是被歸類在 Element 裡面。
3. **Text**: Text 就是指被各個標籤包起來的文字，舉例來說在 ``<h1>Hello World</h1> ``中， ``Hello World`` 被 ``<h1>`` 這個 Element 包起來，因此 ``Hello World`` 就是此 Element 的 Text
4. **Attribute** : Attribute 就是指各個標籤內的相關屬性。
