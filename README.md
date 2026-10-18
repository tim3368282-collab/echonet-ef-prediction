# echonet-ef-prediction
Cardiac Ejection Fraction Prediction from Echocardiography Videos using R(2+1)D-18
Cardiac Ejection Fraction Prediction Using Deep Learning

以深度學習進行心臟超音波影片之射出分率（EF）預測

1. Project Overview

本專案旨在學習如何運用深度學習模型，從心臟超音波影片預測左心室射出分率（Ejection Fraction, EF）。

使用公開的 EchoNet-Dynamic 資料集，並以 R(2+1)D-18 影片模型進行訓練，探索深度學習在醫學影像分析與心臟功能評估上的應用。

本專案於 Kaggle Notebook 環境中執行，使用 GPU 加速模型訓練。

2. Project Objectives
學習影片深度學習模型的訓練流程。
理解 R(2+1)D-18 模型在時空特徵擷取上的應用。
建立由心臟超音波影片預測 EF 數值的流程。
透過模型訓練與測試結果，分析預測誤差及模型限制。
3. Dataset

EchoNet-Dynamic

Dataset: EchoNet-Dynamic
Original repository: echonet/dynamic
Task: Ejection Fraction (EF) prediction
Input: Echocardiography video clips
Output: Predicted EF value

本專案使用 Kaggle 上提供的 EchoNet-Dynamic 資料集。資料集與原始程式碼的使用，依其各自的授權及使用條款辦理。

4. Model and Training Configuration
Parameter	Configuration
Model architecture	R(2+1)D-18
Task	EF regression
Pretrained weights	Enabled
Training epochs	10
Learning rate	0.0001
Weight decay	0.0001
Frames	32
Frame sampling period	2
Batch size	20
Random seed	0
Training environment	Kaggle GPU
5. Training Process

模型使用公開的 EchoNet-Dynamic 專案程式碼進行訓練，並依照本專案設定調整訓練參數。

目前已完成 10 個 Epoch 的訓練，並產生 best.pt 模型權重檔案。

完整的測試流程及模型預測表現，仍需依實際執行結果進行整理。

6. Experimental Results

訓練完成後，將整理以下評估結果：

Mean Absolute Error (MAE)
Root Mean Squared Error (RMSE)
Actual vs. Predicted EF scatter plot
Training and validation performance

目前尚未在此列出最終評估數值，以避免將訓練過程中的數值誤認為測試集結果。

7. Repository Structure
echonet-ef-prediction/
├── README.md
├── notebooks/
│   └── echonet_training.ipynb
├── results/
│   ├── metrics.csv
│   └── actual_vs_predicted.png
└── CITATION.md


以上為預計整理的專案結構。尚未建立或產生的檔案，會在後續完成實驗分析後加入。

8. Reproducibility

訓練環境為 Kaggle Notebook，使用 GPU 執行模型訓練。

主要訓練參數包含：

Model: r2plus1d_18
Task: EF
Epochs: 10
Learning rate: 1e-4
Batch size: 20

實際執行環境、套件版本、資料集來源及程式碼版本，將隨專案整理補充。

9. Attribution

本專案參考並使用 EchoNet-Dynamic 開源專案所提供的程式碼與研究成果。

Original repository: https://github.com/echonet/dynamic

原始作者、論文、軟體授權及資料集來源均應依照各自的規定標註。本專案的訓練與分析成果，將與原始專案的既有成果明確區分。

10. Limitations

本專案為深度學習與醫學影像分析的學習實作，僅針對公開資料集進行實驗。

目前的訓練結果不代表模型已具備臨床診斷能力，也不能直接取代專業醫療人員的判讀。

11. Future Work
完成測試集評估並整理 MAE 與 RMSE。
視需要比較不同訓練參數對預測結果的影響。
加入預測結果視覺化與誤差分析。
改善程式碼組織、環境設定與實驗重現性。
