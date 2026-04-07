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
  File "/kaggle/working/carla_bilstm/carla_pretext.py", line 52, in main
    model = get_model(p)
            ^^^^^^^^^^^^
  File "/kaggle/working/carla_bilstm/utils/common_config.py", line 48, in get_model
    backbone = bilstm_ts(**p['res_kwargs'])
               ^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/kaggle/working/carla_bilstm/models/resent_time.py", line 154, in bilstm_ts
    return {'backbone': BiLSTMRepresentation(**kwargs), 'dim': hidden_size * 2}
                        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
TypeError: BiLSTMRepresentation.__init__() got an unexpected keyword argument 'mid_channels'

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
Total time: 17.22 s
Avg / dataset: 17.22 s
==============================

Time results saved to results/wadi/time_results.json

==============================
STARTING EVALUATION (PAPER STYLE)
==============================
Skip wadi (missing files)
No results!