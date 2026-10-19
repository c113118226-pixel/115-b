# 小組作業 2：專題專案規劃與時程管理

## 1. 專案基本資訊
* **專題名稱**：線上德州撲克多人對戰與策略分析平台
* **專案時程**：2026/10/01 – 2026/12/21
* **繳交日期**：2026/10/09

---

## 2. 個別組員任務分配表

| 組員姓名 | 專案角色 / 職責 | 主要負責任務項目 |
| :--- | :--- | :--- |
| **藍士驊** | 專案管理與系統分析 | 專案進度管控、需求分析與收集、彙整專案報告 |
| **莊又任** | 系統分析與需求設計 | 繪製功能分解圖 (FDD) 與使用案例圖 (Use Case Diagram) |
| **龔宇謙** | 系統流程與介面設計 | 繪製系統環境圖與 DFD (Data Flow Diagram)、UI/UX 分鏡圖 (Storyboard) |
| **謝皓翔** | 物件導向與資料庫設計 | 繪製類別圖 (Class Diagram)、循序圖與實體關係圖 (ERD) |
| **王惟平** | 系統測試與簡報製作 | 系統功能測試與除錯、專題期初與期末報告簡報/影片製作 |

---

## 3. 專題甘特圖 (Gantt Chart)

```mermaid
gantt
    dateFormat  YYYY-MM-DD
    title 專題專案開發甘特圖 (2026/10/01 - 2026/12/21)

    section 需求與系統分析
    專案規劃與組員分工      :a1, 2026-10-01, 7d
    需求收集與功能分析      :a2, after a1, 10d
    使用案例圖與 FDD 繪製    :a3, after a2, 10d

    section 系統與資料庫設計
    繪製系統環境圖與 DFD    :b1, after a3, 10d
    類別圖與循序圖設計      :b2, after b1, 10d
    UI/UX 分鏡圖設計        :b3, after b2, 10d
    繪製 ERD 資料庫設計     :b4, after b3, 10d

    section 系統開發與期末報告
    系統整合與功能測試      :c1, after b4, 12d
    期末總結與簡報報告準備  :c2, 2026-12-15, 2026-12-21
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
