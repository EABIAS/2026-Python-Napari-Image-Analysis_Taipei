# 📘 Pre-class Setup（課前準備）

為確保課程進行順利，請學員於上課前完成以下設定。

---

## 🔧 A. 安裝 OME-Zarr Plugin（napari-ome-zarr）

若欲於課程中操作 OME-Zarr，請先於指定環境中安裝 plugin。

### 環境名稱
```bash
EABIAS_TP_2026
```

---

### 方法 1：透過 Conda 安裝（建議）

```bash
conda activate EABIAS_TP_2026
conda install -c conda-forge napari-ome-zarr
```

建議同時安裝相關相依套件：

```bash
conda install -c conda-forge ome-zarr zarr numcodecs
```

**優點：**
- 相依性自動處理  
- 穩定性較高  
- 較少 plugin 錯誤（如 blosc / numcodecs 問題）  

---

### 方法 2：透過 napari GUI 安裝（較不建議）

1. 開啟 napari：

```bash
napari
```

2. 進入：

```
Plugins → Install/Uninstall Plugins
```

3. 搜尋：

```
napari-ome-zarr
```

4. 點擊 **Install** 安裝  

5. ⚠️ 安裝後需重新啟動 napari  

**可能問題：**
- 版本衝突（Windows 常見）  
- MultipleReaderError  
- numcodecs / blosc import error  

---

## 🚀 B. 啟動環境與 Jupyter Notebook

### Step 1：啟動環境

```bash
conda activate EABIAS_TP_2026
```

---

### Step 2：啟動 Jupyter

```bash
jupyter notebook
```

或（推薦）：

```bash
jupyter lab
```

---

### Step 3：開啟講義 Notebook

1. 下載課程提供的 `.ipynb` 檔案  
2. 上傳至 Jupyter 介面  
3. 點擊開啟即可開始操作  

---

## 📌 注意事項

- 請確認 Kernel 為 `EABIAS_TP_2026`  
- ❗ 請勿在 `base` 環境操作（最常見錯誤）  
- 請避免混用 `pip` 與 `conda` 安裝套件  

若 napari 無法正常運作，請檢查：
- 是否已啟動正確環境  
- plugin 是否安裝成功  

---

## 🎯 課程目標

完成上述設定後，你將可以：

- 讀取 OME-Zarr 多維影像  
- 使用 napari 進行 3D / multiscale visualization  
- 搭配 Jupyter Notebook 進行影像分析  
