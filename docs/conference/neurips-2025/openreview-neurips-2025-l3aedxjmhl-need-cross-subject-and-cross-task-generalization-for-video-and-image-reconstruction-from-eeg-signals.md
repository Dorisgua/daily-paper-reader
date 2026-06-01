---
title: "NEED: Cross-Subject and Cross-Task Generalization for Video and Image Reconstruction from EEG Signals"
title_zh: NEED：基于EEG信号的视频与图像重建的跨主体与跨任务泛化
authors: "Shuai Huang, Huan Luo, Haodong Jing, Qixian Zhang, Litao Chang, Yating Feng, Xiao Lin, Chendong Qin, Han Chen, Shuwen Jia, Siyi Sun, Yongxiong Wang"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=L3aEdxJMHl"
tags: ["query:eeg-latent"]
score: 9.0
evidence: 深度学习用于EEG信号重建：从EEG信号重建视觉内容
tldr: 现有EEG视觉重建方法跨主体泛化能力差且局限于特定视觉任务。本文提出NEED框架，通过个体自适应模块预处理多主体数据，结合对比学习和生成网络，首次实现零样本跨主体、跨任务的EEG视觉重建。在多个基准数据集上显著超越已有方法，推动了BCI与神经解码的发展。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-l3aedxjmhl/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1441, \"height\": 478, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-l3aedxjmhl/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1450, \"height\": 1000, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-l3aedxjmhl/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1443, \"height\": 663, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-l3aedxjmhl/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1436, \"height\": 1114, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-l3aedxjmhl/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1444, \"height\": 464, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-l3aedxjmhl/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1457, \"height\": 823, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-l3aedxjmhl/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1454, \"height\": 1190, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-l3aedxjmhl/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1458, \"height\": 1057, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-l3aedxjmhl/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1430, \"height\": 855, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-l3aedxjmhl/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1450, \"height\": 875, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-l3aedxjmhl/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1415, \"height\": 842, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-l3aedxjmhl/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1447, \"height\": 708, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-l3aedxjmhl/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1452, \"height\": 627, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-l3aedxjmhl/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1450, \"height\": 242, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-l3aedxjmhl/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1451, \"height\": 591, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-l3aedxjmhl/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1445, \"height\": 1359, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-l3aedxjmhl/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1447, \"height\": 1436, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-l3aedxjmhl/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1445, \"height\": 483, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-l3aedxjmhl/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1442, \"height\": 817, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-l3aedxjmhl/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1441, \"height\": 452, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-l3aedxjmhl/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1442, \"height\": 876, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-l3aedxjmhl/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1440, \"height\": 403, \"label\": \"Table\"}]"
motivation: EEG视觉重建面临跨主体泛化差和任务受限的问题。
method: 提出统一框架NEED，包含个体自适应模块、对比学习和生成网络，实现零样本跨主体和跨任务泛化。
result: 在多个EEG视觉重建数据集上取得了最先进性能，并展示了强大的泛化能力。
conclusion: 该方法为EEG神经解码提供了可行的跨主体解决方案。
---

## Abstract
Translating brain activity into meaningful visual content has long been recognized as a fundamental challenge in neuroscience and brain-computer interface research. Recent advances in EEG-based neural decoding have shown promise, yet two critical limitations remain in this area: poor generalization across subjects and constraints to specific visual tasks. We introduce NEED, the first unified framework achieving zero-shot cross-subject and cross-task generalization for EEG-based visual reconstruction. Our approach addresses three fundamental challenges: (1) cross-subject variability through an Individual Adaptation Module pretrained on multiple EEG datasets to normalize subject-specific patterns, (2) limited spatial resolution and complex temporal dynamics via a dual-pathway architecture capturing both low-level visual dynamics and high-level semantics, and (3) task specificity constraints through a unified inference mechanism adaptable to different visual domains. For video reconstruction, NEED achieves better performance than existing methods. Importantly, Our model maintains 93.7% of within-subject classification performance and 92.4% of visual reconstruction quality when generalizing to unseen subjects, while achieving an SSIM of 0.352 when transferring directly to static image reconstruction without fine-tuning, demonstrating how neural decoding can move beyond subject and task boundaries toward truly generalizable brain-computer interfaces.

---

## 论文详细总结（自动生成）

# NEED 论文详细中文总结

## 1. 核心问题与整体含义（研究动机和背景）

- **核心问题**：从脑电图（EEG）信号中重建视觉内容是脑机接口领域的关键挑战。当前方法面临两大瓶颈：（1）跨被试泛化能力差——模型在被试间迁移时性能急剧下降，原因是神经活动模式个体差异大（解剖、电极位置等）；（2）任务特异性限制——现有框架只能针对单一任务（如视频重建或图像重建），无法互相迁移，导致需要为每种视觉刺激类型单独训练。
- **整体含义**：作者提出 NEED（Neural Decoding with Enhanced Extensibility and Diversity），旨在实现**零样本跨被试和跨任务泛化**，使EEG解码真正走向通用可落地的脑机接口。这项突破对瘫痪患者交流、视觉知觉理解、神经科学基础研究等领域具有深远意义。

## 2. 方法论

### 2.1 核心思想
NEED 是一个统一的端到端框架，包含三个关键模块：
- **个体适应模块 (IAM)**：解决被试差异，通过在多数据集预训练将个体信号归一化到共享表征空间。
- **双路径架构**：并行处理低层视觉感知（感知理解模块 PU）和高层语义（语义理解模块 SU），弥补EEG空间分辨率低和时域复杂的不足。
- **统一推理机制**：通过任务自适应扩散模型，在同一框架内灵活生成视频或图像。

### 2.2 关键技术细节
1. **个体适应模块 IAM**：
   - 包含四级自适应：信号级、频谱级、时域级、语义级。
   - 使用可学习被试嵌入和数据集嵌入，通过多头部注意力（6头，d=256）和样式注入进行归一化。
   - 预训练损失：\( \mathcal{L}_{\text{pretrain}} = \alpha \mathcal{L}_{\text{recon}} + \beta \mathcal{L}_{\text{adv}} + \gamma D_{\text{KL}} \)，包含重构、对抗性被试解耦和KL散度项。

2. **双流 EEG 编码器 DSGNet**：
   - 空间流：利用球谐函数表示电极位置，通过图卷积网络建模电极间关系。
   - 时间流：应用 Riemann-Liouville 分数阶变换（α∈{0.2,0.4,0.6,0.8}）捕获多尺度时域动态，配合空洞卷积扩大感受野。
   - 跨流交叉注意力融合空间和时间表征，并采用多维掩码增强抗噪性。

3. **感知理解模块 PU**：
   - 包含动态特征提取器（DFE）和时空记忆增强循环网络（SMARN）。
   - 提取三大特征：运动（3D卷积）、空间（2D卷积）、时域（SMARN）。
   - 使用双向动态对比对齐（BDC）损失对齐EEG与视觉特征。

4. **语义理解模块 SU**：
   - 使用 CLIP-ViT-G/14 提取关键帧特征，通过层次语义对比损失（HSC）对齐。
   - 集成 BLIP-2 和 LLaMA-2-13B（LoRA微调）生成文本描述，通过跨模态语义对齐（CSA）引导扩散模型（SDXL unCLIP）。

5. **统一推理机制**：
   - 任务适配器根据任务类型（视频/图像）调整条件信号权重。
   - 多引导集成：关键帧控制、文本嵌入、动态模式、EEG特征。
   - 条件层调制：\( h_l = \gamma_l(\tau_t) \odot \text{Norm}(h_{l-1}) + \beta_l(\tau_t) \)，对不同任务自动调整特征变换。

### 2.3 算法流程（文字说明）
训练分三阶段：
1. IAM 在多数据集上预训练（SEED、DEAP、EEGEYENET），优化重构与对抗损失。
2. DSGNet 和 PU/SU 模块在 SEED-DV 上训练，分别使用 BDC 和 HSC 损失。
3. 统一推理机制在 SEED-DV 上微调，学习任务特定参数和条件权重。

推理时：对未见被试输入EEG → IAM归一化 → DSGNet编码 → PU/SU提取特征 → TaskAdapter根据任务类型调整 → 多引导条件生成 → 扩散模型去噪（50步，分类器引导7.5）得到重建视频或图像。

## 3. 实验设计

### 3.1 数据集与场景
- **SEED-DV**：20名被试观看1400个视频（40类），62通道1000Hz，作为视频重建主训练集。
- **THINGS-EEG**：10名被试观看22000张静图（1854类），64通道，用于零样本跨任务泛化评估。
- **IAM预训练**：SEED（情感视频）、DEAP（音乐视频，32通道）、EEGEYENET（多视觉任务，14通道便携设备），共约400+被试。
- **评估场景**：视频图像重建、跨被试泛化（训练1~19名被试，测试剩余）、跨任务泛化（视频→图像零样本）、脑区贡献、频带贡献、时域动态等。

### 3.2 Benchmark与对比方法
- **视频重建**：对比 EEG2video (EEG)、多种fMRI方法（Wang, Kupershmidt, MinD-Video, NeuroClips）、MEG方法（META-MEG）等。
- **图像重建**：对比 ATM-S、CognitionCapturer、Mind's Eye (fMRI) 等。
- **EEG分类**：对比 SVM(PSD/DE)、MLP、GLMNet、ShallowNet、DeepNet、EEGNet、TSCNet、Conformer、BraVL、EEGPT、TSConv、GLMNet 等12种基线。
- **指标**：语义（2-way/40-way分类准确率、CLIP相似度）、感知（SSIM、PSNR、PixCorr）、时域（FVD、CLIP-pcc）、结构（Edge-F1、Struct-sim、LPIPS）。

### 3.3 实验充分性
- **分类基准**（表1）：在7个视觉感知任务（40类/9类/二分类）上，DSGNet均显著优于所有基线（p<0.05），相对提升10%–101%。
- **视频重建**（表2）：全模型在语义准确率（0.898）和视觉保真度（SSIM 0.356）达到最优。
- **消融实验**（表2、表5、表6）：详细分析IAM、PU、SU、任务条件、动态模式、控制等各组件，以及DFE、SMARN、BDC子模块、各类LLM和视觉编码器替换。共约30+种配置。
- **跨被试泛化**（表7-11）：训练1/2/5/10/15/19名被试，测试剩余被试，报告每个设置下的性能保持率。还进行了单个被试迁移分析（表10）和组件消融（表11）。
- **额外分析**：脑区贡献（图6）、频带贡献（图9）、时域窗口动态（图11）、定性文本分析（图10）。所有实验均给出标准差或误差线，报告统计显著性。

## 4. 资源与算力

论文在 **Implementation Details** 中仅提到：
> “使用PyTorch，在NVIDIA A100 GPU上进行实验。”

未明确指出GPU数量、训练总时长、显存占用等具体数值。因此算力细节不充分，这是实验透明度的一个不足。

## 5. 实验数量与充分性

- **数量庞大**：包含 11 张表格（主表+附录）和 10+ 幅图表，涵盖分类、重建、泛化、消融、脑区/频带/时域分析。
- **充分性**：对比方法覆盖传统机器学习（SVM）和主流深度学习模型；消融实验从整体模块到子结构（SMARN vs LSTM/GRU/Transformer）均一一验证；跨被试泛化具有系统规模（1→19名被试）；跨任务零样本测试唯一。实验设计相对客观，采用标准化指标和多次重复，统计显著性明确。
- **潜在偏差**：主体实验仅在一个视频数据集（SEED-DV）和一个图像数据集（THINGS-EEG）上进行；虽然预训练涉及其他数据集，但重建任务本身泛化到更多EEG数据集（如自然视频）尚未验证。另外，失败案例分析（如复杂光照、高速运动）仅作定性展示，缺乏定量统计。

## 6. 主要结论与发现

- **跨被试泛化**：使用19名被试训练后，对未见被试保留93.7%分类性能和92.4%重建质量，性能随训练被试数量非线性增长（5→10→15名出现跃升）。
- **跨任务泛化**：视频→图像零样本转移 SSIM 达0.352，超过部分任务专门方法（如CognitionCapturer SSIM 0.150），任务条件移除后 SSIM 骤降至0.063，证明其关键性。
- **EEG编码器优势**：DSGNet在40类分类Top-1准确率14.23%，相对最佳基线提升101.8%；在二分类任务也保持10%左右提升。
- **脑区贡献**：枕叶-颞叶-顶叶联合最优，单一枕叶仅8.1%精度，全脑14.3%。频带分析显示Alpha带最重要（移除后降至8.46%）。
- **时序动态**：语义信息在1400ms左右达到峰值，600ms附近200ms窗口信息含量最高（对应P300/N400成分）。
- **双路径互补**：PU与SU均不可或缺，PU对低层细节和动态更重要，SU对语义更关键；IAM是泛化的核心组件。

## 7. 优点

1. **首次统一解决两大核心挑战**：同时实现跨被试和跨任务零样本泛化，而以前工作只能关注其中一方面。
2. **架构设计巧妙**：IAM的四级自适应机制、DSGNet的双流编码、PU/SU双路径理解，以及任务自适应扩散，各组件可解释性强且互补。
3. **预训练策略有效**：在多数据集（不同任务、不同通道数）上预训练IAM，提升鲁棒性和泛化能力。
4. **实验系统而详尽**：覆盖分类、重建、泛化、消融、脑区/频带/时域等多维度分析，消融实验深入到子模块和替换设置。
5. **跨任务零样本演示**：不使用任何细调直接完成THINGS-EEG图像重建，具有实用创新性。
6. **开源承诺**：论文声明将公开代码和模型，便于复现和后续研究。

## 8. 不足与局限

1. **重建质量仍有提升空间**：复杂光照、精细纹理、快速运动场景下结果较差（文中以红色失败案例展示），远未达到照片级真实感。
2. **对高密度EEG依赖**：主训练集SEED-DV为62通道；跨任务评估THINGS-EEG为64通道。论文虽然用EEGEYENET（14通道便携设备）预训练IAM，但并未直接在14通道数据上测试重建任务（EEGEYENET仅用于IAM预训练）。因此对于低密度/消费级设备，泛化能力未验证。
3. **计算资源与效率不透明**：缺少GPU数量、训练时长、模型参数量、推理速度等关键信息。LLM（LLaMA-2-13B）和扩散模型（SDXL unCLIP）的引入使得模型较重，实际部署可能受限。
4. **跨任务泛化仅单向测试**：只测试了视频→图像，未测试图像→视频；且仅在THINGS-EEG一个数据集上验证，缺乏更多任务（如类别无关、跨模态）评估。
5. **数据集相对局限**：视频训练集来自单个数据集SEED-DV（20名被试，特定40类），自然场景多样性有限。跨被试泛化也局限在同一数据集内（训练即SEED-DV内留出被试），未在全新数据集上验证。
6. **失败分析不够系统**：仅给出定性示例，未统计失败模式分布或极端情况下的性能下降率。

（完）
