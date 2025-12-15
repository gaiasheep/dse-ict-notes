# Module A: Information Processing (資訊處理)

## [cite_start]1. Data Processing Cycle (數據處理週期) [cite: 3251]

### [cite_start]Data vs. Information [cite: 3248]
* **Data (數據):** Raw facts and figures without context. (e.g., "170", "M") [cite_start][cite: 3318]
    * *中文:* 原始的事實和數字，沒有語境。
* [cite_start]**Information (資訊):** Processed data that is meaningful for decision making. [cite: 3328]
    * *中文:* 經處理的數據，對決策有意義。

### [cite_start]The GIGO Principle [cite: 3250]
> **Keyword:** **GIGO (Garbage In, Garbage Out)**
* [cite_start]If input data is incorrect (garbage), output will be incorrect regardless of processing quality. [cite: 3434]
* *中文:* 無用輸入，無用輸出。

### [cite_start]Verification vs. Validation (數據控制) [cite: 3311]

| Feature | Data Verification (核對) | Data Validation (有效性檢驗) |
| :--- | :--- | :--- |
| **定義** | [cite_start]Ensuring data is copied correctly from source. [cite: 3540] | [cite_start]Checking if data is reasonable/follows rules. [cite: 3582] |
| **方法** | [cite_start]**Double Entry** (雙重輸入) [cite: 3542]<br>**Visual Check** (目測) | [cite_start]**Range Check** (範圍檢查) [cite: 3616][cite_start]<br>**Format Check** (格式檢查) [cite: 3600][cite_start]<br>**Check Digit** (檢查數位) [cite: 3624] |
| **例子** | [cite_start]Typing password twice. [cite: 3545] | [cite_start]Checking if Month is 1-12. [cite: 3619] |

---

## 2. Data Representation (數據表達)

### [cite_start]Number Systems [cite: 1473]
* [cite_start]**Binary (二進制):** Base 2 (0, 1). [cite: 1501]
* **Hexadecimal (十六進制):** Base 16 (0-9, A-F). [cite_start]Used to simplify binary representation. [cite: 1537]

### [cite_start]Two's Complement (二補碼 - 負整數) [cite: 4043]
Used to represent **negative integers**.
1.  Invert bits (0→1, 1→0).
2.  Add 1.
* [cite_start]**Range (n-bit):** $-2^{n-1}$ to $+2^{n-1}-1$ [cite: 4074]
* [cite_start]**Overflow Error:** Occurs when result exceeds storage capacity. [cite: 3833]

### [cite_start]Multimedia: Bitmap vs. Vector [cite: 2375]

| Feature | Bitmap (點陣圖) | Vector (向量圖) |
| :--- | :--- | :--- |
| **Unit** | [cite_start]Pixels (像素) [cite: 2313] | [cite_start]Mathematical formulas [cite: 2362] |
| **Scaling** | [cite_start]Jagged/Pixelated (失真) [cite: 2316] | [cite_start]No quality loss (不失真) [cite: 2364] |
| **File Size** | Large (Resolution × Depth) | Small (Complexity based) |
| **Formats** | [cite_start]BMP, JPG, PNG, GIF [cite: 2319] | [cite_start]SVG, WMF, AI [cite: 2368] |

---

## [cite_start]3. Database (數據庫) & SQL [cite: 718]

### [cite_start]SQL Syntax (必背語法) [cite: 993]

```sql
SELECT Field1, Field2       -- 選擇欄位
FROM TableName              -- 來自表格
WHERE Condition             -- 篩選條件 (e.g. Salary > 20000)
GROUP BY Field              -- 分組 (配合 COUNT, SUM 使用)
ORDER BY Field DESC;        -- 排序 (ASC=升序, DESC=降序)
```

### Key Operators (常用運算符)
* **Text Matching:** `LIKE 'K%'` (Starts with K), `LIKE '%A%'` (Contains A)
* **Range:** `BETWEEN 10 AND 20`
* **Null Check:** `IS NULL` / `IS NOT NULL`
* **Logic:** `AND`, `OR`, `NOT`

---

## 4. Spreadsheet (電子試算表)

### Essential Functions (常用函數)

* **`=VLOOKUP(lookup_value, table_array, col_index_num, FALSE)`**
    * *Note:* Use `FALSE` for exact match (e.g., Student ID).
    * *注意:* 必須使用 `FALSE` (0) 進行準確配對。

* **`=IF(condition, value_if_true, value_if_false)`**
    * Logic control (如果...就...否則...).

* **`=COUNTIF(range, criteria)`**
    * Counts cells that meet a condition.

* **`=SUMIF(range, criteria, sum_range)`**
    * Sums cells that meet a condition.

### Pivot Table (樞紐分析表)
* **Usage:** Used for summarizing large datasets dynamically.
* **Feature:** Does **not** change original data.
* **Key Fields:**
    * **Row (列)**
    * **Column (欄)**
    * **Data/Values (值)**
    * **Page/Filter (篩選)**
