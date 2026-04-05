==============================
52.0s	159	STARTING EXPERIMENTS
52.0s	160	==============================
52.3s	161	GPU available: Tesla T4
52.3s	162	
52.3s	163	Running dataset: M-6
64.3s	164	Error running pretext for M-6: Command '['/usr/bin/python3', 'carla_pretext.py', '--config_env', 'configs/env.yml', '--config_exp', 'configs/pretext/carla_pretext_msl.yml', '--fname', 'M-6']' returned non-zero exit status 1.
64.3s	165	Traceback (most recent call last):
64.3s	166	  File "/kaggle/working/carla_bilstm/carla_pretext.py", line 240, in <module>
64.3s	167	    main()
64.3s	168	  File "/kaggle/working/carla_bilstm/carla_pretext.py", line 92, in main
64.3s	169	    train_dataset = get_train_dataset(p, train_transforms, sanomaly, to_augmented_dataset=True,
64.3s	170	                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
64.3s	171	  File "/kaggle/working/carla_bilstm/utils/common_config.py", line 94, in get_train_dataset
64.3s	172	    dataset = MSL(p['fname'], train=True, transform=transform, sanomaly=sanomaly,
64.3s	173	              ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
64.3s	174	  File "/kaggle/working/carla_bilstm/data/MSL.py", line 29, in __init__
64.3s	175	    with open(os.path.join(self.root, 'labeled_anomalies.csv'), 'r') as file:
64.3s	176	         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
64.3s	177	FileNotFoundError: [Errno 2] No such file or directory: '/kaggle/working/carla_bilstm/datasets/MSL/labeled_anomalies.csv'
64.3s	178	
69.0s	179	Error running classification for M-6: Command '['/usr/bin/python3', 'carla_classification.py', '--config_env', 'configs/env.yml', '--config_exp', 'configs/classification/carla_classification_msl.yml', '--fname', 'M-6']' returned non-zero exit status 1.
69.0s	180	Traceback (most recent call last):
69.0s	181	  File "/kaggle/working/carla_bilstm/carla_classification.py", line 216, in <module>
69.0s	182	    main()
69.0s	183	  File "/kaggle/working/carla_bilstm/carla_classification.py", line 52, in main
69.0s	184	    train_dataset = get_aug_train_dataset(p, train_transformations, to_neighbors_dataset = True)
69.0s	185	                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
69.0s	186	  File "/kaggle/working/carla_bilstm/utils/common_config.py", line 172, in get_aug_train_dataset
69.0s	187	    dataloader = torch.load(p['contrastive_dataset'], weights_only=False)
69.0s	188	                 ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
69.0s	189	  File "/usr/local/lib/python3.12/dist-packages/torch/serialization.py", line 1500, in load
69.0s	190	    with _open_file_like(f, "rb") as opened_file:
69.0s	191	         ^^^^^^^^^^^^^^^^^^^^^^^^
69.0s	192	  File "/usr/local/lib/python3.12/dist-packages/torch/serialization.py", line 768, in _open_file_like
69.0s	193	    return _open_file(name_or_buffer, mode)
69.0s	194	           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
69.0s	195	  File "/usr/local/lib/python3.12/dist-packages/torch/serialization.py", line 749, in __init__
69.0s	196	    super().__init__(open(name, mode))  # noqa: SIM115
69.0s	197	                     ^^^^^^^^^^^^^^^^
69.0s	198	FileNotFoundError: [Errno 2] No such file or directory: 'results/MSL/M-6/pretext/con_train_dataset.pth'
69.0s	199	
69.0s	200	Max GPU Memory after M-6: 0.00 MB
69.0s	201	
69.0s	202	Running dataset: M-1
74.3s	203	Error running pretext for M-1: Command '['/usr/bin/python3', 'carla_pretext.py', '--config_env', 'configs/env.yml', '--config_exp', 'configs/pretext/carla_pretext_msl.yml', '--fname', 'M-1']' returned non-zero exit status 1.
74.3s	204	Traceback (most recent call last):
74.3s	205	  File "/kaggle/working/carla_bilstm/carla_pretext.py", line 240, in <module>
74.3s	206	    main()
74.3s	207	  File "/kaggle/working/carla_bilstm/carla_pretext.py", line 92, in main
74.3s	208	    train_dataset = get_train_dataset(p, train_transforms, sanomaly, to_augmented_dataset=True,
74.3s	209	                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
74.3s	210	  File "/kaggle/working/carla_bilstm/utils/common_config.py", line 94, in get_train_dataset
74.3s	211	    dataset = MSL(p['fname'], train=True, transform=transform, sanomaly=sanomaly,
74.3s	212	              ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
74.3s	213	  File "/kaggle/working/carla_bilstm/data/MSL.py", line 29, in __init__
74.3s	214	    with open(os.path.join(self.root, 'labeled_anomalies.csv'), 'r') as file:
74.3s	215	         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
74.3s	216	FileNotFoundError: [Errno 2] No such file or directory: '/kaggle/working/carla_bilstm/datasets/MSL/labeled_anomalies.csv'
74.3s	217	
79.0s	218	Error running classification for M-1: Command '['/usr/bin/python3', 'carla_classification.py', '--config_env', 'configs/env.yml', '--config_exp', 'configs/classification/carla_classification_msl.yml', '--fname', 'M-1']' returned non-zero exit status 1.
79.0s	219	Traceback (most recent call last):
79.0s	220	  File "/kaggle/working/carla_bilstm/carla_classification.py", line 216, in <module>
79.0s	221	    main()
79.0s	222	  File "/kaggle/working/carla_bilstm/carla_classification.py", line 52, in main
79.0s	223	    train_dataset = get_aug_train_dataset(p, train_transformations, to_neighbors_dataset = True)
79.0s	224	                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
79.0s	225	  File "/kaggle/working/carla_bilstm/utils/common_config.py", line 172, in get_aug_train_dataset
79.0s	226	    dataloader = torch.load(p['contrastive_dataset'], weights_only=False)
79.0s	227	                 ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
79.0s	228	  File "/usr/local/lib/python3.12/dist-packages/torch/serialization.py", line 1500, in load
79.0s	229	    with _open_file_like(f, "rb") as opened_file:
79.0s	230	         ^^^^^^^^^^^^^^^^^^^^^^^^
79.0s	231	  File "/usr/local/lib/python3.12/dist-packages/torch/serialization.py", line 768, in _open_file_like
79.0s	232	    return _open_file(name_or_buffer, mode)
79.0s	233	           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
79.0s	234	  File "/usr/local/lib/python3.12/dist-packages/torch/serialization.py", line 749, in __init__
79.0s	235	    super().__init__(open(name, mode))  # noqa: SIM115
79.0s	236	                     ^^^^^^^^^^^^^^^^
79.0s	237	FileNotFoundError: [Errno 2] No such file or directory: 'results/MSL/M-1/pretext/con_train_dataset.pth'
79.0s	238	
79.0s	239	Max GPU Memory after M-1: 0.00 MB