# 生物影像分析的開源AI工具課程 (準備中)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Course Status](https://img.shields.io/badge/status-coming_soon-blue.svg)]()

<!-- [![Course Status](https://img.shields.io/badge/status-active-success.svg)]() -->

##  課程簡介

本課程聚焦於解決生物學家在影像分析中常見的影像分割問題。我們精選了三款強大的開源軟體，涵蓋了傳統機器學習與最新的深度學習技術：

1.  **ilastik**: 適合初學者的互動式機器學習平台。
2.  **Cellpose (Cellpose-SAM)**: 結合 SAM 技術的通用細胞分割工具。
3.  **micro-sam**: 針對顯微影像優化的 Segment Anything Model 工具。

## 課前準備:
1. 請先下載[Installation_steps.pdf](Installation_steps.pdf)並依循步驟安裝課程需要的軟體。
2. 請下載 [Test_Img_Cellpose.zip](Test_Img_Cellpose.zip), [Test_Img_BBBC039_Subset.zip](Test_Img_BBBC039_Subset.zip), [Test_Img_Human_Mitosis.zip](Test_Img_Human_Mitosis.zip) 這三份測試用影像。
3. 課程投影片PDF版: [Practical_AI_Tools_for_Bioimage_Segmentation_V2.pdf](Practical_AI_Tools_for_Bioimage_Segmentation_V2.pdf)。
4. 細節課堂會解說, 但是鼓勵大家先自己玩看看, 特別是第一次在本地端執行Cellpose的時候會被背景會下載 cpsam model (約1.15 G), 會花不少時間下載。

## 完整課程投影片PowerPoint檔案下載連結 [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.19911180.svg)](https://doi.org/10.5281/zenodo.19911180)

---

## 工具列表

### 1. [ilastik](https://www.ilastik.org/)
> **"No code, just biology."** — 透過互動式標註訓練隨機森林 (Random Forest) 分類器。

*   **核心功能**：
    *   **像素分類 (Pixel Classification)**：基於顏色、紋理等特徵進行語意分割 (semantic segmentation)。
    *   **物件分類 (Object Classification)**：從分割遮罩中提取特徵並對個體進行分類。
*   **特色**：完全圖形化介面 (GUI)，無需程式設計背景即可上手。

### 2. [Cellpose](https://www.cellpose.org/) (Latest: Cellpose-SAM)
> **"A generalist algorithm for cellular segmentation."** — 最新版本引入 SAM 技術以強化分割能力。

*   **核心功能**：
    *   **實例分割 (Instance Segmentation)**：精確區分並標記個別細胞，解決細胞沾黏問題。
    *   **Cellpose-SAM**：結合 Segment Anything Model 的強大特徵提取能力，提供更通用的分割效果。
    *   **人機協作訓練微調 (Human-in-the-loop training)**：支援使用少量標註資料 (500-1000 ROIs) 快速微調 (Fine-tuning) 模型。
    *   **3D 支援**：原生支援三維堆疊影像 (Z-stacks) 處理。
*   **特色**：泛化能力極強，大多情況無需調整參數，適用於多種細胞型態與顯微鏡類型。

### 3. [micro-sam](https://github.com/computational-cell-analytics/micro-sam)
> **"Segment Anything for Microscopy."** — 將 Meta 的 SAM 模型針對顯微影像進行微調與優化。

*   **核心功能**：
    *   **互動式分割**：透過點擊 (Prompts) 或框選 (Bounding box) 實現即時分割。
    *   **自動分割 (Automatic Segmentation)**：支援批次處理大量影像。
    *   **專用模型**：提供針對光學顯微鏡 (LM) 與電子顯微鏡 (EM) 優化的通用模型。
    *   **napari 整合**：作為 napari plugin 運行，介面友善且擴充性高。
    *   **追蹤功能**：支援 2D 時序資料的物件追蹤。
*   **特色**：結合視覺基礎模型 (Vision Foundation Model) 的強大零樣本 (Zero-shot) 遷移能力。

---

## 工具比較表

| 特性 | ilastik | Cellpose (Cellpose-SAM) | micro-sam |
| :--- | :---: | :---: | :---: |
| **核心技術** | 機械學習 | 深度學習 | 深度學習 |
| **學習曲線** | 🟢 低 (GUI) | 🟢 低 (Standalone GUI) | 🟢 低 (napari GUI) |
| **互動式標註** | ✅ 強大 | ✅ 支援 | ✅ 強大 (Prompting) |
| **3D 支援** | ✅ | ✅ | ✅ |
| **追蹤功能** | ✅ | ❌ (需搭配其他工具) | ✅ |
| **最佳適用場景** | 紋理明顯、背景複雜的影像 | 細胞密集、型態多樣的細胞/核 | 未知樣本、需要快速標註輔助 |

---

<p align="center">
  <sub>Created for the Bioimage Analysis Course. Maintainer: [Your Name/Organization]</sub>
</p>
