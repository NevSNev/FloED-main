![Qualitative Results](Assert/Fig1.jpg)

 

<h1 align="center" style="font-weight: bold; font-size: 2.5rem;">
  FloED: <span style="font-size: 1.5rem; font-weight: normal; color: #555;">Coherent Video Inpainting Using Optical Flow-Guided Efficient Diffusion</span>
</h1>


<div align="center">

Bohai Gu &emsp; Hao Luo &emsp; Song Guo &emsp; Peiran Dong  &emsp; Qihua Zhou  

HKUST, DAMO Academy, Alibaba Group

[![arXiv](https://img.shields.io/badge/arXiv-2412.00857-b31b1b)](https://arxiv.org/abs/2412.00857)
[![Project Page](https://img.shields.io/badge/Project-Website-orange)](https://nevsnev.github.io/FloED)
</div>



 <div class="content has-text-justified">
          <p>
      The text-guided video inpainting technique has significantly improved the performance of content generation applications. A recent family for these improvements uses diffusion models, which have become essential for achieving high-quality video inpainting results, yet they still face performance bottlenecks in temporal consistency and computational efficiency. This motivates us to propose a new video inpainting framework using optical Flow-guided Efficient Diffusion (FloED) for higher video coherence. Specifically, FloED employs a dual-branch architecture, where the time-agnostic flow branch restores corrupted flow first, and the multi-scale flow adapters provide motion guidance to the main inpainting branch. Besides, a training-free latent interpolation method is proposed to accelerate the multi-step denoising process using flow warping. With the flow attention cache mechanism, FLoED efficiently reduces the computational cost of incorporating optical flow. Extensive experiments on background restoration and object removal tasks show that FloED outperforms state-of-the-art diffusion-based methods in both quality and efficiency. 
          </p>
        </div>


![Method Overview](Assert/Fig_0.jpg)

**Video Demo**

![video demo](Assert/video.gif)


Please refer our [project page](https://nevsnev.github.io/FloED) for more details.



## 🔥 Update

- \[2025.04.13] 🔥 🔥 🔥  Inference code and weightd have been released.



## To-Do List

- [x] Release the inference code and weights.
- [ ] Release the latent interpolation code.
- [ ] Release the training code and evaluation benchmark.



## Install

### 1. Environment Setup

 You can install the necessary dependencies using the following command:

```shell
conda env create -f environment.yaml
```

### 2. Preparing the Checkpoints

Download the FloED [weights](https://drive.google.com/file/d/1_P9_-63ChHDI3knqsx6VRLeqN2TMXHds/view?usp=sharing).



## Quick Start Inference



We provides several examples for OR and BR tasks.  Modifying the `motion_module` path in the text file.

```python
python -m scripts.animate --config configs/prompts/v3-inpainting.yaml
```

We have observed that saving results as **GIFs** may introduce noticeable flickering in videos. For higher-quality output, we recommend converting your results in **MP4 format** instead.

To test with your own videos and masks,  you can use the Stable Diffusion Inpainting script located at `Input/SD2/SD2.py` to generate an anchor frame.

## License

This project is developed based on [Animatediff](https://github.com/guoyww/AnimateDiff). Please refer to their original license for usage details.


## BibTeX

```bibtex
@misc{gu2025coherentvideoinpaintingusing,
      title={Coherent Video Inpainting Using Optical Flow-Guided Efficient Diffusion}, 
      author={Bohai Gu and Hao Luo and Song Guo and Peiran Dong and Qihua Zhou},
      year={2025},
      eprint={2412.00857},
      archivePrefix={arXiv},
      primaryClass={cs.CV},
      url={https://arxiv.org/abs/2412.00857}, 
}
