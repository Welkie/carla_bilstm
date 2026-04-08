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
Max GPU Memory after swat: 2387.74 MB

==============================
DONE ALL SWAT DATASETS
Total time: 1020.48 s
Avg / dataset: 1020.48 s
==============================

Time results saved to results/swat/time_results.json

==============================
STARTING EVALUATION (PAPER STYLE)
==============================
swat: PR-AUC=0.6383, TP=640, FP=0, FN=452

==============================
FINAL RESULTS (PAPER STYLE)
==============================
PRECISION: 1.0000
RECALL: 0.5861
F1: 0.7390
AUPR_MEAN: 0.6383
AUPR_STD: nan
TP: 640
TN: 7902
FP: 0
FN: 452
TOTAL_DATASETS: 1

================ SUMMARY ================
Precision : 1.0000
Recall    : 0.5861
F1-score  : 0.7390
AUPR mean : 0.6383
AUPR std  : nan

Total time     : 1020.48 s
Avg / dataset  : 1020.48 s
GPU max memory : 2387.74 MB
=========================================

Summary written to results/swat/ketqua.txt

Kết quả này là khi tui chạy swat: carla_bilstm 
còn khi chạy carla_resnet của tác giả carla thì kết quả là: & ResNet  & 0.7917 & 0.6126 & 0.6908 & 0.5193 & 1142.35 & 1142.35 & 206.96
còn khi chạy carla(pretext: mamba, classification = resnet): 0.9714 & 0.9029 & 0.9359 & 0.9144 & 1188.81 & 1188.81 & 467.78

còn các bộ dataset khác thì:
\multirow{3}{*}{MSL}
 & ResNet  & 0.3910 & 0.8025 & 0.5258 & 0.4866 $\pm$ 0.2519 & 12351.98 & 457.48 & 1230.80 \\
 & BiLSTM  & 0.5178 & 0.7723 & 0.6199 & 0.5924 $\pm$ 0.2533 & 5377.10 & 199.15 & 1242.98 \\
 & MAMBA   & 0.4196 & 0.8048 & 0.5516 & 0.5126 $\pm$ 0.2327 & 12056.33 & 446.53 & 1549.12 \\
\hline
\multirow{3}{*}{SMAP}
 & ResNet  & 0.4233 & 0.7589 & 0.5435 & 0.4396 $\pm$ 0.3217 & 33924.34 & 616.81 & 382.69 \\
 & BiLSTM  & 0.5008 & 0.8035 & 0.6170 & 0.5181 $\pm$ 0.3529 & 13108.58 & 238.34 & 652.37 \\
 & MAMBA   & 0.3189 & 0.8322 & 0.4611 & 0.3663 $\pm$ 0.3137 & 30623.82 & 556.80 & 469.62 \\
\hline
\multirow{3}{*}{SMD}
 & ResNet  & 0.3144 & 0.5987 & 0.4123 & 0.3870 $\pm$ 0.1908 & 33763.76 & 1205.85 & 1540.48 \\
 & BiLSTM  & 0.3674 & 0.5939 & 0.4540 & 0.3934 $\pm$ 0.1759 & 14728.85 & 526.03 & 1703.86 \\
 & MAMBA   & 0.3884 & 0.8340 & 0.5300 & 0.4401 $\pm$ 0.1808 & 33093.38 & 1181.91 & 3840.36 \\
\hline
\multirow{3}{*}{SWaT}
 & ResNet  & 0.7917 & 0.6126 & 0.6908 & 0.5193 & 1142.35 & 1142.35 & 206.96 \\
 & BiLSTM  & -- & -- & -- & -- & -- & -- & -- \\
 & MAMBA   & 0.9714 & 0.9029 & 0.9359 & 0.9144 & 1188.81 & 1188.81 & 467.78 \\
\hline
\multirow{3}{*}{WADI}
 & ResNet  & 0.2202 & 0.8824 & 0.3525 & 0.1771 & 1496.77 & 1496.77 & 179.48 \\
 & BiLSTM  & -- & -- & -- & -- & -- & -- & -- \\
 & MAMBA   & 0.2298 & 0.7314 & 0.3497 & 0.1959 & 1433.61 & 1433.61 & 297.37 \\
\hline
\multirow{3}{*}{Yahoo-A1}
 & ResNet  & 0.6946 & 0.9746 & 0.8111 & 0.7761 $\pm$ 0.3397 & 5609.75 & 102.00 & 42.39 \\
 & BiLSTM  & 0.8634 & 0.9782 & 0.9172 & 0.9114 $\pm$ 0.1460 & 2558.50 & 46.52 & 587.72 \\
 & MAMBA   & 0.5864 & 0.9867 & 0.7356 & 0.6355 $\pm$ 0.3941 & 5845.12 & 106.27 & 92.93 \\
\hline
\multirow{3}{*}{KPI}
 & ResNet  & 0.1500 & 0.7206 & 0.2483 & 0.2644 $\pm$ 0.2343 & 62356.69 & 2150.23 & 371.06 \\
 & BiLSTM  & 0.2202 & 0.5213 & 0.3096 & 0.3567 $\pm$ 0.2483 & 27882.98 & 961.48 & 531.86 \\
 & MAMBA   & 0.2453 & 0.8415 & 0.3798 & 0.3235 $\pm$ 0.2276 & 66186.61 & 2282.30 & 316.46 \\
\hline

bilstm đang vượt trội mà sao swat lại yếu như vậy. Có gì bất ổn ở đâu ko, config? Cải thiện đc thì cải thiện cho tui