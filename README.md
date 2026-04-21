# 智慧停車位預測系統：基於 DD-LSTM 的輕量化多特徵融合框架
> **Smart Parking Prediction System: A Lightweight Multi-feature Fusion Framework based on DD-LSTM**

[![Project Status: Proposal](https://img.shields.io/badge/Project%20Status-Proposal-blue.svg)](https://github.com/Hellowar12345/aiot_project_proposal)
[![Data Source: TDX](https://img.shields.io/badge/Data%20Source-TDX%20Open%20Data-orange.svg)](https://tdx.transportdata.tw/)

本專案旨在解決都會區「尋找停車位」造成的交通壅塞與時間成本問題。透過整合政府 TDX 即時 API、天氣數據與節假日特徵，提出 **DD-LSTM (Dual-Feature LSTM)** 預測框架，實現高精準度且輕量化的即時停車位預測系統。

---

## 🔍 研究動機與痛點 (Research Motivation)

根據相關數據查證與市場分析：
- **尋車痛點**：在六都市中心區域，平均每次停車前的尋車時間高達 **8–12 分鐘**。
- **交通影響**：根據 INRIX 2023 Global Traffic Scorecard，市區交通壅塞有 **30%** 是由尋找車位（Cruising for parking）所造成。
- **資料現況**：政府 TDX 平台擁有超過 5,000 個停車場資訊，但原始 API 存在雜訊（如剩餘車位數異常）且缺乏外部特徵整合。

---

## 🚀 核心技術：DD-LSTM 框架

本專案提出的 **DD-LSTM** (Dual-Feature Long Short-Term Memory) 具備以下三大創新切入點：

1. **多特徵融合 (Multi-feature Fusion)**：不同於傳統僅依賴歷史時序的模型，我們額外引入「天氣因子」與「節假日特徵」，有效捕捉日曆效應對停車行為的影響。
2. **資料清洗層 (Data Cleaning Layer)**：專門處理 TDX API 的邏輯異常（如：剩餘車位 > 總車位），確保模型輸入的高品質。
3. **輕量化部署 (Lightweight Deployment)**：捨棄高運算成本的空間圖神經網路 (GCNN)，優化時序模型結構，使其適合即時 API 推論與行動端部署。

---

## 🏗️ 系統架構 (System Architecture)

系統分為四個核心層級：
- **Layer 1: Data Acquisition** - 介接 TDX API 獲取即時與歷史停車數據。
- **Layer 2: Preprocessing** - 進行去雜訊、歸一化及外部特徵（氣象、日曆）整合。
- **Layer 3: Model Engine** - DD-LSTM 核心預測模型，處理時序依賴與特徵權重。
- **Layer 4: Application/API** - 提供 RESTful API 供前端或行動 App 呼叫，顯示未來預測趨勢。

---

## 📚 文獻回顧 (Related Work)

本研究參考並優化了以下 5 篇關鍵文獻之技術：

| 技術來源 | 方法論 | 優點 | 本研究之優化點 |
| :--- | :--- | :--- | :--- |
| **Badii et al. (2018)** | 傳統 ML + 開放資料 | 高可解釋性 | 引入 LSTM 捕捉長期時序依賴 |
| **Awan et al. (2020)** | RF / KNN 比較 | 準確率達 86.5% | 整合天氣與節假日外部特徵 |
| **Mishra (2021)** | 端對端 LSTM | 捕捉時序依賴 | 解決多停車場即時 API 介接問題 |
| **Yang et al. (2019)** | GCNN + LSTM | 空間時序聯合建模 | **輕量化優化**，降低訓練與部署成本 |
| **MDPI IJGI (2024)** | MAT-LSTM (Attention) | 強化特徵擷取 | 降低推論延遲，實現即時預測 |

---

## 📂 Repository Structure

```text
.
├── docs/
│   ├── Smart_Parking_Prediction.pdf   # Optimized Slide Deck (via NotebookLM)
│   ├── Group2_Project_Proposal.pptx   # Original Design (via Claude Design)
│   └── DEVELOPMENT_LOG.md             # Development History & Data Verification
├── src/                               # Source Code (In Development)
├── data/                              # Sample Data & Scripts (In Development)
└── README.md                          # Project Documentation
```

---

## 🛠️ Future Roadmap

1. [ ] **Phase 1**: TDX API Automation & Database Integration.
2. [ ] **Phase 2**: DD-LSTM Model Implementation & Hyperparameter Tuning.
3. [ ] **Phase 3**: Web Dashboard for Predictive Heatmap Visualization.

---
*This project is a Group 2 Proposal for the AIOT course.*
