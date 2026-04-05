Found Kaggle dataset at: /kaggle/input/datasets/mgusat/smd-onmiad/ServerMachineDataset
46.2s	154	Copying /kaggle/input/datasets/mgusat/smd-onmiad/ServerMachineDataset/train to /kaggle/working/carla_bilstm/datasets/smd/train...
52.0s	155	Copying /kaggle/input/datasets/mgusat/smd-onmiad/ServerMachineDataset/test to /kaggle/working/carla_bilstm/datasets/smd/test...
57.2s	156	Copying /kaggle/input/datasets/mgusat/smd-onmiad/ServerMachineDataset/test_label to /kaggle/working/carla_bilstm/datasets/smd/test_label...
57.5s	157	Found total 28 datasets in smd.
57.5s	158	PHASE 1: Running first 14 datasets.
57.5s	159	
57.5s	160	==============================
57.5s	161	STARTING EXPERIMENTS SMD - PHASE 1
57.5s	162	==============================
57.8s	163	GPU available: Tesla T4
57.8s	164	
57.8s	165	Running dataset: machine-1-1.txt
128.0s	166	Error running pretext for machine-1-1.txt: Command '['/usr/bin/python3', 'carla_pretext.py', '--config_env', 'configs/env.yml', '--config_exp', 'configs/pretext/carla_pretext_smd.yml', '--fname', 'machine-1-1.txt']' returned non-zero exit status 1.
128.0s	167	Traceback (most recent call last):
128.0s	168	  File "/kaggle/working/carla_bilstm/carla_pretext.py", line 240, in <module>
128.0s	169	    main()
128.0s	170	  File "/kaggle/working/carla_bilstm/carla_pretext.py", line 196, in main
128.0s	171	    tmp_loss = pretext_train(train_dataloader, model, criterion, optimizer, epoch, prev_loss, device=device)
128.0s	172	               ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
128.0s	173	  File "/kaggle/working/carla_bilstm/utils/train_utils.py", line 32, in pretext_train
128.0s	174	    output = model(input_)
128.0s	175	             ^^^^^^^^^^^^^
128.0s	176	  File "/usr/local/lib/python3.12/dist-packages/torch/nn/modules/module.py", line 1776, in _wrapped_call_impl
128.0s	177	    return self._call_impl(*args, **kwargs)
128.0s	178	           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
128.0s	179	  File "/usr/local/lib/python3.12/dist-packages/torch/nn/modules/module.py", line 1787, in _call_impl
128.0s	180	    return forward_call(*args, **kwargs)
128.0s	181	           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
128.0s	182	  File "/kaggle/working/carla_bilstm/models/models.py", line 26, in forward
128.0s	183	    features = self.backbone(x)
128.0s	184	               ^^^^^^^^^^^^^^^^
128.0s	185	  File "/usr/local/lib/python3.12/dist-packages/torch/nn/modules/module.py", line 1776, in _wrapped_call_impl
128.0s	186	    return self._call_impl(*args, **kwargs)
128.0s	187	           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
128.0s	188	  File "/usr/local/lib/python3.12/dist-packages/torch/nn/modules/module.py", line 1787, in _call_impl
128.0s	189	    return forward_call(*args, **kwargs)
128.0s	190	           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
128.0s	191	  File "/kaggle/working/carla_bilstm/models/resent_time.py", line 146, in forward
128.0s	192	    out, _ = self.lstm(x)
128.0s	193	             ^^^^^^^^^^^^
128.0s	194	  File "/usr/local/lib/python3.12/dist-packages/torch/nn/modules/module.py", line 1776, in _wrapped_call_impl
128.0s	195	    return self._call_impl(*args, **kwargs)
128.0s	196	           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
128.0s	197	  File "/usr/local/lib/python3.12/dist-packages/torch/nn/modules/module.py", line 1787, in _call_impl
128.0s	198	    return forward_call(*args, **kwargs)
128.0s	199	           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
128.0s	200	  File "/usr/local/lib/python3.12/dist-packages/torch/nn/modules/rnn.py", line 1118, in forward
128.0s	201	    self.check_forward_args(input, hx, batch_sizes)
128.0s	202	  File "/usr/local/lib/python3.12/dist-packages/torch/nn/modules/rnn.py", line 1015, in check_forward_args
128.0s	203	    self.check_input(input, batch_sizes)
128.0s	204	  File "/usr/local/lib/python3.12/dist-packages/torch/nn/modules/rnn.py", line 316, in check_input
128.0s	205	    raise RuntimeError(
128.0s	206	RuntimeError: input.size(-1) must be equal to input_size. Expected 55, got 38
128.0s	207	
132.6s	208	Error running classification for machine-1-1.txt: Command '['/usr/bin/python3', 'carla_classification.py', '--config_env', 'configs/env.yml', '--config_exp', 'configs/classification/carla_classification_smd.yml', '--fname', 'machine-1-1.txt']' returned non-zero exit status 1.
132.6s	209	Traceback (most recent call last):
132.6s	210	  File "/kaggle/working/carla_bilstm/carla_classification.py", line 216, in <module>
132.6s	211	    main()
132.6s	212	  File "/kaggle/working/carla_bilstm/carla_classification.py", line 52, in main
132.6s	213	    train_dataset = get_aug_train_dataset(p, train_transformations, to_neighbors_dataset = True)