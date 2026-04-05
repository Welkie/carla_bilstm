!pip install -r requirements.txt
Collecting arch==5.3.1 (from -r requirements.txt (line 1))
  Downloading arch-5.3.1.tar.gz (3.1 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 3.1/3.1 MB 32.5 MB/s eta 0:00:00
  Installing build dependencies ... done
  error: subprocess-exited-with-error
  
  × Getting requirements to build wheel did not run successfully.
  │ exit code: 1
  ╰─> See above for output.
  
  note: This error originates from a subprocess, and is likely not a problem with pip.
  Getting requirements to build wheel ... error
error: subprocess-exited-with-error

× Getting requirements to build wheel did not run successfully.
│ exit code: 1
╰─> See above for output.

note: This error originates from a subprocess, and is likely not a problem with pip.
!git clean -fd     # xóa output rác
!git pull
Already up to date.
!python run_msl.py
Found Kaggle dataset at: /kaggle/input/datasets/patrickfleith/nasa-anomaly-detection-dataset-smap-msl
Copying /kaggle/input/datasets/patrickfleith/nasa-anomaly-detection-dataset-smap-msl/labeled_anomalies.csv to /kaggle/working/carla_bilstm/datasets/msl/labeled_anomalies.csv...
Copying /kaggle/input/datasets/patrickfleith/nasa-anomaly-detection-dataset-smap-msl/data/data/train to /kaggle/working/carla_bilstm/datasets/msl/train...
Copying /kaggle/input/datasets/patrickfleith/nasa-anomaly-detection-dataset-smap-msl/data/data/test to /kaggle/working/carla_bilstm/datasets/msl/test...

==============================
STARTING EXPERIMENTS
==============================
GPU available: Tesla T4

Running dataset: M-6
Error running pretext for M-6: Command '['/usr/bin/python3', 'carla_pretext.py', '--config_env', 'configs/env.yml', '--config_exp', 'configs/pretext/carla_pretext_msl.yml', '--fname', 'M-6']' returned non-zero exit status 1.
Traceback (most recent call last):
  File "/kaggle/working/carla_bilstm/carla_pretext.py", line 15, in <module>
    from utils.repository import TSRepository
  File "/kaggle/working/carla_bilstm/utils/repository.py", line 4, in <module>
    import faiss
ModuleNotFoundError: No module named 'faiss'

Error running classification for M-6: Command '['/usr/bin/python3', 'carla_classification.py', '--config_env', 'configs/env.yml', '--config_exp', 'configs/classification/carla_classification_msl.yml', '--fname', 'M-6']' returned non-zero exit status 1.
Traceback (most recent call last):
  File "/kaggle/working/carla_bilstm/carla_classification.py", line 216, in <module>
    main()
  File "/kaggle/working/carla_bilstm/carla_classification.py", line 52, in main
    train_dataset = get_aug_train_dataset(p, train_transformations, to_neighbors_dataset = True)
                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/kaggle/working/carla_bilstm/utils/common_config.py", line 172, in get_aug_train_dataset
    dataloader = torch.load(p['contrastive_dataset'], weights_only=False)
                 ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/serialization.py", line 1500, in load
    with _open_file_like(f, "rb") as opened_file:
         ^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/serialization.py", line 768, in _open_file_like
    return _open_file(name_or_buffer, mode)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/serialization.py", line 749, in __init__
    super().__init__(open(name, mode))  # noqa: SIM115
                     ^^^^^^^^^^^^^^^^
FileNotFoundError: [Errno 2] No such file or directory: 'results/MSL/M-6/pretext/con_train_dataset.pth'

Max GPU Memory after M-6: 0.00 MB

Running dataset: M-1
Error running pretext for M-1: Command '['/usr/bin/python3', 'carla_pretext.py', '--config_env', 'configs/env.yml', '--config_exp', 'configs/pretext/carla_pretext_msl.yml', '--fname', 'M-1']' returned non-zero exit status 1.
Traceback (most recent call last):
  File "/kaggle/working/carla_bilstm/carla_pretext.py", line 15, in <module>
    from utils.repository import TSRepository
  File "/kaggle/working/carla_bilstm/utils/repository.py", line 4, in <module>
    import faiss
ModuleNotFoundError: No module named 'faiss'

Error running classification for M-1: Command '['/usr/bin/python3', 'carla_classification.py', '--config_env', 'configs/env.yml', '--config_exp', 'configs/classification/carla_classification_msl.yml', '--fname', 'M-1']' returned non-zero exit status 1.
Traceback (most recent call last):
  File "/kaggle/working/carla_bilstm/carla_classification.py", line 216, in <module>
    main()
  File "/kaggle/working/carla_bilstm/carla_classification.py", line 52, in main
    train_dataset = get_aug_train_dataset(p, train_transformations, to_neighbors_dataset = True)
                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/kaggle/working/carla_bilstm/utils/common_config.py", line 172, in get_aug_train_dataset
    dataloader = torch.load(p['contrastive_dataset'], weights_only=False)
                 ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/serialization.py", line 1500, in load
    with _open_file_like(f, "rb") as opened_file:
         ^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/serialization.py", line 768, in _open_file_like
    return _open_file(name_or_buffer, mode)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/serialization.py", line 749, in __init__
    super().__init__(open(name, mode))  # noqa: SIM115
                     ^^^^^^^^^^^^^^^^
FileNotFoundError: [Errno 2] No such file or directory: 'results/MSL/M-1/pretext/con_train_dataset.pth'

Max GPU Memory after M-1: 0.00 MB