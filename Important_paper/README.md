# 1. Important Paper for us 

**这个章节包含了几篇对我们研究十分重要的顶会论文，需仔细调研阅读**

- [[CVPR 2025] **Neuro-3D: Towards 3D Visual Decoding from EEG Signals**](Neuro-3D_Towards_3D_Visual_Decoding_from_EEG_Signals_CVPR_2025.pdf)
  
  *Guo, Jia and Lu, Shuai and Zhang, Weihang and Chen, Fang and Li, Huiqi and Liao, Hongen*[:octocat:code](https://github.com/gzq17/neuro-3D)

<div align="center">
  <img src="https://github.com/user-attachments/assets/93cfe9fb-49ae-4d40-b1ed-cd12389a0cd8" width="80%">
</div>

<details close>
<summary><b>📋 Abstract (Click to Expand)</b></summary>
Human's perception of the visual world is shaped by the stereo processing of 3D information. Understanding how the brain perceives and processes 3D visual stimuli in the real world has been a longstanding endeavor in neuroscience. Towards this goal, we introduce a new neuroscience task: decoding 3D visual perception from EEG signals, a neuroimaging technique that enables real-time monitoring of neural dynamics enriched with complex visual cues. To provide the essential benchmark, we first present EEG-3D, a pioneering dataset featuring multimodal analysis data and extensive EEG recordings from 12 subjects viewing 72 categories of 3D objects rendered in both videos and images. Furthermore, we propose Neuro-3D, a 3D visual decoding framework based on EEG signals. This framework adaptively integrates EEG features derived from static and dynamic stimuli to learn complementary and robust neural representations, which are subsequently utilized to recover both the shape and color of 3D objects through the proposed diffusion-based colored point cloud decoder. To the best of our knowledge, we are the first to explore EEG-based 3D visual decoding. Experiments indicate that Neuro-3D not only reconstructs colored 3D objects with high fidelity, but also learns effective neural representations that enable insightful brain region analysis.
</details>

<details close>
<summary><b>📋 对比实验调研 </b></summary>
<div align="center">
  <img src="https://github.com/user-attachments/assets/93cfe9fb-49ae-4d40-b1ed-cd12389a0cd8" width="80%">
</div>
</details>

<details close>
<summary><b>📋 为什么加入fMRI的数据集进行对比？ </b></summary>
<div align="center">
  <img src="https://github.com/user-attachments/assets/9e839734-68aa-4bb9-8e1b-6fa1a5e3d213" width="80%">
</div>
      论文通过fMRI重建3D的不足与缺陷引出EEG重建3D的优点与创新，所以在数据集对比时会加入相关的fMRI数据集
</details>

- [[CVPR 2023] **High-resolution image reconstruction with latent diffusion models from human brain activity**](High-resolution_image_reconstruction_with_latent_diffusion_models_from_human_brain_activity.pdf)
  
  *Yu Takagi, Shinji Nishimoto* [:octocat:code](https://sites.google.com/view/stablediffusion-with-brain/)

<div align="center">
  <img src="https://github.com/user-attachments/assets/edf9a662-df79-4441-80d0-81faef41000b" width="40%">
</div>

<details close>
<summary><b>📋 Abstract (Click to Expand)</b></summary>
Reconstructing visual experiences from human brain activity offers a unique way to understand how the brain represents the world, and to interpret the connection between computer vision models and our visual system. While deep generative models have recently been employed for this task, reconstructing realistic images with high semantic fidelity is still a challenging problem. Here, we propose a new method based on a diffusion model (DM) to reconstruct images from human brain activity obtained via functional magnetic resonance imaging (fMRI). More specifically, we rely on a latent diffusion model (LDM) termed Stable Diffusion. This model reduces the computational cost of DMs, while preserving their high generative performance. We also characterize the inner mechanisms of the LDM by studying how its different components (such as the latent vector of image Z, conditioning inputs C, and different elements of the denoising U-Net) relate to distinct brain functions. We show that our proposed method can reconstruct high-resolution images with high fidelity in straight-forward fashion, without the need for any additional training and fine-tuning of complex deep-learning models. We also provide a quantitative interpretation of different LDM components from a neuroscientific perspective. Overall, our study proposes a promising method for reconstructing images from human brain activity, and provides a new framework for understanding DMs.
</details>

- [[CONFERENCE YEAR] **Paper Title Goes Here**](/path-to-paper)
  
  *Author, First and Author, Second and Author, Third* [:octocat:code](https://github.com/username/repository)

<div align="center">
  <img src="https://github.com/user-attachments/assets/your-image-asset-id" width="50%">
</div>

<details close>
<summary><b>📋 Abstract (Click to Expand)</b></summary>
Your abstract content goes here. 可以去arivx搜文章名字然后复制摘要。
</details>

[![](https://capsule-render.vercel.app/api?type=waving&height=200&color=0:0F172A,65:4F46E5,100:22D3EE&text=Click%20and%20Back%20to%20Content&section=footer&fontSize=30&fontAlignY=65&fontColor=FFFFFF)](../README.md)
