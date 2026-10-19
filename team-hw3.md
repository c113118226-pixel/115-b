# 小組作業 3：需求分析與系統架構設計

* **專題名稱**：線上德州撲克多人對戰與策略分析平台
* **繳交日期**：2026/10/19

---

## 1. 系統需求分析

### (1) 功能性需求 (Functional Requirements)
1. **玩家對戰與房間管理**：系統須支援玩家建立房間、加入對戰、盲注設定與實時撲克發牌與下注流程。
2. **手牌歷史與數據記錄**：系統須自動記錄每場對局的過程（包括手牌、下注動作、池底大小），並提供玩家隨時查閱歷史牌局。
3. **策略分析與勝率計算**：系統須提供 EV (Expected Value) 勝率計算與 VPIP/PFR 等玩家風格數據分析，協助玩家檢討對局策略。

### (2) 非功能性需求 (Non-Functional Requirements)
1. **效能與實時性**：發牌與玩家下注動作的網路延遲 (Latency) 需低於 500 毫秒，以確保即時連線對戰順暢。
2. **安全性與公正性**：洗牌演算法須具備密碼學等級的隨機性 (RNG)，且玩家通訊須加密，防止看牌外掛與資料竄改。
3. **可用性與擴充性**：系統服務可用性 (Availability) 須達到 99.5% 以上，並能在熱門時段支援至少 1000 名玩家同時線上對戰。

---

## 2. 功能分解圖 (Functional Decomposition Diagram, FDD)

```mermaid
graph TD
    Root[線上德州撲克對戰與策略分析平台]
    
    Root --> Module1[1. 帳號與玩家管理]
    Module1 --> M1_1[1.1 註冊與登入]
    Module1 --> M1_2[1.2 個人資料管理]
    Module1 --> M1_3[1.3 籌碼管理]

    Root --> Module2[2. 多人對戰系統]
    Module2 --> M2_1[2.1 房間大廳與配對]
    Module2 --> M2_2[2.2 牌局邏輯與發牌]
    Module2 --> M2_3[2.3 下注與池底結算]

    Root --> Module3[3. 策略分析系統]
    Module3 --> M3_1[3.1 牌局歷史回放]
    Module3 --> M3_2[3.2 勝率即時計算]
    Module3 --> M3_3[3.3 玩家數據統計 VPIP/PFR]
```

```mermaid
flowchart TD
    T1["1. 專案規劃與分工<br/>(10/01 - 10/07)"] --> T2["2. 需求收集與功能分析<br/>(10/08 - 10/17)"]
    T2 --> T3["3. 劃出使用案例圖與 FDD<br/>(10/18 - 10/27)"]
    T3 --> T4["4. 繪製 DFD 系統流程圖<br/>(10/28 - 11/06)"]
    T4 --> T5["5. 類別圖與循序圖設計<br/>(11/07 - 11/16)"]
    T5 --> T6["6. UI/UX 分鏡圖設計<br/>(11/17 - 11/26)"]
    T5 --> T7["7. ERD 資料庫架構設計<br/>(11/17 - 11/26)"]
    T6 --> T8["8. 系統整合與展示<br/>(11/27 - 12/14)"]
    T7 --> T8
    T8 --> T9["9. 期末報告準備與展示<br/>(12/15 - 12/21)"]

    %% 標示關鍵路徑
    style T1 fill:#e1f5fe,stroke:#0288d1,stroke-width:2px
    style T2 fill:#e1f5fe,stroke:#0288d1,stroke-width:2px
    style T3 fill:#e1f5fe,stroke:#0288d1,stroke-width:2px
    style T4 fill:#e1f5fe,stroke:#0288d1,stroke-width:2px
    style T5 fill:#e1f5fe,stroke:#0288d1,stroke-width:2px
    style T6 fill:#e1f5fe,stroke:#0288d1,stroke-width:2px
    style T8 fill:#e1f5fe,stroke:#0288d1,stroke-width:2px
    style T9 fill:#e1f5fe,stroke:#0288d1,stroke-width:2px
```
