!python run_wadi.py 
Copying train file: /kaggle/input/datasets/giovannimonco/wadi-data/WADI_14days_new.csv → /kaggle/working/carla_bilstm/datasets/wadi/WADI_14days_new.csv
Copying test file:  /kaggle/input/datasets/giovannimonco/wadi-data/WADI_attackdataLABLE.csv → /kaggle/working/carla_bilstm/datasets/wadi/WADI_attackdataLABLE.csv
Set wadi_DATASET_PATH to /kaggle/working/carla_bilstm/datasets/wadi

==============================
STARTING EXPERIMENTS
==============================
GPU available: Tesla T4

Running dataset: wadi
Max GPU Memory after wadi: 1323.35 MB

==============================
DONE ALL WADI DATASETS
Total time: 1184.16 s
Avg / dataset: 1184.16 s
==============================

Time results saved to results/wadi/time_results.json

==============================
STARTING EVALUATION (PAPER STYLE)
==============================
wadi: PR-AUC=0.1792, TP=153, FP=701, FN=0

==============================
FINAL RESULTS (PAPER STYLE)
==============================
PRECISION: 0.1792
RECALL: 1.0000
F1: 0.3039
AUPR_MEAN: 0.1792
AUPR_STD: nan
TP: 153
TN: 0
FP: 701
FN: 0
TOTAL_DATASETS: 1

================ SUMMARY ================
Precision : 0.1792
Recall    : 1.0000
F1-score  : 0.3039
AUPR mean : 0.1792
AUPR std  : nan

Total time     : 1184.16 s
Avg / dataset  : 1184.16 s
GPU max memory : 1323.35 MB
=========================================

Summary written to results/wadi/ketqua.txt