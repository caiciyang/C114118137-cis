# credit-dirty.csv 欄位規格

| 欄位 | 型別 | 格式／單位 | 合法範圍 | 識別欄位 |
|---|---|---|---|---|
| ID | 字串 | — | 非空、不重複 | 是 |
| AGE | 整數 | 歲 | 18–100 | 否 |
| MARITAL_STATUS | 類別 | — | single／married／divorced | 否 |
| PAY_0 | 整數 | 還款狀態代碼 | -2–9 | 否 |
| BILL_AMT1 | 數值 | 新台幣元 | — | 否 |
| default | 整數 | 0／1 | 0、1 | 否（目標變數） |
| signup_at | 時間 | ISO-8601 UTC | — | 否 |
| LEAK_FUTURE_DEFAULT | 整數 | 0／1 | 0、1 | 否 |

- 空值不算違反規格；空值另外計入 missing_rate。
- 輸出資料必須包含 ID、PAY_0、default。
