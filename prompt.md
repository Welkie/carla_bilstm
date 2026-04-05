STARTING EXPERIMENTS
42.9s	145	==============================
43.2s	146	GPU available: Tesla T4
43.2s	147	
43.2s	148	Running dataset: P-1
70.3s	149	Error running pretext for P-1: Command '['/usr/bin/python3', 'carla_pretext.py', '--config_env', 'configs/env.yml', '--config_exp', 'configs/pretext/carla_pretext_smap.yml', '--fname', 'P-1']' returned non-zero exit status 1.
70.3s	150	Traceback (most recent call last):
70.3s	151	  File "/kaggle/working/carla_bilstm/carla_pretext.py", line 240, in <module>
70.3s	152	    main()
70.3s	153	  File "/kaggle/working/carla_bilstm/carla_pretext.py", line 196, in main
70.3s	154	    tmp_loss = pretext_train(train_dataloader, model, criterion, optimizer, epoch, prev_loss, device=device)
70.3s	155	               ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
70.3s	156	  File "/kaggle/working/carla_bilstm/utils/train_utils.py", line 32, in pretext_train
70.3s	157	    output = model(input_)
70.3s	158	             ^^^^^^^^^^^^^
70.3s	159	  File "/usr/local/lib/python3.12/dist-packages/torch/nn/modules/module.py", line 1773, in _wrapped_call_impl
70.3s	160	    return self._call_impl(*args, **kwargs)
70.3s	161	           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
70.3s	162	  File "/usr/local/lib/python3.12/dist-packages/torch/nn/modules/module.py", line 1784, in _call_impl
70.3s	163	    return forward_call(*args, **kwargs)
70.3s	164	           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
70.3s	165	  File "/kaggle/working/carla_bilstm/models/models.py", line 26, in forward
70.3s	166	    features = self.backbone(x)
70.3s	167	               ^^^^^^^^^^^^^^^^
70.3s	168	  File "/usr/local/lib/python3.12/dist-packages/torch/nn/modules/module.py", line 1773, in _wrapped_call_impl
70.3s	169	    return self._call_impl(*args, **kwargs)
70.3s	170	           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
70.3s	171	  File "/usr/local/lib/python3.12/dist-packages/torch/nn/modules/module.py", line 1784, in _call_impl
70.3s	172	    return forward_call(*args, **kwargs)
70.3s	173	           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
70.3s	174	  File "/kaggle/working/carla_bilstm/models/resent_time.py", line 146, in forward
70.3s	175	    out, _ = self.lstm(x)
70.3s	176	             ^^^^^^^^^^^^
70.3s	177	  File "/usr/local/lib/python3.12/dist-packages/torch/nn/modules/module.py", line 1773, in _wrapped_call_impl
70.3s	178	    return self._call_impl(*args, **kwargs)
70.3s	179	           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
70.3s	180	  File "/usr/local/lib/python3.12/dist-packages/torch/nn/modules/module.py", line 1784, in _call_impl
70.3s	181	    return forward_call(*args, **kwargs)
70.3s	182	           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
70.3s	183	  File "/usr/local/lib/python3.12/dist-packages/torch/nn/modules/rnn.py", line 1101, in forward
70.3s	184	    self.check_forward_args(input, hx, batch_sizes)
70.3s	185	  File "/usr/local/lib/python3.12/dist-packages/torch/nn/modules/rnn.py", line 1002, in check_forward_args
70.3s	186	    self.check_input(input, batch_sizes)
70.3s	187	  File "/usr/local/lib/python3.12/dist-packages/torch/nn/modules/rnn.py", line 315, in check_input
70.3s	188	    raise RuntimeError(
70.3s	189	RuntimeError: input.size(-1) must be equal to input_size. Expected 55, got 25
70.3s	190	
74.9s	191	Error running classification for P-1: Command '['/usr/bin/python3', 'carla_classification.py', '--config_env', 'configs/env.yml', '--config_exp', 'configs/classification/carla_classification_smap.yml', '--fname', 'P-1']' returned non-zero exit status 1.
74.9s	192	Traceback (most recent call last):
74.9s	193	  File "/kaggle/working/carla_bilstm/carla_classification.py", line 216, in <module>
74.9s	194	    main()
74.9s	195	  File "/kaggle/working/carla_bilstm/carla_classification.py", line 52, in main
74.9s	196	    train_dataset = get_aug_train_dataset(p, train_transformations, to_neighbors_dataset = True)
74.9s	197	                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
74.9s	198	  File "/kaggle/working/carla_bilstm/utils/common_config.py", line 173, in get_aug_train_dataset
74.9s	199	    dataloader = torch.load(p['contrastive_dataset'], weights_only=False)
74.9s	200	                 ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
74.9s	201	  File "/usr/local/lib/python3.12/dist-packages/torch/serialization.py", line 1484, in load
74.9s	202	    with _open_file_like(f, "rb") as opened_file:
74.9s	203	         ^^^^^^^^^^^^^^^^^^^^^^^^
74.9s	204	  File "/usr/local/lib/python3.12/dist-packages/torch/serialization.py", line 759, in _open_file_like
74.9s	205	    return _open_file(name_or_buffer, mode)
74.9s	206	           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
74.9s	207	  File "/usr/local/lib/python3.12/dist-packages/torch/serialization.py", line 740, in __init__
74.9s	208	    super().__init__(open(name, mode))
74.9s	209	                     ^^^^^^^^^^^^^^^^