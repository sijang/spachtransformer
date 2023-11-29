
# Spach Transformer: Spatial and Channel-wise Transformer Based on Local and Global Self-attentions for PET Image Denoising


[Se-In Jang](https://scholar.google.co.kr/citations?user=I7zRmqkAAAAJ&hl=en), [Tinsu Pan](https://faculty.mdanderson.org/profiles/tinsu_pan.html), [Gary Y. Li](https://scholar.google.com/citations?user=Zy1GPkUAAAAJ&hl=en), [Pedram Heidari](https://scholar.google.com/citations?hl=en&user=V9faymoAAAAJ&view_op=list_works&sortby=pubdate), [Junyu Chen](https://scholar.google.com/citations?hl=en&user=9jIpgScAAAAJ&view_op=list_works&sortby=pubdate), [Quanzheng Li](https://scholar.google.com/citations?hl=en&user=MHq2z7oAAAAJ), and [Kuang Gong](https://scholar.google.com/citations?user=zc6kc4kAAAAJ&hl=en)

[![paper](https://img.shields.io/badge/arXiv-Paper-<COLOR>.svg)](https://arxiv.org/abs/2209.03300)

### News
- **Nov 2023:** Accepted in IEEE Transactions on Medical Imaging! [[Paper]](https://ieeexplore.ieee.org/document/10327759)

### Brief Introduction
- The focus of this project is on handling 3D PET input data.
- It incorporates a 3D-based approach, utilizing both the Swin Transformer and Restormer architectures specifically adapted for 3D data processing.


### Installation

See [INSTALL.md](INSTALL.md) for the installation of dependencies required to run Spach Transformer.


### Quick Run
```
import torch
from model.SpachTransformer import SpachTransformer

model = SpachTransformer()
input = torch.rand(1, 1, 96, 96, 96)
output = model(input)
```

<hr />

> **Abstract:** *Position emission tomography (PET) is widely used in clinics and research due to its quantitative merits and high sensitivity, but suffers from low signal-to-noise ratio (SNR). Recently convolutional neural networks (CNNs) have been widely used to improve PET image quality. Though successful and efficient in local feature extraction, CNN cannot capture long-range dependencies well due to its limited receptive field. Global multi-head self-attention (MSA) is a popular approach to capture long-range information. However, the calculation of global MSA for 3D images has high computational costs. In this work, we proposed an efficient spatial and channel-wise encoder-decoder transformer, Spach Transformer, that can leverage spatial and channel information based on local and global MSAs. Experiments based on datasets of different PET tracers, i.e., 18F-FDG, 18F-ACBC, 18F-DCFPyL, and 68Ga-DOTATATE, were conducted to evaluate the proposed framework. Quantitative results show that the proposed Spach Transformer can achieve better performance than other reference methods.* 
<hr />



### Citation
If you use Spach Transformer, please consider citing:

    @article{jang2022spach, 
        title={Spach Transformer: Spatial and channel-wise transformer based on local and global self-attentions for PET image denoising}, 
        author={Jang, Se-In and Pan, Tinsu and Li, Ye and Heidari, Pedram and Chen, Junyu and Li, Quanzheng and Gong, Kuang}, 
        journal={arXiv preprint arXiv:2209.03300}, 
        year={2022} }
    }


### Contact
Should you have any question, please contact sjang7@mgh.harvard.edu


**Acknowledgment:** This code is based on the [Restormer](https://github.com/swz30/Restormer) and [Swin Transformer](https://github.com/microsoft/Swin-Transformer).
