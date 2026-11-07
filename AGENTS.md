# AGENTS.md

本倉庫是原創語言 susedifu（笛芙語）的資料庫，只有文件與字體，沒有程式碼：無 build／test／lint，改動後靠內容一致性檢查。

## 語言要點

- susedifu 意為「人的語言」：suse（話語）+ difu（人）
- 黏著構詞，新詞由詞根複合派生：`hosiwe` = hosi（空氣）+ we；`di-` 表人（dikabu 神、didabu 勞動者）
- 詞形一律小寫拉丁字母、無空格；架空世界觀詞彙（woza 魔法、mahasamu 首都）須保持同一設定風格

## 檔案

- `Documents/words.toml` — 詞彙表（64 條），詞源的唯一事實來源；一詞一段（`[[word]]`），欄位說明見檔頭註解
- `Documents/swadesh-duibi.md` — Swadesh 207 詞對照與新詞草案（草案欄可改可棄，採納後才寫入 words.toml）
- `Documents/grammar/` — 語法文檔：phonology／morphology／syntax／examples；examples 為語法改動的回歸錨點
- `Fonts/susedifu.ttf`、`Fonts/susedifu.svg` — 自創文字字體，非必要不修改

## 慣例

- 倉庫元文檔（本檔）與對話用繁體中文；語言內容（words.toml、grammar/）一律英文，術語與標注縮寫採萊比錫慣例（Leipzig Glossing Rules），詞表保留 `zh` 欄對照原始中文釋義
- 直接 commit 到 `main` 並 push，無 PR 流程
