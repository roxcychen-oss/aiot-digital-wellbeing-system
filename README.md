<img width="800" height="385" alt="AIOT digital behavioral (1)" src="https://github.com/user-attachments/assets/36987e44-02c8-4d33-b1ef-0da598586147" />

# aiot-digital-wellbeing-system
AIoT Digital Wellbeing &amp; Behavioral Intervention Prototype
# 🛡️ AIoT 數位健康與行為干預系統 (Digital Wellbeing & Behavioral Intervention Prototype)

## 📌 專案背景與設計動機 (Problem Statement)
在資訊爆炸與眼球經濟的時代，現代人面對 YouTube 等串流平台的無限滾動與自動播放機制，容易陷入無意識的數位沉迷（Digital Addiction）。現有的防沉迷工具多半採用「事後限制」或「粗暴斷網」，往往引發使用者的反彈與焦慮。
本專案從 **產品經理 (PM) 與行為科學** 角度出發，設計一套結合前端即時監控、自動化工作流與遊戲化機制的 **「主動式行為干預系統」**，透過「認知中斷」與「目標解鎖」引導使用者重建健康的使用習慣。

---

## 📐 系統架構設計 (System Architecture)
本系統採用輕量化、模組化的全端與自動化架構，不依賴複雜的雲端付費服務，具備高度的可移植性與展示性：

```text
[ 前端介面：HTML5/JS 狀態機與計時器 ] 
       │
       ├──(滿指定秒數觸發 HTTP POST Webhook)──> [ n8n 自動化工作流引擎 (Asia/Taipei) ] 
       │                                            │
       │                                    (OAuth2 / Sheets API)
       │                                            ▼
[ 強制干預：智慧貪食蛇與護眼遮罩 ] <─────────── [ 雲端數據資料庫 (Google Sheets) ]
---

## ⚙️ 核心功能模組 (Core Features)

1. **多模態影音與專注時序監控**：
   * 內建精選、安全的嵌入式串流影音。
   * 背景靜默計時，並於關鍵時間節點（如 10 秒）透過 Webhook 向後端發送 telemetry（遙測數據）。
2. **強制行為干預機制 (Gamified Cognitive Interruption)**：
   * 當觀看時數達上限（如 20 秒）時，系統強制中斷串流、切斷音訊，並無縫切換至「智慧軌跡貪食蛇」遊戲介面。
   * **破關解鎖邏輯**：必須透過專注操作獲得 50 分，才能解鎖全螢幕「數位健康護眼遮罩」，迫使大腦從被動接收轉為主動思考。
3. **雲端數據閉環 (Data Loop)**：
   * 透過 n8n 自動化接收前端請求，即時將使用者行為數據（時間戳記、帳號、觀看時數）寫入 Google 雲端試算表，實現數據化管理。

---

## 🛠️ 技術棧 (Tech Stack)
* **前端介面 (Frontend)**：HTML5, CSS3, JavaScript (Canvas 2D 遊戲引擎、DOM 動態狀態機)
* **自動化後端 (Automation)**：n8n (Local Webhook Listener & Workflow Automation)
* **雲端與資料持久化 (Cloud & Storage)**：Google Sheets API, OAuth2 授權協議

---

## 🚀 專案展示與亮點 (Demo & Highlights)

* **設計亮點**：兼顧使用者體驗 (UX) 與行為科學，跳脫傳統冰冷的錯誤畫面，以「遊戲化挑戰」化解防沉迷機制的對立感。

* **動態操作展示**：[![Watch Demo](https://img.shields.io/badge/🎥_點擊觀看系統操作示範-Click_Here-blue?style=for-the-badge)](https://github.com/user-attachments/assets/10a3312b-330e-4226-9616-20ddd2d8f939)
