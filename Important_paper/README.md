# 1. Important Paper for us 

**这个章节包含了几篇对我们研究十分重要的顶会论文，需仔细调研阅读**

## [[CVPR 2025] **Neuro-3D: Towards 3D Visual Decoding from EEG Signals**](Neuro-3D_Towards_3D_Visual_Decoding_from_EEG_Signals_CVPR_2025.pdf)
  
  *Guo, Jia and Lu, Shuai and Zhang, Weihang and Chen, Fang and Li, Huiqi and Liao, Hongen* [:octocat:code](https://github.com/gzq17/neuro-3D)

<div align="center">
  <img src="https://github.com/user-attachments/assets/93cfe9fb-49ae-4d40-b1ed-cd12389a0cd8" width="80%">
</div>

<details close>
<summary><b>📋 Abstract (Click to Expand)</b></summary>
Human's perception of the visual world is shaped by the stereo processing of 3D information. Understanding how the brain perceives and processes 3D visual stimuli in the real world has been a longstanding endeavor in neuroscience. Towards this goal, we introduce a new neuroscience task: decoding 3D visual perception from EEG signals, a neuroimaging technique that enables real-time monitoring of neural dynamics enriched with complex visual cues. To provide the essential benchmark, we first present EEG-3D, a pioneering dataset featuring multimodal analysis data and extensive EEG recordings from 12 subjects viewing 72 categories of 3D objects rendered in both videos and images. Furthermore, we propose Neuro-3D, a 3D visual decoding framework based on EEG signals. This framework adaptively integrates EEG features derived from static and dynamic stimuli to learn complementary and robust neural representations, which are subsequently utilized to recover both the shape and color of 3D objects through the proposed diffusion-based colored point cloud decoder. To the best of our knowledge, we are the first to explore EEG-based 3D visual decoding. Experiments indicate that Neuro-3D not only reconstructs colored 3D objects with high fidelity, but also learns effective neural representations that enable insightful brain region analysis.
</details>

<details close>
<summary><b>📋 2025.8.15 对比实验调研 cjh</b></summary>
<div align="center">
  <img src="https://github.com/user-attachments/assets/93cfe9fb-49ae-4d40-b1ed-cd12389a0cd8" width="80%">
</div>
</details>

<details close>
<summary><b>📋 为什么加入fMRI的数据集进行对比 cyf </b></summary>
<div align="center">
  <img src="https://github.com/user-attachments/assets/9e839734-68aa-4bb9-8e1b-6fa1a5e3d213" width="80%">
</div>
      论文通过fMRI重建3D的不足与缺陷引出EEG重建3D的优点与创新，所以在数据集对比时会加入相关的fMRI数据集
</details>

## [[CVPR 2025] **NSD-Imagery: A benchmark dataset for extending fMRI vision decoding methods to mental imagery**](https://arxiv.org/abs/2506.06898)
<details close>

  *Reese Kneeland, Paul S. Scotti, Ghislain St-Yves, Jesse Breedlove, Kendrick Kay, Thomas Naselaris* [:octocat:code](https://www.naturalscenesdataset.org/)

<div align="center">
  <img src="https://github.com/user-attachments/assets/faf4b8a2-72ba-4aa1-8af3-a18cec0b8076" width="80%">
</div>

<details close>
<summary><b>📋 2025.8.18 初次总结 cjh</b></summary>
这篇论文发布了一个名为 **NSD-Imagery** 的新基准数据集。该数据集记录了人类在进行“心理想象”时的大脑功能性磁共振成像（fMRI）活动。

**核心内容和主要发现：**

1.  **对现有数据集的补充：** NSD-Imagery 是对现有的大型数据集 NSD (Natural Scenes Dataset) 的补充。NSD 数据集记录的是人们在“看到”实际图像时的大脑 fMRI 活动，而 NSD-Imagery 则专注于“想象”出的图像。

2.  **新的评估维度：** 此前，基于 NSD 数据集训练的各种先进模型（如 MindEye, Brain Diffuser 等）都只在“看到的图像”重建任务上进行过评估。NSD-Imagery 的发布，使得研究人员可以首次评估这些模型在重建“心理图像”方面的表现如何。

3.  **“想象”比“看见”更具挑战性：** 从大脑活动中重建心理图像是一个巨大的挑战，因为心理图像在大脑中编码的信号信噪比和空间分辨率都相对较低。然而，能否成功地从“看见”的解码模型泛化到“想象”的解码，对于医疗、脑机接口等实际应用至关重要，因为在这些场景中，需要解码的信息往往是内部产生的（即“想象”）。

4.  **关键发现——模型表现与架构有关：**
    *   一个模型在重建“看到的图像”方面表现好，并不意味着它在重建“心理图像”方面也同样出色。两者的性能在很大程度上是**不相关**的。
    *   模型的**架构选择**对泛化到心理图像的能力有显著影响。采用简单线性解码架构和多模态特征解码的模型，其泛化能力更好。
    *   相比之下，那些架构复杂的模型更容易对“看到的图像”训练数据产生过拟合，导致在处理心理图像时效果不佳。

**结论：**

作者们认为，要开发出真正实用的视觉解码应用（如脑机接口），使用像 NSD-Imagery 这样的心理意象数据集进行模型训练和评估是至关重要的。他们将 NSD-Imagery 作为一个宝贵的资源，旨在推动视觉解码方法更好地服务于这一最终目标。

**应用前景**

*   **医疗诊断：** 开发用于精神疾病的诊断工具，特别是那些与侵入性或负面情绪的心理意象相关的疾病（如 PTSD、焦虑症等）。
*   **替代性交流：** 为那些因各种原因无法通过常规方式（如语言）进行交流的患者提供一种新的沟通方法。
*   **意识检测（重点应用）：**
    *   全球每年有 5000 万人遭受创伤性脑损伤，其中约 15-20% 的患者可能处于“隐蔽性意识（covertly conscious）”状态，即外表看起来没有反应，但内心仍有意识。
    *   利用这种非侵入性的脑成像技术，来解码出患者想象的可验证内容（比如问一个只有他知道答案的问题，让他想象答案），可以帮助准确诊断这类患者，从而**防止生命支持系统被过早地撤除**。
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

## [[CVPR 2025] **Bridging the Vision-Brain Gap with an Uncertainty-Aware Blur Prior**](https://arxiv.org/abs/2503.04207)
  
  *Haitao Wu, Qing Li, Changqing Zhang, Zhen He, Xiaomin Ying* [:octocat:code](https://github.com/HaitaoWuTJU/Uncertainty-aware-Blur-Prior)

<div align="center">
  <img src="https://github.com/user-attachments/assets/091c9927-e982-4871-a8a9-26f5b5b1ad2e" width="80%">
</div>

<details close>
<summary><b>📋 2025.8.18 初次阅读 cjh</b></summary>
这篇论文的核心思想非常巧妙，它探讨并解决了一个在“从脑信号解码图像”任务中的关键问题：**我们的大脑信号并不完美，充满了信息损失和噪声，直接用它来对齐清晰的原始图像会让模型“学得很痛苦”，导致性能不佳。**

---

### **核心摘要**

为了解决脑信号与原始视觉图像之间的“保真度差距”，研究者提出了一种简单而高效的新方法，名为**“不确定性感知模糊先验”（Uncertainty-aware Blur Prior, UBP）**。该方法的核心是：**在训练时，主动地、有策略地将原始图像进行模糊处理，使其在信息层面上更接近于“不完整”的脑信号**。通过这种方式，模型不再需要费力地去弥补一个巨大的信息鸿沟，从而能更好地学习两者间的真实对应关系，显著提升了解码的准确性。

---

### **详细分解**

1.  **提出了两个核心问题（两个GAP）：**
    *   **系统性差距 (System GAP):** 当我们看一个东西时，由于人类视觉系统的物理限制（比如注意力和记忆力有限），一些信息在转化为脑信号的过程中就**必然丢失**了。例如，图像中非常精细的、高频的细节可能无法被大脑完全编码。
    *   **随机性差距 (Random GAP):** 除了系统性的信息损失，还有很多**随机因素**会进一步降低脑信号的质量，比如我们看东西时的认知状态波动、测量设备本身带来的技术噪声等。

2.  **指出了当前方法的困境：**
    *   传统的解码模型试图直接将“不完美的”脑信号与“完美的”高清图像进行配对学习。
    *   由于上述两个“差距”的存在，这种配对实际上是**不匹配**的。
    *   在训练数据有限的情况下，模型很难学会如何跨越这个巨大的信息鸿沟，最终导致**过拟合**——模型只是死记硬背了训练样本，而对于新的、没见过的脑信号，其泛化能力会很差。

3.  **提出了创新的解决方案 (UBP):**
    *   **核心思路：** 与其强迫模型去弥补这个差距，不如主动把这个差距“填平”一部分。具体做法是，**降低完美图像的质量，让它向不完美的脑信号“靠拢”**。
    *   **具体方法：**
        1.  首先，模型会**评估**每一对“脑信号-图像”数据之间的**不确定性（uncertainty）**。这种不确定性的大小，就反映了这对数据之间的“差距”有多大。
        2.  然后，基于这个评估出的不确定性程度，UBP会**动态地**对原始图像进行**高斯模糊**处理。
        3.  **差距大（不确定性高）** -> **模糊程度就高**，丢掉更多高频细节。
        4.  **差距小（不确定性低）** -> **模糊程度就低**，保留更多图像细节。
    *   **最终效果：** 通过这种方式，模糊后的图像在信息内容上与脑信号更加匹配，降低了模型学习对齐的难度，从而改善了模型的性能。

4.  **展示了卓越的成果：**
    *   该方法在“零样本脑信号到图像检索”任务上取得了当前最先进（SOTA）的成果。
    *   **Top-1 准确率达到 50.9%**（比之前最好的方法高了13.7个百分点）。
    *   **Top-5 准确率达到 79.7%**（比之前最好的方法高了9.8个百分点）。
    *   这是一个非常显著的性能提升，证明了该方法的有效性。

<div align="center">
  <img src="https://github.com/user-attachments/assets/dbb5e2b6-f176-42ca-b684-24503a986f61" width="80%">
</div>

**一句话总结：** 这篇论文不再强求模型去学习一个从“噪声信号”到“高清图像”的不可能任务，而是通过智能地“模糊”高清图像，创造了一个从“噪声信号”到“模糊图像”的更简单的任务，结果效果拔群。
</details>

[![](https://capsule-render.vercel.app/api?type=waving&height=200&color=0:0F172A,65:4F46E5,100:22D3EE&text=Click%20and%20Back%20to%20Content&section=footer&fontSize=30&fontAlignY=65&fontColor=FFFFFF)](../README.md)
