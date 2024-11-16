<p align="center">
  <img src="assets/logo.jpg" height=100>
</p>
<div align="center">

## Deno (https://huggingface.co/spaces/svjack/MotionCtrl_SVD)
## MotionCtrl: A Unified and Flexible Motion Controller for Video Generation

#### [SIGGRAPH 2024 CONFERENCE PROCEEDINGS]

### <div align="center">👉 MotionCtrl for <b><a href="https://github.com/TencentARC/MotionCtrl/tree/svd">[SVD]</a>, for <a href="https://github.com/TencentARC/MotionCtrl/tree/main">[VideoCrafter]</a>, for <a href="https://github.com/TencentARC/MotionCtrl/tree/animatediff">[AnimateDiff]</a></b></div>

[![Paper](https://img.shields.io/badge/Paper-gray)](https://wzhouxiff.github.io/projects/MotionCtrl/assets/paper/MotionCtrl.pdf) &ensp; [![arXiv](https://img.shields.io/badge/arXiv-red)](https://arxiv.org/pdf/2312.03641.pdf) &ensp; [![Project Page](https://img.shields.io/badge/Project%20Page-green
)](https://wzhouxiff.github.io/projects/MotionCtrl/)

🤗 [![HF Demo](https://img.shields.io/static/v1?label=Demo&message=MotionCtrl%2BSVD&color=orange)](https://huggingface.co/spaces/TencentARC/MotionCtrl_SVD) &ensp; 🤗 [![HF Demo](https://img.shields.io/static/v1?label=Demo&message=MotionCtrl%2BVideoCrafter&color=orange)](https://huggingface.co/spaces/TencentARC/MotionCtrl)

</div>

---

## 🔥🔥🔥 We have released both **Training** and **Inference** code of MotionCtrl deployed on [AnimateDiff](https://github.com/TencentARC/MotionCtrl/tree/animatediff)

🔥🔥 We release the codes, [models](https://huggingface.co/TencentARC/MotionCtrl/tree/main) and [demos](https://huggingface.co/spaces/TencentARC/MotionCtrl_SVD) for MotionCtrl on [Stable Video Diffusion (SVD)](https://github.com/Stability-AI/generative-models).

---

https://github.com/TencentARC/MotionCtrl/assets/19488619/45d44bf5-d4bf-4e45-8628-2c8926b5954a

---


Official implementation of [MotionCtrl: A Unified and Flexible Motion Controller for Video Generation](https://arxiv.org/abs/2312.03641).

MotionCtrl can Independently control **complex camera motion** and **object motion** of generated videos, with **only a unified** model.

### Results of MotionCtrl+AnimateDiff

<div align="center">
    <img src="assets/animatediff/sample-d971457c81bca597-Photon.gif", width="600">
    <img src="assets/animatediff/sample-d971457c81bca597-HelloObject.gif", width="600">
    <img src="assets/animatediff/sample-SPIN-LR-HelloObject.gif", width="600">
    <img src="assets/animatediff/sample-none_motion-swaying_0.gif", width="600">
</div>

### Results of MotionCtrl+SVD

More results are in [showcase_svd](https://github.com/TencentARC/MotionCtrl/blob/svd/doc/showcase_svd.md) and our [Project Page](https://wzhouxiff.github.io/projects/MotionCtrl/).

<div align="center">
    <img src="assets/svd/00_ibzz5-dxv2h.gif", width="300">
    <img src="assets/svd/01_5guvn-0x6v2.gif", width="300">
    <img src="assets/svd/12_sn7bz-0hcaf.gif", width="300">
    <img src="assets/svd/13_3lyco-4ru8j.gif", width="300">
</div>


### Results of MotionCtrl+VideoCrafter

More results are in our [Project Page](https://wzhouxiff.github.io/projects/MotionCtrl/).

<div align="center">
    <img src="assets/hpxvu-3d8ym.gif", width="600">
    <img src="assets/w3nb7-9vz5t.gif", width="600">
    <img src="assets/62n2a-wuvsw.gif", width="600">
    <img src="assets/ilw96-ak827.gif", width="600">
</div>

---

## 📝 Changelog

- [x] 20231225: Release MotionCtrl deployed on ***LVDM/VideoCrafter***.
- [x] 20231225: Gradio demo available. 🤗 [![HF Demo](https://img.shields.io/static/v1?label=Demo&message=MotionCtrl%2BVideoCrafter&color=orange)](https://huggingface.co/spaces/TencentARC/MotionCtrl)
- [x] 20231228: Provide local gradio demo for convenience.
- [x] 20240115 More camera poses used for testing are provided in `dataset/camera_poses`
- [x] 20240115 Release MotionCtrl deployed on ***SVD***. Codes are in the branch [svd](https://github.com/TencentARC/MotionCtrl/tree/svd) and Gradio Demo is available in 🤗 [![HF Demo](https://img.shields.io/static/v1?label=Demo&message=MotionCtrl%2BSVD&color=orange)](https://huggingface.co/spaces/TencentARC/MotionCtrl_SVD).
- [x] ❗❗❗ Gradio demo of MotionCtrl deployed on ***VideoCrafter2*** is available in 🤗 [![HF Demo](https://img.shields.io/static/v1?label=Demo&message=MotionCtrl%2BVideoCrafter&color=orange)](https://huggingface.co/spaces/TencentARC/MotionCtrl). You can also run it locally by `python -m app --share`.
<!-- - [ ] ❗❗❗ ***Training Code*** will be released soon. -->
- [x] ❗❗❗ Release MotionCtrl deployed on ***AnimateDiff*** are available in branch [animatediff](https://github.com/TencentARC/MotionCtrl/tree/animatediff), containing both **training** and **inference** code.
- [x] 20240920 Provide scripts for collecting object trajectories with [ParticleSfM](https://github.com/bytedance/particle-sfm). 
- [x] 20240920 We provide a [HandyTrajDrawer](https://github.com/wzhouxiff/HandyTrajDrawer) to customize object trajectoires more conveniently.

---

## ⚙️ Environment
    conda create -n motionctrl python=3.10.6
    conda activate motionctrl
    pip install -r requirements.txt

## 💫 Inference

- #### Run local inference script

1. Download the weights of MotionCtrl [motionctrl.pth](https://huggingface.co/TencentARC/MotionCtrl/blob/main/motionctrl.pth) and put it to `./checkpoints`.
2. Go into `configs/inference/run.sh` and set `condtype` as 'camera_motion', 'object_motion', or 'both'.
- `condtype=camera_motion` means only control the **camera motion** in the generated video.
- `condtype=object_motion` means only control the **object motion** in the generated video.
- `condtype=both` means control the camera motion and object motion in the generated video **simultaneously**.
3. Running scripts:
        sh configs/inference/run.sh

- #### Run local gradio demo
      python -m app --share

## 🔥🔥 Training 👉 [Details](https://github.com/TencentARC/MotionCtrl/tree/animatediff?tab=readme-ov-file#-training)

###  Preparing Dataset
  - [RealEstate10K](https://google.github.io/realestate10k/)

    1.  Following https://github.com/cashiwamochi/RealEstate10K_Downloader to download and process the videos.
    2. Corresponding Captions and List are provided in [GoogleDrive](https://drive.google.com/drive/folders/1RYdBW3JUBYMUPdMHL2Yig6getEYN3Z3g?usp=drive_link).

  - [WebVid](https://www.v7labs.com/open-datasets/the-webvid-10m-dataset) with Object Trajectories
    1. Preparing [ParticleSfM](https://github.com/bytedance/particle-sfm). Our experiments is running on CentOS 8.5 and we provide a detailed install note in `dataset/object_trajectories/ParticleSfM_Install_Note.pdf`.
    2. Moving `dataset/object_trajectories/prepare_webvideo_len32.py` and `dataset/object_trajectories/run_particlesfm_obj_traj.py` to **ParticleSfM** project.
    3. Step 1: Prepare sub-videos with lenth of 32 and size of 256 x 256.
        ```
        ## start_idx and end_idx is used to process a subset of the dataset in different machines parallelly
        
        python prepare_webvideo_len32.py --start_idx 0 --end_idx 1000
        ```
    4. Step 2: Get object trajectories
      
        ```
          root_dir="WebVid/train_256_32"
          start_idx=0
          end_idx=1000

          CUDA_VISIBLE_DEVICES=0 python run_particlesfm_obj_traj.py \
          --root_dir $root_dir \
          --start_idx $start_idx \
          --end_idx $end_idx \
        ```

  - You can customize object Trajectories with our provided [HandyTrajDrawer](https://github.com/wzhouxiff/HandyTrajDrawer).


## :books: Citation
If you make use of our work, please cite our paper.
```bibtex
@inproceedings{wang2024motionctrl,
  title={Motionctrl: A unified and flexible motion controller for video generation},
  author={Wang, Zhouxia and Yuan, Ziyang and Wang, Xintao and Li, Yaowei and Chen, Tianshui and Xia, Menghan and Luo, Ping and Shan, Ying},
  booktitle={ACM SIGGRAPH 2024 Conference Papers},
  pages={1--11},
  year={2024}
}
```

## 🤗 Acknowledgment
The current version of **MotionCtrl** is built on [VideoCrafter](https://github.com/AILab-CVC/VideoCrafter). We appreciate the authors for sharing their awesome codebase.

## ❓ Contact
For any question, feel free to email `wzhoux@connect.hku.hk` or `zhouzi1212@gmail.com`.
