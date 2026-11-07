# AGENTS.md

本倉庫是原創語言 susedifu（笛芙語）的資料庫，只有文件與字體，沒有程式碼：無 build／test／lint，改動後靠內容一致性檢查。

## 語言要點

- susedifu 意為「人的語言」：suse（話語）+ difu（人）
- 黏著構詞，新詞由詞根複合派生：`hosiwe` = hosi（空氣）+ we；`di-` 表人（dikabu 神、didabu 勞動者）
- 詞形一律小寫拉丁字母、無空格；架空世界觀詞彙（woza 魔法、mahasamu 首都）須保持同一設定風格

## 檔案

- `Documents/words.ods` — 詞彙表（64 條），詞源的唯一事實來源。ODS 本質是 zip，可用 `unzip -p Documents/words.ods content.xml` 直接讀取；資料列為 `編號 | 詞 | 詞（偶有差異）| 中文釋義`
- `Fonts/susedifu.ttf`、`Fonts/susedifu.svg` — 自創文字字體，非必要不修改

## 慣例

- 文檔一律用繁體中文（與詞表釋義一致）
- 直接 commit 到 `main` 並 push，無 PR 流程
