!python run_wadi.py 
Copying train file: /kaggle/input/datasets/giovannimonco/wadi-data/WADI_14days_new.csv → /kaggle/working/carla_bilstm/datasets/wadi/WADI_14days_new.csv
Copying test file:  /kaggle/input/datasets/giovannimonco/wadi-data/WADI_attackdataLABLE.csv → /kaggle/working/carla_bilstm/datasets/wadi/WADI_attackdataLABLE.csv
Set wadi_DATASET_PATH to /kaggle/working/carla_bilstm/datasets/wadi

==============================
STARTING EXPERIMENTS
==============================
GPU available: Tesla T4

Running dataset: wadi
Error running classification for wadi: Command '['/usr/bin/python3', 'carla_classification.py', '--config_env', 'configs/env.yml', '--config_exp', 'configs/classification/carla_classification_wadi.yml', '--fname', 'wadi']' returned non-zero exit status 1.
Traceback (most recent call last):
  File "/kaggle/working/carla_bilstm/carla_classification.py", line 216, in <module>
    main()
  File "/kaggle/working/carla_bilstm/carla_classification.py", line 184, in main
    predictions = get_predictions(p, tst_dl, model, False, False)
                  ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/utils/_contextlib.py", line 124, in decorate_context
    return func(*args, **kwargs)
           ^^^^^^^^^^^^^^^^^^^^^
  File "/kaggle/working/carla_bilstm/utils/evaluate_utils.py", line 80, in get_predictions
    res = _forward_with_pass(model, ts.view(bs, h, w), 'return_all')
          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/kaggle/working/carla_bilstm/utils/evaluate_utils.py", line 39, in _forward_with_pass
    return m(x, forward_pass=forward_pass)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/nn/modules/module.py", line 1776, in _wrapped_call_impl
    return self._call_impl(*args, **kwargs)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/nn/modules/module.py", line 1787, in _call_impl
    return forward_call(*args, **kwargs)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/kaggle/working/carla_bilstm/models/models.py", line 54, in forward
    features = self.backbone(x)
               ^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/nn/modules/module.py", line 1776, in _wrapped_call_impl
    return self._call_impl(*args, **kwargs)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/nn/modules/module.py", line 1787, in _call_impl
    return forward_call(*args, **kwargs)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/kaggle/working/carla_bilstm/models/resent_time.py", line 146, in forward
    out, _ = self.lstm(x)
             ^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/nn/modules/module.py", line 1776, in _wrapped_call_impl
    return self._call_impl(*args, **kwargs)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/nn/modules/module.py", line 1787, in _call_impl
    return forward_call(*args, **kwargs)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/nn/modules/rnn.py", line 1141, in forward
    result = _VF.lstm(
             ^^^^^^^^^
RuntimeError: Input and parameter tensors are not at the same device, found input tensor at cpu and parameter tensor at cuda:0

Max GPU Memory after wadi: 1323.35 MB

==============================
DONE ALL WADI DATASETS
Total time: 986.20 s
Avg / dataset: 986.20 s
==============================

Time results saved to results/wadi/time_results.json

==============================
STARTING EVALUATION (PAPER STYLE)
==============================
Skip wadi (missing files)
No results!


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
Error running classification for swat: Command '['/usr/bin/python3', 'carla_classification.py', '--config_env', 'configs/env.yml', '--config_exp', 'configs/classification/carla_classification_swat.yml', '--fname', 'swat']' returned non-zero exit status 1.
Traceback (most recent call last):
  File "/kaggle/working/carla_bilstm/carla_classification.py", line 216, in <module>
    main()
  File "/kaggle/working/carla_bilstm/carla_classification.py", line 184, in main
    predictions = get_predictions(p, tst_dl, model, False, False)
                  ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/utils/_contextlib.py", line 120, in decorate_context
    return func(*args, **kwargs)
           ^^^^^^^^^^^^^^^^^^^^^
  File "/kaggle/working/carla_bilstm/utils/evaluate_utils.py", line 80, in get_predictions
    res = _forward_with_pass(model, ts.view(bs, h, w), 'return_all')
          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/kaggle/working/carla_bilstm/utils/evaluate_utils.py", line 39, in _forward_with_pass
    return m(x, forward_pass=forward_pass)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/nn/modules/module.py", line 1773, in _wrapped_call_impl
    return self._call_impl(*args, **kwargs)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/nn/modules/module.py", line 1784, in _call_impl
    return forward_call(*args, **kwargs)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/kaggle/working/carla_bilstm/models/models.py", line 54, in forward
    features = self.backbone(x)
               ^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/nn/modules/module.py", line 1773, in _wrapped_call_impl
    return self._call_impl(*args, **kwargs)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/nn/modules/module.py", line 1784, in _call_impl
    return forward_call(*args, **kwargs)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/kaggle/working/carla_bilstm/models/resent_time.py", line 146, in forward
    out, _ = self.lstm(x)
             ^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/nn/modules/module.py", line 1773, in _wrapped_call_impl
    return self._call_impl(*args, **kwargs)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/nn/modules/module.py", line 1784, in _call_impl
    return forward_call(*args, **kwargs)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/nn/modules/rnn.py", line 1124, in forward
    result = _VF.lstm(
             ^^^^^^^^^
RuntimeError: Input and parameter tensors are not at the same device, found input tensor at cpu and parameter tensor at cuda:0

Max GPU Memory after swat: 2387.73 MB

==============================
DONE ALL SWAT DATASETS
Total time: 347.90 s
Avg / dataset: 347.90 s
==============================

Time results saved to results/swat/time_results.json

==============================
STARTING EVALUATION (PAPER STYLE)
==============================
Skip swat (missing files)
No results!