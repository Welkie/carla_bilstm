!python run_wadi.py 
Copying train file: /kaggle/input/datasets/giovannimonco/wadi-data/WADI_14days_new.csv → /kaggle/working/carla_bilstm/datasets/wadi/WADI_14days_new.csv
Copying test file:  /kaggle/input/datasets/giovannimonco/wadi-data/WADI_attackdataLABLE.csv → /kaggle/working/carla_bilstm/datasets/wadi/WADI_attackdataLABLE.csv
Set wadi_DATASET_PATH to /kaggle/working/carla_bilstm/datasets/wadi

==============================
STARTING EXPERIMENTS
==============================
GPU available: Tesla T4

Running dataset: wadi
Error running pretext for wadi: Command '['/usr/bin/python3', 'carla_pretext.py', '--config_env', 'configs/env.yml', '--config_exp', 'configs/pretext/carla_pretext_wadi.yml', '--fname', 'wadi']' returned non-zero exit status 1.
Traceback (most recent call last):
  File "/kaggle/working/carla_bilstm/carla_pretext.py", line 240, in <module>
    main()
  File "/kaggle/working/carla_bilstm/carla_pretext.py", line 143, in main
    train_dataset = get_train_dataset(p, train_transforms, sanomaly, to_augmented_dataset=True)
                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/kaggle/working/carla_bilstm/utils/common_config.py", line 146, in get_train_dataset
    dataset = WADI(p['fname'], train=True, transform=transform, sanomaly=sanomaly,
              ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/kaggle/working/carla_bilstm/data/WADI.py", line 44, in __init__
    fr = pd.read_csv(file_path)
         ^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/pandas/io/parsers/readers.py", line 1026, in read_csv
    return _read(filepath_or_buffer, kwds)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/pandas/io/parsers/readers.py", line 620, in _read
    parser = TextFileReader(filepath_or_buffer, **kwds)
             ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/pandas/io/parsers/readers.py", line 1620, in __init__
    self._engine = self._make_engine(f, self.engine)
                   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/pandas/io/parsers/readers.py", line 1880, in _make_engine
    self.handles = get_handle(
                   ^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/pandas/io/common.py", line 873, in get_handle
    handle = open(
             ^^^^^
FileNotFoundError: [Errno 2] No such file or directory: '/kaggle/working/carla_bilstm/datasets/wadi/wadi_14days_new.csv'

Error running classification for wadi: Command '['/usr/bin/python3', 'carla_classification.py', '--config_env', 'configs/env.yml', '--config_exp', 'configs/classification/carla_classification_wadi.yml', '--fname', 'wadi']' returned non-zero exit status 1.
Traceback (most recent call last):
  File "/kaggle/working/carla_bilstm/carla_classification.py", line 216, in <module>
    main()
  File "/kaggle/working/carla_bilstm/carla_classification.py", line 52, in main
    train_dataset = get_aug_train_dataset(p, train_transformations, to_neighbors_dataset = True)
                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/kaggle/working/carla_bilstm/utils/common_config.py", line 176, in get_aug_train_dataset
    data_dict = torch.load(p['contrastive_dataset'], weights_only=False)
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
FileNotFoundError: [Errno 2] No such file or directory: 'results/wadi/wadi/pretext/con_train_dataset.pth'

Max GPU Memory after wadi: 0.00 MB

==============================
DONE ALL WADI DATASETS
Total time: 19.91 s
Avg / dataset: 19.91 s
==============================

Time results saved to results/wadi/time_results.json

==============================
STARTING EVALUATION (PAPER STYLE)
==============================
Skip wadi (missing files)
No results!