# 小組作業 3：系統需求分析與使用案例

## 1. 需求分析

### (1) 功能性需求 (Functional Requirements)
* **FR-01 使用者身份驗證**：系統應提供使用者註冊、登入、登出及密碼重設之功能。
* **FR-02 資料管理功能**：使用者可以新增、檢視、編輯與刪除個人專案/任務資料。
* **FR-03 報表與統計查詢**：系統能根據使用者設定的條件匯出專案進度與統計圖表。

### (2) 非功能性需求 (Non-Functional Requirements)
* **NFR-01 效能需求 (Performance)**：系統在常態負載下，頁面響應時間應小於 2 秒。
* **NFR-02 安全性需求 (Security)**：所有使用者密碼與敏感資料傳輸皆須經過加密處理（如 SHA-256 / HTTPS）。
* **NFR-03 可用性與相容性 (Usability & Compatibility)**：系統介面須採用響應式網頁設計（RWD），支援桌機與行動裝置瀏覽。

---

## 2. 功能分解圖 (Functional Decomposition Diagram, FDD)

```mermaid
graph TD
    Root[系統核心功能] --> A[使用者管理]
    Root --> B[核心業務功能]
    Root --> C[報表與系統設定]

    A --> A1[帳號註冊與登入]
    A --> A2[個人資料修改]

    B --> B1[新增與編輯資料]
    B --> B2[資料查詢與篩選]

    C --> C1[統計圖表生成]
    C --> C2[系統參數設定]


Admin --> UC1
Admin --> UC4
