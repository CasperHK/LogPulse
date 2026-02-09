# LogPulse - 秒級多媒體事件紀錄器

LogPulse 是一款基於 Compose Multiplatform (CMP) 開發的跨平台行動應用程式（Android & iOS）。旨在幫助使用者在事件發生瞬間，以「秒」為單位精確捕捉時序，並支援豐富的多媒體附件（錄音、照片、文件），最後可匯出為 CSV/Excel 進行深度分析。

## ✨ 核心特色
* ⚡ 瞬時紀錄 (Instant Capture)： 點擊按鈕瞬間即鎖定 System.Timestamp，確保人類行動延遲降至最低。
* 📸 多媒體敘事： 一鍵夾帶錄音、現場照片或相關 PDF 文件，豐富事件情境。
* ⏳ 自動時差計算： 自動計算事件與事件之間的間隔時間（Duration），無需手動計算。
* 📊 分析導向導出： 支援一鍵匯出符合標準格式的 .csv 檔案，方便在 Excel 或 Google Sheets 進行數據分析。
* 📱 跨平台一致性： 採用 Kotlin 共享業務邏輯，在 Android 與 iOS 上擁有原生效能與一致體驗。

## 🛠 技術棧 (Tech Stack)
* UI 框架: Compose Multiplatform (CMP)
* 資料庫: SQLDelight (支援跨平台 SQL 存儲)
* 時間處理: Kotlinx Datetime
* 檔案處理: FileKit (處理圖片與文件選取)
* 多媒體: KMP-Record (跨平台錄音實作)
* 依賴注入: Koin

## 📂 導出資料結構範例
導出的 CSV 將包含以下欄位，方便後續分析：
| Timestamp (精確到秒)	| Event (事件描述)	| Duration (與上筆間隔) | Attachment (附件路徑) |
|---|---|---|---|
| 2023-10-27 14:00:05	| 啟動測試儀器 |	- | - |
| 2023-10-27 14:05:20	| 紀錄異常數據	| 00:05:15 | IMG_001.jpg | 
| 2023-10-27 14:06:10	| 語音備註回報	| 00:00:50 | REC_002.m4a |

## 🚀 快速上手 (開發者)
### 環境需求
1. Android Studio (最新穩定版) 或 IntelliJ IDEA
2. Xcode (用於 iOS 建置)
3. Kotlin Multiplatform Mobile (KMM) Plugin

### 安裝步驟
1. 複製專案：
```bash
git clone https://github.com
```

2. 運行 Android：
   直接在 Android Studio 選擇 composeApp 並按下 Run。
3. 運行 iOS：
   在 Android Studio 中選擇 iosApp 運行，或進入 iosApp 目錄執行 pod install 後使用 Xcode 開啟。

---

### 📝 授權協議 (License)
本專案採用 MIT 授權協議 - 詳見 LICENSE 檔案。

### 💡 未來路線圖 (Roadmap)
* 支援雲端備份與多裝置同步。
* 加入 AI 語音轉文字 (STT) 自動填充事件描述。
* 加入 AI 改善描述文筆。
* 自定義 Excel 模板導出。
