## table tag  基本介紹

### 1. **< table>** : 表格的標籤

  - **< thead>** : 表格column name
    - **< tr>, table row** : 表格的第一列，所有這列要寫的東西寫在這裡
      - **< th>, table head**: 表格的內容，一個th 一格
  - **< tbody>** : 表格的主體內容
    - **< tr>, table row** : 表格的第一列，所有這列要寫的東西寫在這裡
      - **< td>, table data**: 表格的內容，一個td 一格
  - **< tfoot>** : 表格的尾部標題
    - **< tr>, table row** : 表格的第一列，所有這列要寫的東西寫在這裡
      - **< td>, table data**: 表格的內容，一個td 一格


```html
<table>
    <thead>
        <tr>
            <th>...</th>
        </tr>
    </thead>

    <tbody>
        <tr>
            <td>...</td>
        </tr>
    </tbody>

    <tfoot>
        <tr>
            <td>...</td>
        </tr>
    </tfoot>

</table>

```
### 2. < tr>, < td>, < th> 常用屬性:

- **rowspan**: row合併

- **colspan**: column合併
