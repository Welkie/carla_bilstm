!python run_swat.py
Found Kaggle dataset at: /kaggle/input/datasets/vishala28/swat-dataset-secure-water-treatment-system
Found merged dataset: /kaggle/input/datasets/vishala28/swat-dataset-secure-water-treatment-system/merged.csv
Processing merged dataset from /kaggle/input/datasets/vishala28/swat-dataset-secure-water-treatment-system/merged.csv...
Split merged.csv into:
Train (normal.csv): 496800 rows
Test (attack.csv): 449919 rows
Set swat_DATASET_PATH to /kaggle/working/carla_bilstm/datasets/swat
Set swat_DATASET_PATH to /kaggle/working/carla_bilstm/datasets/swat

==============================
STARTING EXPERIMENTS
==============================
GPU available: Tesla T4

Running dataset: swat
Max GPU Memory after swat: 2387.73 MB

==============================
DONE ALL SWAT DATASETS
Total time: 791.11 s
Avg / dataset: 791.11 s
==============================

Time results saved to results/swat/time_results.json

==============================
STARTING EVALUATION (PAPER STYLE)
==============================
swat: PR-AUC=0.1254, TP=1092, FP=7902, FN=0

==============================
FINAL RESULTS (PAPER STYLE)
==============================
PRECISION: 0.1214
RECALL: 1.0000
F1: 0.2165
AUPR_MEAN: 0.1254
AUPR_STD: nan
TP: 1092
TN: 0
FP: 7902
FN: 0
TOTAL_DATASETS: 1

================ SUMMARY ================
Precision : 0.1214
Recall    : 1.0000
F1-score  : 0.2165
AUPR mean : 0.1254
AUPR std  : nan

Total time     : 791.11 s
Avg / dataset  : 791.11 s
GPU max memory : 2387.73 MB
=========================================

Summary written to results/swat/ketqua.txt
sao lại overfit, fix cho tui