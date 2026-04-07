!python run_swat.py
Found Kaggle dataset at: /kaggle/input/datasets/vishala28/swat-dataset-secure-water-treatment-system
Found merged dataset: /kaggle/input/datasets/vishala28/swat-dataset-secure-water-treatment-system/merged.csv
Processing merged dataset from /kaggle/input/datasets/vishala28/swat-dataset-secure-water-treatment-system/merged.csv...
Merged CSV columns: ['Timestamp', 'FIT101', 'LIT101', 'MV101', 'P101', 'P102', 'AIT201', 'AIT202', 'AIT203', 'FIT201', 'MV201', 'P201', 'P202', 'P203', 'P204', 'P205', 'P206', 'DPIT301', 'FIT301', 'LIT301', 'MV301', 'MV302', 'MV303', 'MV304', 'P301', 'P302', 'AIT401', 'AIT402', 'FIT401', 'LIT401', 'P401', 'P402', 'P403', 'P404', 'UV401', 'AIT501', 'AIT502', 'AIT503', 'AIT504', 'FIT501', 'FIT502', 'FIT503', 'FIT504', 'P501', 'P502', 'PIT501', 'PIT502', 'PIT503', 'FIT601', 'P601', 'P602', 'P603', 'Normal/Attack']
Converted 'Normal/Attack' -> 'attack' (0=Normal, 1=Attack)
  Label distribution: {0: 1387098, 1: 54621}
Split merged.csv into:
Train (swat_train.csv): 496800 rows
Test (swat_test.csv): 449919 rows
Set swat_DATASET_PATH to /kaggle/working/carla_bilstm/datasets/swat
Set swat_DATASET_PATH to /kaggle/working/carla_bilstm/datasets/swat

==============================
STARTING EXPERIMENTS
==============================
GPU available: Tesla T4

Running dataset: swat
Error running pretext for swat: Command '['/usr/bin/python3', 'carla_pretext.py', '--config_env', 'configs/env.yml', '--config_exp', 'configs/pretext/carla_pretext_swat.yml', '--fname', 'swat']' returned non-zero exit status 1.
Traceback (most recent call last):
  File "/kaggle/working/carla_bilstm/carla_pretext.py", line 240, in <module>
    main()
  File "/kaggle/working/carla_bilstm/carla_pretext.py", line 196, in main
    tmp_loss = pretext_train(train_dataloader, model, criterion, optimizer, epoch, prev_loss, device=device)
               ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/kaggle/working/carla_bilstm/utils/train_utils.py", line 20, in pretext_train
    for i, batch in enumerate(train_loader):
                    ^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/utils/data/dataloader.py", line 734, in __next__
    data = self._next_data()
           ^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/utils/data/dataloader.py", line 1516, in _next_data
    return self._process_data(data, worker_id)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/utils/data/dataloader.py", line 1551, in _process_data
    data.reraise()
  File "/usr/local/lib/python3.12/dist-packages/torch/_utils.py", line 769, in reraise
    raise exception
RuntimeError: Caught RuntimeError in DataLoader worker process 0.
Original Traceback (most recent call last):
  File "/usr/local/lib/python3.12/dist-packages/torch/utils/data/_utils/worker.py", line 349, in _worker_loop
    data = fetcher.fetch(index)  # type: ignore[possibly-undefined]
           ^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/utils/data/_utils/fetch.py", line 52, in fetch
    data = [self.dataset[idx] for idx in possibly_batched_index]
            ~~~~~~~~~~~~^^^^^
  File "/kaggle/working/carla_bilstm/data/custom_dataset.py", line 46, in __getitem__
    item = self.dataset.__getitem__(index)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/kaggle/working/carla_bilstm/data/SWAT.py", line 97, in __getitem__
    ts_org = torch.from_numpy(self.data[index]).float().to(device)  # cuda
             ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/cuda/__init__.py", line 398, in _lazy_init
    raise RuntimeError(
RuntimeError: Cannot re-initialize CUDA in forked subprocess. To use CUDA with multiprocessing, you must use the 'spawn' start method


Error running classification for swat: Command '['/usr/bin/python3', 'carla_classification.py', '--config_env', 'configs/env.yml', '--config_exp', 'configs/classification/carla_classification_swat.yml', '--fname', 'swat']' returned non-zero exit status 1.
Traceback (most recent call last):
  File "/kaggle/working/carla_bilstm/carla_classification.py", line 216, in <module>
    main()
  File "/kaggle/working/carla_bilstm/carla_classification.py", line 52, in main
    train_dataset = get_aug_train_dataset(p, train_transformations, to_neighbors_dataset = True)
                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/kaggle/working/carla_bilstm/utils/common_config.py", line 176, in get_aug_train_dataset
    data_dict = torch.load(p['contrastive_dataset'], weights_only=False)
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
FileNotFoundError: [Errno 2] No such file or directory: 'results/swat/swat/pretext/con_train_dataset.pth'

Max GPU Memory after swat: 0.00 MB

==============================
DONE ALL SWAT DATASETS
Total time: 23.16 s
Avg / dataset: 23.16 s
==============================

Time results saved to results/swat/time_results.json

==============================
STARTING EVALUATION (PAPER STYLE)
==============================
Skip swat (missing files)
No results!

và lỗi của khi chạy wadi:
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