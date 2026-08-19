# Templates 設計規格（Notion / Google Sheets）

本文件提供 Day-200 Marketing OS 可用於建立 Notion 或 Google Sheets 模板的結構規格，供團隊自行建立專屬工作空間（需登入自己的 Notion / Google 帳號建立，本 I 不代為登入）。

## 1. Notion 模板結構建議

### Database：「Module Tracker」
| 欄位 | 類型 | 說明 |
|---|---|---|
| 模組編號 | Text | 對應 00-17 |
| 模組名稱 | Title | 如 PRODUCT_ANALYSIS |
| 狀態 | Select | 未開始 / 進行中 / 已完成 |
| 負責人 | Person | 團隊成員 |
| 優先度 | Select | 高/中/低 |
| 連結文件 | URL | 連到 GitHub 對應檔案 |
| 備註 | Text | 自由文字 |

### Database：「Competitor Intelligence Log」（對應模組 05）
| 欄位 | 類型 |
|---|---|
| 竞爭對手名稱 | Title |
| 監控日期 | Date |
| 動作描述 | Text |
| 媒體來源 | URL |
| 威脅等級 | Select（高/中/低）|
| 建議應對 | Text |

### Database：「KOL Collaboration Tracker」（對應模組 11）
| 欄位 | 類型 |
|---|---|
| KOL 名稱 | Title |
| 平台 | Select（IG/小紅書/拖音）|
| 粉絲數 | Number |
| 互動率 | Number (%) |
| 合作費用 | Number |
| 合作狀態 | Select |
| ROI | Formula |

## 2. Google Sheets 工具包建議結構

### Sheet 1：Module_Overview
列出 17 個模組、狀態、負責人、完成度（%）

### Sheet 2：Campaign_Planner
欄位：活動名稱、目標、受眾、渠道、預算、開始日期、結束日期、KPI、實際成果

### Sheet 3：Competitor_Matrix
欄位：竞爭對手、產品特點、定價、主要渠道、強項、弱項、我方差異化策略

### Sheet 4：KOL_ROI_Calculator
欄位：KOL 名稱、合作費用、曝光量、點擊/轉化量、CPM、CPA（公式自動計算）

### Sheet 5：Content_Calendar
欄位：日期、平台、內容類型（品牌/價值/互動）、狀態、連結

## 3. 建立步驟（供使用者自行執行）

1. 登入自己的 Notion 帳號，新建 Workspace 並根據上述 Database 結構手動建立
2. 登入 Google 帳號，在 Google Sheets 建立新檔案，根據上述 5 個 Sheet 結構建立標題列
3. 將建立完成的 Notion/Sheets 連結回填入本文件下方「實際連結」部分

## 4. 實際連結（待填寫）

- Notion 模板連結：`待填寫`
- Google Sheets 工具包連結：`待填寫`

---
*注：由於 Notion / Google Sheets 需要登入個人帳號才能建立檔案，本文件僅提供結構設計方案，需由使用者自行在自己帳號內建立。*
