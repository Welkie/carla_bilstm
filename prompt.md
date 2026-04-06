!git clone https://github.com/Welkie/carla_bilstm.git
Cloning into 'carla_bilstm'...
remote: Enumerating objects: 126, done.
remote: Counting objects: 100% (126/126), done.
remote: Compressing objects: 100% (93/93), done.
remote: Total 126 (delta 28), reused 122 (delta 24), pack-reused 0 (from 0)
Receiving objects: 100% (126/126), 1.08 MiB | 9.82 MiB/s, done.
Resolving deltas: 100% (28/28), done.
%cd carla_bilstm
/kaggle/working/carla_bilstm
!pip install -r requirements.txt
Collecting arch (from -r requirements.txt (line 1))
  Downloading arch-8.0.0-cp312-cp312-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl.metadata (13 kB)
Collecting faiss-cpu (from -r requirements.txt (line 2))
  Downloading faiss_cpu-1.13.2-cp310-abi3-manylinux_2_27_x86_64.manylinux_2_28_x86_64.whl.metadata (7.6 kB)
Requirement already satisfied: matplotlib>=3.7.0 in /usr/local/lib/python3.12/dist-packages (from -r requirements.txt (line 3)) (3.10.0)
Collecting numpy<2.0.0,>=1.24.0 (from -r requirements.txt (line 4))
  Downloading numpy-1.26.4-cp312-cp312-manylinux_2_17_x86_64.manylinux2014_x86_64.whl.metadata (61 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 61.0/61.0 kB 2.3 MB/s eta 0:00:00
Collecting pandas==2.2.2 (from -r requirements.txt (line 5))
  Downloading pandas-2.2.2-cp312-cp312-manylinux_2_17_x86_64.manylinux2014_x86_64.whl.metadata (19 kB)
Collecting scikit-learn==1.4.2 (from -r requirements.txt (line 6))
  Downloading scikit_learn-1.4.2-cp312-cp312-manylinux_2_17_x86_64.manylinux2014_x86_64.whl.metadata (11 kB)
Collecting scipy==1.13.1 (from -r requirements.txt (line 7))
  Downloading scipy-1.13.1-cp312-cp312-manylinux_2_17_x86_64.manylinux2014_x86_64.whl.metadata (60 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 60.6/60.6 kB 4.4 MB/s eta 0:00:00
Collecting seaborn==0.13.0 (from -r requirements.txt (line 8))
  Downloading seaborn-0.13.0-py3-none-any.whl.metadata (5.3 kB)
Requirement already satisfied: torch>=2.1.0 in /usr/local/lib/python3.12/dist-packages (from -r requirements.txt (line 9)) (2.10.0+cu128)
Requirement already satisfied: torchaudio>=2.1.0 in /usr/local/lib/python3.12/dist-packages (from -r requirements.txt (line 10)) (2.10.0+cu128)
Collecting torchmetrics==1.0.1 (from -r requirements.txt (line 11))
  Downloading torchmetrics-1.0.1-py3-none-any.whl.metadata (21 kB)
Requirement already satisfied: torchvision>=0.16.0 in /usr/local/lib/python3.12/dist-packages (from -r requirements.txt (line 12)) (0.25.0+cu128)
Requirement already satisfied: easydict>=1.10 in /usr/local/lib/python3.12/dist-packages (from -r requirements.txt (line 13)) (1.13)
Requirement already satisfied: pyyaml>=6.0 in /usr/local/lib/python3.12/dist-packages (from -r requirements.txt (line 14)) (6.0.3)
Requirement already satisfied: termcolor>=2.3.0 in /usr/local/lib/python3.12/dist-packages (from -r requirements.txt (line 15)) (3.3.0)
Requirement already satisfied: statsmodels>=0.14.0 in /usr/local/lib/python3.12/dist-packages (from -r requirements.txt (line 16)) (0.14.6)
Requirement already satisfied: python-dateutil>=2.8.2 in /usr/local/lib/python3.12/dist-packages (from pandas==2.2.2->-r requirements.txt (line 5)) (2.9.0.post0)
Requirement already satisfied: pytz>=2020.1 in /usr/local/lib/python3.12/dist-packages (from pandas==2.2.2->-r requirements.txt (line 5)) (2025.2)
Requirement already satisfied: tzdata>=2022.7 in /usr/local/lib/python3.12/dist-packages (from pandas==2.2.2->-r requirements.txt (line 5)) (2025.3)
Requirement already satisfied: joblib>=1.2.0 in /usr/local/lib/python3.12/dist-packages (from scikit-learn==1.4.2->-r requirements.txt (line 6)) (1.5.3)
Requirement already satisfied: threadpoolctl>=2.0.0 in /usr/local/lib/python3.12/dist-packages (from scikit-learn==1.4.2->-r requirements.txt (line 6)) (3.6.0)
Requirement already satisfied: packaging in /usr/local/lib/python3.12/dist-packages (from torchmetrics==1.0.1->-r requirements.txt (line 11)) (26.0)
Requirement already satisfied: lightning-utilities>=0.7.0 in /usr/local/lib/python3.12/dist-packages (from torchmetrics==1.0.1->-r requirements.txt (line 11)) (0.15.3)
Requirement already satisfied: contourpy>=1.0.1 in /usr/local/lib/python3.12/dist-packages (from matplotlib>=3.7.0->-r requirements.txt (line 3)) (1.3.3)
Requirement already satisfied: cycler>=0.10 in /usr/local/lib/python3.12/dist-packages (from matplotlib>=3.7.0->-r requirements.txt (line 3)) (0.12.1)
Requirement already satisfied: fonttools>=4.22.0 in /usr/local/lib/python3.12/dist-packages (from matplotlib>=3.7.0->-r requirements.txt (line 3)) (4.61.1)
Requirement already satisfied: kiwisolver>=1.3.1 in /usr/local/lib/python3.12/dist-packages (from matplotlib>=3.7.0->-r requirements.txt (line 3)) (1.4.9)
Requirement already satisfied: pillow>=8 in /usr/local/lib/python3.12/dist-packages (from matplotlib>=3.7.0->-r requirements.txt (line 3)) (11.3.0)
Requirement already satisfied: pyparsing>=2.3.1 in /usr/local/lib/python3.12/dist-packages (from matplotlib>=3.7.0->-r requirements.txt (line 3)) (3.3.2)
Requirement already satisfied: filelock in /usr/local/lib/python3.12/dist-packages (from torch>=2.1.0->-r requirements.txt (line 9)) (3.24.3)
Requirement already satisfied: typing-extensions>=4.10.0 in /usr/local/lib/python3.12/dist-packages (from torch>=2.1.0->-r requirements.txt (line 9)) (4.15.0)
Requirement already satisfied: setuptools in /usr/local/lib/python3.12/dist-packages (from torch>=2.1.0->-r requirements.txt (line 9)) (75.2.0)
Requirement already satisfied: sympy>=1.13.3 in /usr/local/lib/python3.12/dist-packages (from torch>=2.1.0->-r requirements.txt (line 9)) (1.14.0)
Requirement already satisfied: networkx>=2.5.1 in /usr/local/lib/python3.12/dist-packages (from torch>=2.1.0->-r requirements.txt (line 9)) (3.6.1)
Requirement already satisfied: jinja2 in /usr/local/lib/python3.12/dist-packages (from torch>=2.1.0->-r requirements.txt (line 9)) (3.1.6)
Requirement already satisfied: fsspec>=0.8.5 in /usr/local/lib/python3.12/dist-packages (from torch>=2.1.0->-r requirements.txt (line 9)) (2026.2.0)
Requirement already satisfied: cuda-bindings==12.9.4 in /usr/local/lib/python3.12/dist-packages (from torch>=2.1.0->-r requirements.txt (line 9)) (12.9.4)
Requirement already satisfied: nvidia-cuda-nvrtc-cu12==12.8.93 in /usr/local/lib/python3.12/dist-packages (from torch>=2.1.0->-r requirements.txt (line 9)) (12.8.93)
Requirement already satisfied: nvidia-cuda-runtime-cu12==12.8.90 in /usr/local/lib/python3.12/dist-packages (from torch>=2.1.0->-r requirements.txt (line 9)) (12.8.90)
Requirement already satisfied: nvidia-cuda-cupti-cu12==12.8.90 in /usr/local/lib/python3.12/dist-packages (from torch>=2.1.0->-r requirements.txt (line 9)) (12.8.90)
Requirement already satisfied: nvidia-cudnn-cu12==9.10.2.21 in /usr/local/lib/python3.12/dist-packages (from torch>=2.1.0->-r requirements.txt (line 9)) (9.10.2.21)
Requirement already satisfied: nvidia-cublas-cu12==12.8.4.1 in /usr/local/lib/python3.12/dist-packages (from torch>=2.1.0->-r requirements.txt (line 9)) (12.8.4.1)
Requirement already satisfied: nvidia-cufft-cu12==11.3.3.83 in /usr/local/lib/python3.12/dist-packages (from torch>=2.1.0->-r requirements.txt (line 9)) (11.3.3.83)
Requirement already satisfied: nvidia-curand-cu12==10.3.9.90 in /usr/local/lib/python3.12/dist-packages (from torch>=2.1.0->-r requirements.txt (line 9)) (10.3.9.90)
Requirement already satisfied: nvidia-cusolver-cu12==11.7.3.90 in /usr/local/lib/python3.12/dist-packages (from torch>=2.1.0->-r requirements.txt (line 9)) (11.7.3.90)
Requirement already satisfied: nvidia-cusparse-cu12==12.5.8.93 in /usr/local/lib/python3.12/dist-packages (from torch>=2.1.0->-r requirements.txt (line 9)) (12.5.8.93)
Requirement already satisfied: nvidia-cusparselt-cu12==0.7.1 in /usr/local/lib/python3.12/dist-packages (from torch>=2.1.0->-r requirements.txt (line 9)) (0.7.1)
Requirement already satisfied: nvidia-nccl-cu12==2.27.5 in /usr/local/lib/python3.12/dist-packages (from torch>=2.1.0->-r requirements.txt (line 9)) (2.27.5)
Requirement already satisfied: nvidia-nvshmem-cu12==3.4.5 in /usr/local/lib/python3.12/dist-packages (from torch>=2.1.0->-r requirements.txt (line 9)) (3.4.5)
Requirement already satisfied: nvidia-nvtx-cu12==12.8.90 in /usr/local/lib/python3.12/dist-packages (from torch>=2.1.0->-r requirements.txt (line 9)) (12.8.90)
Requirement already satisfied: nvidia-nvjitlink-cu12==12.8.93 in /usr/local/lib/python3.12/dist-packages (from torch>=2.1.0->-r requirements.txt (line 9)) (12.8.93)
Requirement already satisfied: nvidia-cufile-cu12==1.13.1.3 in /usr/local/lib/python3.12/dist-packages (from torch>=2.1.0->-r requirements.txt (line 9)) (1.13.1.3)
Requirement already satisfied: triton==3.6.0 in /usr/local/lib/python3.12/dist-packages (from torch>=2.1.0->-r requirements.txt (line 9)) (3.6.0)
Requirement already satisfied: cuda-pathfinder~=1.1 in /usr/local/lib/python3.12/dist-packages (from cuda-bindings==12.9.4->torch>=2.1.0->-r requirements.txt (line 9)) (1.3.5)
Requirement already satisfied: patsy>=0.5.6 in /usr/local/lib/python3.12/dist-packages (from statsmodels>=0.14.0->-r requirements.txt (line 16)) (1.0.2)
Requirement already satisfied: six>=1.5 in /usr/local/lib/python3.12/dist-packages (from python-dateutil>=2.8.2->pandas==2.2.2->-r requirements.txt (line 5)) (1.17.0)
Requirement already satisfied: mpmath<1.4,>=1.1.0 in /usr/local/lib/python3.12/dist-packages (from sympy>=1.13.3->torch>=2.1.0->-r requirements.txt (line 9)) (1.3.0)
Requirement already satisfied: MarkupSafe>=2.0 in /usr/local/lib/python3.12/dist-packages (from jinja2->torch>=2.1.0->-r requirements.txt (line 9)) (3.0.3)
Downloading pandas-2.2.2-cp312-cp312-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (12.7 MB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 12.7/12.7 MB 98.9 MB/s eta 0:00:00
Downloading scikit_learn-1.4.2-cp312-cp312-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (12.2 MB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 12.2/12.2 MB 101.2 MB/s eta 0:00:00
Downloading scipy-1.13.1-cp312-cp312-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (38.2 MB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 38.2/38.2 MB 52.9 MB/s eta 0:00:00
Downloading seaborn-0.13.0-py3-none-any.whl (294 kB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 294.6/294.6 kB 24.2 MB/s eta 0:00:00
Downloading torchmetrics-1.0.1-py3-none-any.whl (729 kB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 729.2/729.2 kB 40.7 MB/s eta 0:00:00
Downloading arch-8.0.0-cp312-cp312-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl (981 kB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 981.3/981.3 kB 51.7 MB/s eta 0:00:00
Downloading faiss_cpu-1.13.2-cp310-abi3-manylinux_2_27_x86_64.manylinux_2_28_x86_64.whl (23.8 MB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 23.8/23.8 MB 71.7 MB/s eta 0:00:00
Downloading numpy-1.26.4-cp312-cp312-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (18.0 MB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 18.0/18.0 MB 84.7 MB/s eta 0:00:00
Installing collected packages: numpy, scipy, pandas, faiss-cpu, scikit-learn, torchmetrics, seaborn, arch
  Attempting uninstall: numpy
    Found existing installation: numpy 2.0.2
    Uninstalling numpy-2.0.2:
      Successfully uninstalled numpy-2.0.2
  Attempting uninstall: scipy
    Found existing installation: scipy 1.16.3
    Uninstalling scipy-1.16.3:
      Successfully uninstalled scipy-1.16.3
  Attempting uninstall: pandas
    Found existing installation: pandas 2.3.3
    Uninstalling pandas-2.3.3:
      Successfully uninstalled pandas-2.3.3
  Attempting uninstall: scikit-learn
    Found existing installation: scikit-learn 1.6.1
    Uninstalling scikit-learn-1.6.1:
      Successfully uninstalled scikit-learn-1.6.1
  Attempting uninstall: torchmetrics
    Found existing installation: torchmetrics 1.9.0
    Uninstalling torchmetrics-1.9.0:
      Successfully uninstalled torchmetrics-1.9.0
  Attempting uninstall: seaborn
    Found existing installation: seaborn 0.13.2
    Uninstalling seaborn-0.13.2:
      Successfully uninstalled seaborn-0.13.2
ERROR: pip's dependency resolver does not currently take into account all the packages that are installed. This behaviour is the source of the following dependency conflicts.
bigframes 2.35.0 requires google-cloud-bigquery-storage<3.0.0,>=2.30.0, which is not installed.
kaggle-environments 1.27.3 requires numpy>=2.0, but you have numpy 1.26.4 which is incompatible.
tpot 1.1.0 requires scikit-learn>=1.6, but you have scikit-learn 1.4.2 which is incompatible.
tpot 1.1.0 requires seaborn>=0.13.2, but you have seaborn 0.13.0 which is incompatible.
cesium 0.12.4 requires numpy<3.0,>=2.0, but you have numpy 1.26.4 which is incompatible.
category-encoders 2.9.0 requires scikit-learn>=1.6.0, but you have scikit-learn 1.4.2 which is incompatible.
google-colab 1.0.0 requires jupyter-server==2.14.0, but you have jupyter-server 2.12.5 which is incompatible.
dopamine-rl 4.1.2 requires gym<=0.25.2, but you have gym 0.26.2 which is incompatible.
jaxlib 0.7.2 requires numpy>=2.0, but you have numpy 1.26.4 which is incompatible.
cupy-cuda12x 14.0.1 requires numpy<2.6,>=2.0, but you have numpy 1.26.4 which is incompatible.
opencv-python 4.13.0.92 requires numpy>=2; python_version >= "3.9", but you have numpy 1.26.4 which is incompatible.
tsfresh 0.21.1 requires scipy>=1.14.0; python_version >= "3.10", but you have scipy 1.13.1 which is incompatible.
cuml-cu12 26.2.0 requires scikit-learn>=1.5, but you have scikit-learn 1.4.2 which is incompatible.
shap 0.50.0 requires numpy>=2, but you have numpy 1.26.4 which is incompatible.
jax 0.7.2 requires numpy>=2.0, but you have numpy 1.26.4 which is incompatible.
umap-learn 0.5.11 requires scikit-learn>=1.6, but you have scikit-learn 1.4.2 which is incompatible.
opencv-python-headless 4.13.0.92 requires numpy>=2; python_version >= "3.9", but you have numpy 1.26.4 which is incompatible.
rasterio 1.5.0 requires numpy>=2, but you have numpy 1.26.4 which is incompatible.
hdbscan 0.8.41 requires scikit-learn>=1.6, but you have scikit-learn 1.4.2 which is incompatible.
tobler 0.13.0 requires numpy>=2.0, but you have numpy 1.26.4 which is incompatible.
xarray-einstats 0.10.0 requires numpy>=2.0, but you have numpy 1.26.4 which is incompatible.
pytensor 2.38.0 requires numpy>=2.0, but you have numpy 1.26.4 which is incompatible.
opencv-contrib-python 4.13.0.92 requires numpy>=2; python_version >= "3.9", but you have numpy 1.26.4 which is incompatible.
access 1.1.10.post3 requires scipy>=1.14.1, but you have scipy 1.13.1 which is incompatible.
Successfully installed arch-8.0.0 faiss-cpu-1.13.2 numpy-1.26.4 pandas-2.2.2 scikit-learn-1.4.2 scipy-1.13.1 seaborn-0.13.0 torchmetrics-1.0.1
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
Max GPU Memory after M-6: 684.10 MB

Running dataset: M-1
Max GPU Memory after M-1: 765.56 MB

Running dataset: M-2
Max GPU Memory after M-2: 765.56 MB

Running dataset: S-2
Max GPU Memory after S-2: 765.56 MB

Running dataset: P-10
Max GPU Memory after P-10: 1242.98 MB

Running dataset: T-4
Max GPU Memory after T-4: 1242.98 MB

Running dataset: T-5
Max GPU Memory after T-5: 1242.98 MB

Running dataset: F-7
Max GPU Memory after F-7: 1242.98 MB

Running dataset: M-3
Max GPU Memory after M-3: 1242.98 MB

Running dataset: M-4
Max GPU Memory after M-4: 1242.98 MB

Running dataset: M-5
Max GPU Memory after M-5: 1242.98 MB

Running dataset: P-15
Max GPU Memory after P-15: 1242.98 MB

Running dataset: C-1
Max GPU Memory after C-1: 1242.98 MB

Running dataset: C-2
Error running classification for C-2: Command '['/usr/bin/python3', 'carla_classification.py', '--config_env', 'configs/env.yml', '--config_exp', 'configs/classification/carla_classification_msl.yml', '--fname', 'C-2']' returned non-zero exit status 1.
Traceback (most recent call last):
  File "/kaggle/working/carla_bilstm/carla_classification.py", line 216, in <module>
    main()
  File "/kaggle/working/carla_bilstm/carla_classification.py", line 192, in main
    predictions = get_predictions(p, val_dataloader, model, False, False)
                  ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/utils/_contextlib.py", line 124, in decorate_context
    return func(*args, **kwargs)
           ^^^^^^^^^^^^^^^^^^^^^
  File "/kaggle/working/carla_bilstm/utils/evaluate_utils.py", line 74, in get_predictions
    res = model(ts.view(bs, h, w), forward_pass='return_all')
          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/nn/modules/module.py", line 1776, in _wrapped_call_impl
    return self._call_impl(*args, **kwargs)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/nn/modules/module.py", line 1787, in _call_impl
    return forward_call(*args, **kwargs)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/nn/parallel/data_parallel.py", line 197, in forward
    outputs = self.parallel_apply(replicas, inputs, module_kwargs)
              ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/nn/parallel/data_parallel.py", line 214, in parallel_apply
    return parallel_apply(
           ^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/nn/parallel/parallel_apply.py", line 133, in parallel_apply
    output.reraise()
  File "/usr/local/lib/python3.12/dist-packages/torch/_utils.py", line 775, in reraise
    raise exception
TypeError: Caught TypeError in replica 1 on device 1.
Original Traceback (most recent call last):
  File "/usr/local/lib/python3.12/dist-packages/torch/nn/parallel/parallel_apply.py", line 103, in _worker
    output = module(*input, **kwargs)
             ^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/nn/modules/module.py", line 1776, in _wrapped_call_impl
    return self._call_impl(*args, **kwargs)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/torch/nn/modules/module.py", line 1787, in _call_impl
    return forward_call(*args, **kwargs)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
TypeError: ClusteringModel.forward() missing 1 required positional argument: 'x'


Max GPU Memory after C-2: 1242.98 MB

Running dataset: T-12
Max GPU Memory after T-12: 1242.98 MB

Running dataset: T-13
Max GPU Memory after T-13: 1242.98 MB

Running dataset: F-4
Max GPU Memory after F-4: 1242.98 MB

Running dataset: F-5
Max GPU Memory after F-5: 1242.98 MB

Running dataset: D-14
Max GPU Memory after D-14: 1242.98 MB

Running dataset: T-9
Max GPU Memory after T-9: 1242.98 MB

Running dataset: P-14
Max GPU Memory after P-14: 1242.98 MB

Running dataset: T-8
Max GPU Memory after T-8: 1242.98 MB

Running dataset: P-11
Max GPU Memory after P-11: 1242.98 MB

Running dataset: D-15
Max GPU Memory after D-15: 1242.98 MB

Running dataset: D-16
Max GPU Memory after D-16: 1242.98 MB

Running dataset: M-7
Max GPU Memory after M-7: 1242.98 MB

Running dataset: F-8
Max GPU Memory after F-8: 1242.98 MB

==============================
DONE ALL MSL DATASETS
Total time: 5791.01 s
Avg / dataset: 214.48 s
==============================

Time results saved to results/msl/time_results.json

==============================
STARTING EVALUATION (PAPER STYLE)
==============================
Skip M-6 (missing files)
Skip M-1 (missing files)
Skip M-2 (missing files)
Skip S-2 (missing files)
Skip P-10 (missing files)
Skip T-4 (missing files)
Skip T-5 (missing files)
Skip F-7 (missing files)
Skip M-3 (missing files)
Skip M-4 (missing files)
Skip M-5 (missing files)
Skip P-15 (missing files)
Skip C-1 (missing files)
Skip C-2 (missing files)
Skip T-12 (missing files)
Skip T-13 (missing files)
Skip F-4 (missing files)
Skip F-5 (missing files)
Skip D-14 (missing files)
Skip T-9 (missing files)
Skip P-14 (missing files)
Skip T-8 (missing files)
Skip P-11 (missing files)
Skip D-15 (missing files)
Skip D-16 (missing files)
Skip M-7 (missing files)
Skip F-8 (missing files)
No results!