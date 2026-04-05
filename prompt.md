!python run_smap.py
Found Kaggle dataset at: /kaggle/input/datasets/patrickfleith/nasa-anomaly-detection-dataset-smap-msl
Copying /kaggle/input/datasets/patrickfleith/nasa-anomaly-detection-dataset-smap-msl/labeled_anomalies.csv to /kaggle/working/carla_bilstm/datasets/smap/labeled_anomalies.csv...
Copying /kaggle/input/datasets/patrickfleith/nasa-anomaly-detection-dataset-smap-msl/data/data/train to /kaggle/working/carla_bilstm/datasets/smap/train...
Copying /kaggle/input/datasets/patrickfleith/nasa-anomaly-detection-dataset-smap-msl/data/data/test to /kaggle/working/carla_bilstm/datasets/smap/test...

==============================
STARTING EXPERIMENTS
==============================
GPU available: Tesla T4

Running dataset: P-1
Error running pretext for P-1: Command '['/usr/bin/python3', 'carla_pretext.py', '--config_env', 'configs/env.yml', '--config_exp', 'configs/pretext/carla_pretext_smap.yml', '--fname', 'P-1']' returned non-zero exit status 1.
Traceback (most recent call last):
  File "/kaggle/working/carla_bilstm/carla_pretext.py", line 240, in <module>
    main()
  File "/kaggle/working/carla_bilstm/carla_pretext.py", line 92, in main
    train_dataset = get_train_dataset(p, train_transforms, sanomaly, to_augmented_dataset=True,
                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/kaggle/working/carla_bilstm/utils/common_config.py", line 94, in get_train_dataset
    dataset = MSL(p['fname'], train=True, transform=transform, sanomaly=sanomaly,
              ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/kaggle/working/carla_bilstm/data/MSL.py", line 29, in __init__
    with open(os.path.join(self.root, 'labeled_anomalies.csv'), 'r') as file:
         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
FileNotFoundError: [Errno 2] No such file or directory: '/kaggle/working/carla_bilstm/datasets/msl/labeled_anomalies.csv'

Error running classification for P-1: Command '['/usr/bin/python3', 'carla_classification.py', '--config_env', 'configs/env.yml', '--config_exp', 'configs/classification/carla_classification_smap.yml', '--fname', 'P-1']' returned non-zero exit status 1.
Traceback (most recent call last):
  File "/kaggle/working/carla_bilstm/carla_classification.py", line 216, in <module>
    main()
  File "/kaggle/working/carla_bilstm/carla_classification.py", line 52, in main
    train_dataset = get_aug_train_dataset(p, train_transformations, to_neighbors_dataset = True)
                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/kaggle/working/carla_bilstm/utils/common_config.py", line 172, in get_aug_train_dataset
    dataloader = torch.load(p['contrastive_dataset'], weights_only=False)
                 ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/serialization.py", line 1484, in load
    with _open_file_like(f, "rb") as opened_file:
         ^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/serialization.py", line 759, in _open_file_like
    return _open_file(name_or_buffer, mode)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/serialization.py", line 740, in __init__
    super().__init__(open(name, mode))
                     ^^^^^^^^^^^^^^^^
FileNotFoundError: [Errno 2] No such file or directory: 'results/SMAP/P-1/pretext/con_train_dataset.pth'

Max GPU Memory after P-1: 0.00 MB

Running dataset: S-1
Error running pretext for S-1: Command '['/usr/bin/python3', 'carla_pretext.py', '--config_env', 'configs/env.yml', '--config_exp', 'configs/pretext/carla_pretext_smap.yml', '--fname', 'S-1']' returned non-zero exit status 1.
Traceback (most recent call last):
  File "/kaggle/working/carla_bilstm/carla_pretext.py", line 240, in <module>
    main()
  File "/kaggle/working/carla_bilstm/carla_pretext.py", line 92, in main
    train_dataset = get_train_dataset(p, train_transforms, sanomaly, to_augmented_dataset=True,
                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/kaggle/working/carla_bilstm/utils/common_config.py", line 94, in get_train_dataset
    dataset = MSL(p['fname'], train=True, transform=transform, sanomaly=sanomaly,
              ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/kaggle/working/carla_bilstm/data/MSL.py", line 29, in __init__
    with open(os.path.join(self.root, 'labeled_anomalies.csv'), 'r') as file:
         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
FileNotFoundError: [Errno 2] No such file or directory: '/kaggle/working/carla_bilstm/datasets/msl/labeled_anomalies.csv'

Error running classification for S-1: Command '['/usr/bin/python3', 'carla_classification.py', '--config_env', 'configs/env.yml', '--config_exp', 'configs/classification/carla_classification_smap.yml', '--fname', 'S-1']' returned non-zero exit status 1.
Traceback (most recent call last):
  File "/kaggle/working/carla_bilstm/carla_classification.py", line 216, in <module>
    main()
  File "/kaggle/working/carla_bilstm/carla_classification.py", line 52, in main
    train_dataset = get_aug_train_dataset(p, train_transformations, to_neighbors_dataset = True)
                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/kaggle/working/carla_bilstm/utils/common_config.py", line 172, in get_aug_train_dataset
    dataloader = torch.load(p['contrastive_dataset'], weights_only=False)
                 ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/serialization.py", line 1484, in load
    with _open_file_like(f, "rb") as opened_file:
         ^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/serialization.py", line 759, in _open_file_like
    return _open_file(name_or_buffer, mode)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/serialization.py", line 740, in __init__
    super().__init__(open(name, mode))
                     ^^^^^^^^^^^^^^^^
FileNotFoundError: [Errno 2] No such file or directory: 'results/SMAP/S-1/pretext/con_train_dataset.pth'

Max GPU Memory after S-1: 0.00 MB

Running dataset: E-1
Error running pretext for E-1: Command '['/usr/bin/python3', 'carla_pretext.py', '--config_env', 'configs/env.yml', '--config_exp', 'configs/pretext/carla_pretext_smap.yml', '--fname', 'E-1']' returned non-zero exit status 1.
Traceback (most recent call last):
  File "/kaggle/working/carla_bilstm/carla_pretext.py", line 240, in <module>
    main()
  File "/kaggle/working/carla_bilstm/carla_pretext.py", line 92, in main
    train_dataset = get_train_dataset(p, train_transforms, sanomaly, to_augmented_dataset=True,
                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/kaggle/working/carla_bilstm/utils/common_config.py", line 94, in get_train_dataset
    dataset = MSL(p['fname'], train=True, transform=transform, sanomaly=sanomaly,
              ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/kaggle/working/carla_bilstm/data/MSL.py", line 29, in __init__
    with open(os.path.join(self.root, 'labeled_anomalies.csv'), 'r') as file:
         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
FileNotFoundError: [Errno 2] No such file or directory: '/kaggle/working/carla_bilstm/datasets/msl/labeled_anomalies.csv'
