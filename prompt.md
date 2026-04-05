STARTING EXPERIMENTS
39.0s	43	==============================
39.3s	44	GPU available: Tesla T4
39.3s	45	
39.3s	46	Running dataset: M-6
51.8s	47	Error running pretext for M-6: Command '['/usr/bin/python3', 'carla_pretext.py', '--config_env', 'configs/env.yml', '--config_exp', 'configs/pretext/carla_pretext_msl.yml', '--fname', 'M-6']' returned non-zero exit status 1.
51.8s	48	Traceback (most recent call last):
51.8s	49	  File "/kaggle/working/carla_bilstm/carla_pretext.py", line 15, in <module>
51.8s	50	    from utils.repository import TSRepository
51.8s	51	  File "/kaggle/working/carla_bilstm/utils/repository.py", line 4, in <module>
51.8s	52	    import faiss
51.8s	53	ModuleNotFoundError: No module named 'faiss'
51.8s	54	
58.0s	55	Error running classification for M-6: Command '['/usr/bin/python3', 'carla_classification.py', '--config_env', 'configs/env.yml', '--config_exp', 'configs/classification/carla_classification_msl.yml', '--fname', 'M-6']' returned non-zero exit status 1.
58.0s	56	Traceback (most recent call last):
58.0s	57	  File "/kaggle/working/carla_bilstm/carla_classification.py", line 216, in <module>
58.0s	58	    main()
58.0s	59	  File "/kaggle/working/carla_bilstm/carla_classification.py", line 52, in main
58.0s	60	    train_dataset = get_aug_train_dataset(p, train_transformations, to_neighbors_dataset = True)
58.0s	61	                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
58.0s	62	  File "/kaggle/working/carla_bilstm/utils/common_config.py", line 172, in get_aug_train_dataset
58.0s	63	    dataloader = torch.load(p['contrastive_dataset'], weights_only=False)
58.0s	64	                 ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
58.0s	65	  File "/usr/local/lib/python3.12/dist-packages/torch/serialization.py", line 1500, in load
58.0s	66	    with _open_file_like(f, "rb") as opened_file:
58.0s	67	         ^^^^^^^^^^^^^^^^^^^^^^^^
58.0s	68	  File "/usr/local/lib/python3.12/dist-packages/torch/serialization.py", line 768, in _open_file_like
58.0s	69	    return _open_file(name_or_buffer, mode)
58.0s	70	           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
58.0s	71	  File "/usr/local/lib/python3.12/dist-packages/torch/serialization.py", line 749, in __init__
58.0s	72	    super().__init__(open(name, mode))  # noqa: SIM115
58.0s	73	                     ^^^^^^^^^^^^^^^^
58.0s	74	FileNotFoundError: [Errno 2] No such file or directory: 'results/MSL/M-6/pretext/con_train_dataset.pth'
58.0s	75	
58.0s	76	Max GPU Memory after M-6: 0.00 MB
58.0s	77	
58.0s	78	Running dataset: M-1
63.8s	79	Error running pretext for M-1: Command '['/usr/bin/python3', 'carla_pretext.py', '--config_env', 'configs/env.yml', '--config_exp', 'configs/pretext/carla_pretext_msl.yml', '--fname', 'M-1']' returned non-zero exit status 1.
63.8s	80	Traceback (most recent call last):
63.8s	81	  File "/kaggle/working/carla_bilstm/carla_pretext.py", line 15, in <module>
63.8s	82	    from utils.repository import TSRepository
63.8s	83	  File "/kaggle/working/carla_bilstm/utils/repository.py", line 4, in <module>
63.8s	84	    import faiss
63.8s	85	ModuleNotFoundError: No module named 'faiss'
63.8s	86	
69.5s	87	Error running classification for M-1: Command '['/usr/bin/python3', 'carla_classification.py', '--config_env', 'configs/env.yml', '--config_exp', 'configs/classification/carla_classification_msl.yml', '--fname', 'M-1']' returned non-zero exit status 1.
69.5s	88	Traceback (most recent call last):
69.5s	89	  File "/kaggle/working/carla_bilstm/carla_classification.py", line 216, in <module>
69.5s	90	    main()
69.5s	91	  File "/kaggle/working/carla_bilstm/carla_classification.py", line 52, in main
69.5s	92	    train_dataset = get_aug_train_dataset(p, train_transformations, to_neighbors_dataset = True)
69.5s	93	                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
69.5s	94	  File "/kaggle/working/carla_bilstm/utils/common_config.py", line 172, in get_aug_train_dataset
69.5s	95	    dataloader = torch.load(p['contrastive_dataset'], weights_only=False)
69.5s	96	                 ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
69.5s	97	  File "/usr/local/lib/python3.12/dist-packages/torch/serialization.py", line 1500, in load
69.5s	98	    with _open_file_like(f, "rb") as opened_file:
69.5s	99	         ^^^^^^^^^^^^^^^^^^^^^^^^
69.5s	100	  File "/usr/local/lib/python3.12/dist-packages/torch/serialization.py", line 768, in _open_file_like
69.5s	101	    return _open_file(name_or_buffer, mode)
69.5s	102	           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
69.5s	103	  File "/usr/local/lib/python3.12/dist-packages/torch/serialization.py", line 749, in __init__
69.5s	104	    super().__init__(open(name, mode))  # noqa: SIM115
69.5s	105	                     ^^^^^^^^^^^^^^^^
69.5s	106	FileNotFoundError: [Errno 2] No such file or directory: 'results/MSL/M-1/pretext/con_train_dataset.pth'
69.5s	107	
69.5s	108	Max GPU Memory after M-1: 0.00 MB
69.5s	109	
69.5s	110	Running dataset: M-2
75.2s	111	Error running pretext for M-2: Command '['/usr/bin/python3', 'carla_pretext.py', '--config_env', 'configs/env.yml', '--config_exp', 'configs/pretext/carla_pretext_msl.yml', '--fname', 'M-2']' returned non-zero exit status 1.
75.2s	112	Traceback (most recent call last):
75.2s	113	  File "/kaggle/working/carla_bilstm/carla_pretext.py", line 15, in <module>
75.2s	114	    from utils.repository import TSRepository
75.2s	115	  File "/kaggle/working/carla_bilstm/utils/repository.py", line 4, in <module>
75.2s	116	    import faiss