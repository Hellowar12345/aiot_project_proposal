# 專案對話紀錄

**專案名稱：** DL-introduction — 智慧停車位預測系統簡報  
**日期：** 2026-04-21  

---

## 對話摘要

### 1. 需求確認

**使用者：** 想製作一份報告/簡報，主題為透過政府公開平台提供的即時車位、歷史資料、其他特徵預測停車位（課程 Part A 作業）。

**確認細節：**
- 口頭報告時長：透過 NotebookLM 生成約 10 分鐘介紹
- 語言：繁體中文為主，專有名詞用英文
- 預測方法：由 AI 決定（採用 DD-LSTM）
- 資料來源：政府停車場即時 API（交通部）、TDX 平台
- 文獻數量：5 篇
- 視覺風格：淺色背景（學術/簡潔）

---

### 2. 簡報製作

製作 15 張投影片，結構如下：

| 張數 | 內容 |
|------|------|
| 01 | 封面 |
| 02 | 目錄 |
| 03 | Introduction 章節頁 |
| 04 | A — 研究動機（統計數據） |
| 05 | B+C — 挑戰與痛點實例 |
| 06 | D — 提出方案（DD-LSTM） |
| 07 | E+F — 評估方式與主要貢獻 |
| 08 | Related Work 章節頁 |
| 09 | 文獻回顧 ①②③ |
| 10 | 文獻回顧 ④⑤ |
| 11 | Article Summary Table |
| 12 | Proposed Design 章節頁 |
| 13 | 系統架構（四層式架構圖） |
| 14 | 資料流 Data Flow |
| 15 | 核心貢獻（結尾頁） |

---

### 3. 文獻真實性確認

**使用者詢問：** 文獻引用數字是否真實？

**說明：** 初版文獻為 AI 生成（虛構），經搜尋後更新為以下 5 篇**真實論文**：

| # | 論文 | 方法 | 連結 |
|---|------|------|------|
| ① | Badii et al., IEEE Access, 2018 | 開放資料 + 傳統 ML | https://doi.org/10.1109/ACCESS.2018.2864157 |
| ② | Awan et al., Sensors, 2020 | ML 模型比較（RF 86.5%）| https://doi.org/10.3390/s20010322 |
| ③ | Mishra & Deshpande, Springer ICTIS, 2021 | LSTM 時序預測 | https://doi.org/10.1007/978-981-15-7062-9_59 |
| ④ | Yang et al., arXiv, 2019 | GCNN + LSTM 空間時序 | https://arxiv.org/abs/1901.06758 |
| ⑤ | MAT-LSTM, MDPI IJGI, 2024 | Multi-head Attention + LSTM | https://www.mdpi.com/2220-9964/13/5/151 |

> ⚠️ **請自行點擊連結確認論文內容與簡報描述一致。**

---

### 4. 簡報連結功能

文獻卡片上加入藍色可點擊連結，點擊後直接開啟原始論文頁面。

---

### 5. 匯出 PPTX

匯出為 `Parking_Prediction_Deck.pptx`（446 KB），共 15 張投影片，所有文字為可編輯原生 PowerPoint 物件，字型替換為 Arial。

---

## 產出檔案

| 檔案 | 說明 |
|------|------|
| `Parking Prediction Deck.html` | 主要簡報（HTML，含動畫與連結） |
| `Parking_Prediction_Deck.pptx` | 匯出版本（PowerPoint 可編輯） |
| `deck-stage.js` | 簡報引擎元件 |
| `對話紀錄.md` | 本檔案 |

---

## 後續建議

1. **驗證文獻**：點擊連結確認每篇論文的方法描述正確
2. **補充引用格式**：將完整 APA/IEEE 引用格式加入參考資料頁
3. **NotebookLM**：將簡報內容匯入，生成 10 分鐘口頭解說腳本（Part B）
4. **繳交**：上傳 PPTX 或 PDF 至指定平台
