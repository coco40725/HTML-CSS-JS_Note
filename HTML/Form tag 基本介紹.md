## form tag 基本介紹
### 1. < form>
< form> : 將使用者輸入的資料，用form標籤 包起來，然後透過 < button>傳出去
- action: < form> 的屬性， 資料要傳去的網址
- method: < form> 的屬性，資料以甚麼形式傳出去，主要有 get (格式: action?資料1&資料2，例如: https://www.example?username=abc&password=123) / post(資料傳到FromData)


**以下介紹會包在 < form> 標籤內的常用標籤:**
#### 1.2 < input> 輸入框
- type : 屬性，輸入的文字類型: text / password / hidden / radio(勾選紐，常用於單選) / checkedbox(勾選方塊，常用於多選) / file (上傳檔案)
- placeholder : 屬性，顯示提示文字
- id : 屬性，該文字框的id
- value : 屬性，用來指定當你選到此選項後，會以甚麼value傳遞
- readonly : 屬性，唯讀
- disabled : 屬性，無法編輯
- checked: type=radio 時才有的屬性，預設勾選 
- name : 屬性，用來指定送出去的該筆資料要用什麼名稱當名字
- accept: type=file 時才有的屬性，用於限定上傳檔案的類型

#### 1.3 < label> :
時常搭配input一起使用
- for : 屬性，當點擊時，會去尋找 id = "username" 的物件。

#### 1.4 < textarea> 打字框
使用者可以自己拉大小
- rows: 屬性，text area 的高
- cols: 屬性，text area 的長
- 其餘屬性與 <input > 相同

#### 1.5 < select> 下拉選單

- multiple : 屬性，可複選的下拉選單
- < optgroup> : 子標籤，將 < option> 分群
  - label : 屬性，群名稱
  - < option> : 子標籤，選項
    - value : 屬性，用來指定當你選到此選項後，會以**甚麼value傳遞**
    - selected : 屬性，預設選擇

```html
<select multiple>
    <optgroup label="分群1">
        <option value="1">選項一</option>
        <option value="2" selected>選項二</option>
    </optgroup>
    <optgroup label="分群2">
        <option value="3">選項三</option>
        <option value="4">選項四</option>
        <option value="5">選項五</option>
    </optgroup>
</select>
```

#### 1.6  < button> : 一般按鈕
- type : 屬性，決定此按鈕的功能，button(一般按鈕) / submit (資料送出，form標籤內的資料會全部送到action的網址)

### 2. 使用 label 與 input 串聯兩者
* 方式1: 使用 < label for=""> 與 < input id=""> 

```html
<label for="username"> 帳號: </label>
<input type="text" placeholder="這裡是提示文字" id="username">
```

* 方式2: 將< input> 寫在 < label> 中
 
```html
<label >
    email:
    <input type="text" placeholder="第二種 input 與 label的搭配寫法" value="預設文字" >
</label>
```
