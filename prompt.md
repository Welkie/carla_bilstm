!python run_smd.py --phase 1 
Found Kaggle dataset at: /kaggle/input/datasets/mgusat/smd-onmiad/ServerMachineDataset
Copying /kaggle/input/datasets/mgusat/smd-onmiad/ServerMachineDataset/train to /kaggle/working/carla_bilstm/datasets/smd/train...
Copying /kaggle/input/datasets/mgusat/smd-onmiad/ServerMachineDataset/test to /kaggle/working/carla_bilstm/datasets/smd/test...
Copying /kaggle/input/datasets/mgusat/smd-onmiad/ServerMachineDataset/test_label to /kaggle/working/carla_bilstm/datasets/smd/test_label...
Found total 28 datasets in smd.
PHASE 1: Running first 14 datasets.

==============================
STARTING EXPERIMENTS SMD - PHASE 1
==============================
GPU available: Tesla T4

Running dataset: machine-1-1.txt
Max GPU Memory after machine-1-1.txt: 1690.26 MB

Running dataset: machine-1-2.txt
Max GPU Memory after machine-1-2.txt: 1690.26 MB

Running dataset: machine-1-3.txt
Max GPU Memory after machine-1-3.txt: 1690.26 MB

Running dataset: machine-1-4.txt
Error running classification for machine-1-4.txt: Command '['/usr/bin/python3', 'carla_classification.py', '--config_env', 'configs/env.yml', '--config_exp', 'configs/classification/carla_classification_smd.yml', '--fname', 'machine-1-4.txt']' returned non-zero exit status 1.
Traceback (most recent call last):
  File "/kaggle/working/carla_bilstm/carla_classification.py", line 216, in <module>
    main()
  File "/kaggle/working/carla_bilstm/carla_classification.py", line 192, in main
    predictions = get_predictions(p, val_dataloader, model, False, False)
                  ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/utils/_contextlib.py", line 124, in decorate_context
    return func(*args, **kwargs)
           ^^^^^^^^^^^^^^^^^^^^^
  File "/kaggle/working/carla_bilstm/utils/evaluate_utils.py", line 74, in get_predictions
    res = model(ts.view(bs, h, w), forward_pass='return_all')
          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/nn/modules/module.py", line 1776, in _wrapped_call_impl
    return self._call_impl(*args, **kwargs)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/nn/modules/module.py", line 1787, in _call_impl
    return forward_call(*args, **kwargs)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/nn/parallel/data_parallel.py", line 197, in forward
    outputs = self.parallel_apply(replicas, inputs, module_kwargs)
              ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/nn/parallel/data_parallel.py", line 214, in parallel_apply
    return parallel_apply(
           ^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/nn/parallel/parallel_apply.py", line 133, in parallel_apply
    output.reraise()
  File "/usr/local/lib/python3.12/dist-packages/torch/_utils.py", line 775, in reraise
    raise exception
TypeError: Caught TypeError in replica 1 on device 1.
Original Traceback (most recent call last):
  File "/usr/local/lib/python3.12/dist-packages/torch/nn/parallel/parallel_apply.py", line 103, in _worker
    output = module(*input, **kwargs)
             ^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/nn/modules/module.py", line 1776, in _wrapped_call_impl
    return self._call_impl(*args, **kwargs)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/nn/modules/module.py", line 1787, in _call_impl
    return forward_call(*args, **kwargs)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
TypeError: ClusteringModel.forward() missing 1 required positional argument: 'x'


Max GPU Memory after machine-1-4.txt: 1690.26 MB

Running dataset: machine-1-5.txt
Error running classification for machine-1-5.txt: Command '['/usr/bin/python3', 'carla_classification.py', '--config_env', 'configs/env.yml', '--config_exp', 'configs/classification/carla_classification_smd.yml', '--fname', 'machine-1-5.txt']' returned non-zero exit status 1.
Traceback (most recent call last):
  File "/kaggle/working/carla_bilstm/carla_classification.py", line 216, in <module>
    main()
  File "/kaggle/working/carla_bilstm/carla_classification.py", line 192, in main
    predictions = get_predictions(p, val_dataloader, model, False, False)
                  ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/utils/_contextlib.py", line 124, in decorate_context
    return func(*args, **kwargs)
           ^^^^^^^^^^^^^^^^^^^^^
  File "/kaggle/working/carla_bilstm/utils/evaluate_utils.py", line 74, in get_predictions
    res = model(ts.view(bs, h, w), forward_pass='return_all')
          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/nn/modules/module.py", line 1776, in _wrapped_call_impl
    return self._call_impl(*args, **kwargs)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/nn/modules/module.py", line 1787, in _call_impl
    return forward_call(*args, **kwargs)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/nn/parallel/data_parallel.py", line 197, in forward
    outputs = self.parallel_apply(replicas, inputs, module_kwargs)
              ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/nn/parallel/data_parallel.py", line 214, in parallel_apply
    return parallel_apply(
           ^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/nn/parallel/parallel_apply.py", line 133, in parallel_apply
    output.reraise()
  File "/usr/local/lib/python3.12/dist-packages/torch/_utils.py", line 775, in reraise
    raise exception
TypeError: Caught TypeError in replica 1 on device 1.
Original Traceback (most recent call last):
  File "/usr/local/lib/python3.12/dist-packages/torch/nn/parallel/parallel_apply.py", line 103, in _worker
    output = module(*input, **kwargs)
             ^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/nn/modules/module.py", line 1776, in _wrapped_call_impl
    return self._call_impl(*args, **kwargs)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/nn/modules/module.py", line 1787, in _call_impl
    return forward_call(*args, **kwargs)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
TypeError: ClusteringModel.forward() missing 1 required positional argument: 'x'


Max GPU Memory after machine-1-5.txt: 1690.26 MB

Running dataset: machine-1-6.txt
Max GPU Memory after machine-1-6.txt: 1690.26 MB

Running dataset: machine-1-7.txt
Max GPU Memory after machine-1-7.txt: 1690.26 MB

Running dataset: machine-1-8.txt
Max GPU Memory after machine-1-8.txt: 1690.26 MB

Running dataset: machine-2-1.txt
Max GPU Memory after machine-2-1.txt: 1690.26 MB

Running dataset: machine-2-2.txt
Max GPU Memory after machine-2-2.txt: 1690.26 MB

Running dataset: machine-2-3.txt
Max GPU Memory after machine-2-3.txt: 1690.26 MB

Running dataset: machine-2-4.txt
Max GPU Memory after machine-2-4.txt: 1690.26 MB

Running dataset: machine-2-5.txt
Max GPU Memory after machine-2-5.txt: 1690.26 MB

Running dataset: machine-2-6.txt
Max GPU Memory after machine-2-6.txt: 1703.86 MB

==============================
DONE PHASE 1 (14 datasets)
Total time (this phase): 6852.58 s
Avg / dataset: 489.47 s
==============================

Evaluating Phase 1 results...

==============================
STARTING EVALUATION SMD
==============================
/kaggle/working/carla_bilstm/run_smd.py:207: FutureWarning: The behavior of DataFrame concatenation with empty or all-NA entries is deprecated. In a future version, this will no longer exclude empty or all-NA columns when determining the result dtypes. To retain the old behavior, exclude the relevant entries before the concat operation.
  res_df = pd.concat([res_df, new_row], ignore_index=True)
machine-1-1.txt: PR-AUC=0.1183, TP=795, FP=3862, FN=62
machine-1-2.txt: PR-AUC=0.5147, TP=276, FP=316, FN=215
machine-1-3.txt: PR-AUC=0.3550, TP=224, FP=338, FN=415
Skip machine-1-4.txt (missing files)
Skip machine-1-5.txt (missing files)
machine-1-6.txt: PR-AUC=0.7162, TP=1616, FP=1778, FN=270
machine-1-7.txt: PR-AUC=0.2706, TP=833, FP=2084, FN=126
machine-1-8.txt: PR-AUC=0.3724, TP=329, FP=379, FN=584
machine-2-1.txt: PR-AUC=0.2835, TP=340, FP=511, FN=412
machine-2-2.txt: PR-AUC=0.4432, TP=689, FP=1007, FN=301
machine-2-3.txt: PR-AUC=0.2517, TP=78, FP=20, FN=361
machine-2-4.txt: PR-AUC=0.4799, TP=881, FP=707, FN=229
machine-2-5.txt: PR-AUC=0.3292, TP=681, FP=1813, FN=300
machine-2-6.txt: PR-AUC=0.3970, TP=125, FP=56, FN=240
Saved metrics to results/smd/phase_1_metrics_df.csv

==============================
FINAL RESULTS SMD
==============================
PRECISION: 0.3479
RECALL: 0.6614
F1: 0.4560
AUPR_MEAN: 0.3776
AUPR_STD: 0.1522
TP: 6867
TN: 35091
FP: 12871
FN: 3515
TOTAL_DATASETS: 12
Phase 1 completed. Please push 'results/smd/phase_1_metrics_df.csv' and 'results/smd/phase_1_time_stats.json' to continue in Phase 2.

đây là lỗi khi tui chạy file smd phase 1 trước khi update code, bạn check xem lỗi này được fix chưa, nếu chưa thì fix cho tui.