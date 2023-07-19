My installation attempt starts at 2023.07. Due to Pytorch, CUDA and other environmental changes, when i follow the readme instructions i meet several issues, which i will write down here for record.

1. Although `conda env create -f environment.yml` is elegant, the installation will be interrupted when one package fails to be installed. If happens, i have to run `pip install` one by one.

2. Suggestions: 
- install `torch==1.11.0+cu113` instead of `torch=1.10.1+cu113`
- if `protobuf` meets errors, it will affect torch-scatter and torch-sparse since they are built from source. And `segmentation errors` may be found. Therefore, you can install them from this link(https://data.pyg.org/whl/) and follow the instructions from torch-sactter(https://github.com/rusty1s/pytorch_scatter) and torch-sparse(https://github.com/rusty1s/pytorch_sparse)
- Remember to  `--recursive` command when running `git clone git@github.com:romainloiseau/Helix4D.git --recursive`