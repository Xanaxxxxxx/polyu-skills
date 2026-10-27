# PolyU Skills

供 PolyU Computing 本科生使用的個人 Codex skill，整合 Notion 學業管理、Canvas／Blackboard 查詢、Daily Brief、講義學習和校園聯絡資料。日常回覆使用繁體中文，日期及時間使用 `Asia/Hong_Kong`；英文授課科目的筆記預設以英文撰寫。

## 功能

| 模式 | 用途 | 例子 |
| --- | --- | --- |
| 查詢 | 查閱需要的學業記錄、課程及截止日期 | 最近有哪些 assignment？ |
| 指定同步 | 只同步指定項目，或按要求更新個人進度 | 同步 HCI group project |
| Daily Brief | 收集過去 24 小時電郵與未來 21 天 LMS 概覽，更新相關 Notion 記錄 | 執行完整 Daily Brief |
| 學習 | PDF 大綱、逐章講解、互動 lab 輔導及按要求儲存筆記 | 解釋這份 PDF 的第二章 |
| 聯絡資料 | 查證目前導師及校園服務的聯絡方式 | 我的 Game Design lecturer 怎麼聯絡？ |

一般程式設計作業不會觸發資料同步。查詢、講解及聯絡資料查找不會自動變成完整 Daily Brief。

## 目錄

- [SKILL.md](SKILL.md)：入口、模式選擇及共用限制。
- [references/workspace.md](references/workspace.md)：個人 Notion 位置與可選的 COMP4122 筆記參考。
- [references/query.md](references/query.md)：最小範圍的唯讀查詢。
- [references/sync.md](references/sync.md)：指定項目同步及明確要求的進度更新。
- [references/sync-policy.md](references/sync-policy.md)：去重、欄位、來源及保留規則。
- [references/daily-brief.md](references/daily-brief.md)、[輸出格式](references/daily-brief-output.md)：完整簡報流程。
- [references/lecture-study.md](references/lecture-study.md)、[圖學例子](references/lecture-study-graphics-examples.md)：學習與筆記流程。
- [references/contacts.md](references/contacts.md)：導師及服務聯絡資料；`campus-guide.md` 保留作舊連結相容入口。

## 安裝與設定

本儲存庫根目錄就是 `polyu` skill。新環境可將整個儲存庫放在專案的 `.agents/skills/polyu/`；現有環境先保留自己的設定，再合併更新。

需要在 Codex 連接 Notion、Gmail 及 LMS。LMS 使用已安裝的 `lms-cli:lms-query` skill，並選用 `canvas-polyu-edu-hk` profile；PDF 工作需要可用的 PDF skill。實際工具名稱與參數以當前環境提供的工具為準。

此版本包含個人 Notion 連結及學期規則，儲存庫設為私人。供其他帳戶使用時，先替換 `references/workspace.md` 中的位置，再核對同步規則中的學年、修讀要求、欄位和 LMS profile。修改這些設定不會建立資料庫或授權存取。

## 資料處理界線

- LMS 唯讀；不提交作業、不開始考試、不發送訊息。
- Gmail 不標記已讀、不回覆；此流程不使用 Google Calendar。
- 保留手動進度、筆記、來源歷史、公式、rollup 及 Notion views。
- Notion `Events.Date` 是結構化日期的依據；電郵與 LMS 是原始證據。
- 不將密碼、token、cookies、MFA 或課程匯出檔存入儲存庫。

## 維護

工作流程與 schema 規則集中在 skill 及 references；排程提示只引用共用規則。僅完整 Daily Brief 更新 dashboard 的檢查時間。修改後檢查相對連結、skill 格式，以及是否保留既有的讀寫範圍。
