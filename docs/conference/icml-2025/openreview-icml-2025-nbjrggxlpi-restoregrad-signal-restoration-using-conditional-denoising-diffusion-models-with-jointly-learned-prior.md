---
title: "RestoreGrad: Signal Restoration Using Conditional Denoising Diffusion Models with Jointly Learned Prior"
title_zh: RestoreGrad：基于联合学习先验的条件去噪扩散模型信号恢复
authors: "Ching-Hua Lee, Chouchang Yang, Jaejin Cho, Yashas Malur Saidutta, Rakshith Sharma Srinivasa, Yilin Shen, Hongxia Jin"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=NbjrGgxLPi"
tags: ["query:eeg-latent"]
score: 8.0
evidence: 带联合学习先验的条件扩散模型用于信号恢复，可应用于EEG重建
tldr: 本文提出RestoreGrad，改进条件去噪扩散概率模型（DDPM）用于信号恢复。现有方法使用标准高斯先验，丢弃了退化信号中的有用信息。RestoreGrad联合学习一个更具信息量的先验，显著提升了信号恢复质量。该方法可应用于EEG信号重建与缺失通道补全。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-nbjrggxlpi/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 846, \"height\": 472, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nbjrggxlpi/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 846, \"height\": 796, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nbjrggxlpi/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 851, \"height\": 260, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nbjrggxlpi/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1759, \"height\": 426, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nbjrggxlpi/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 851, \"height\": 315, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nbjrggxlpi/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 691, \"height\": 388, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nbjrggxlpi/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1771, \"height\": 536, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nbjrggxlpi/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1511, \"height\": 424, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nbjrggxlpi/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1517, \"height\": 383, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nbjrggxlpi/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1599, \"height\": 515, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nbjrggxlpi/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1412, \"height\": 1442, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nbjrggxlpi/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1246, \"height\": 921, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nbjrggxlpi/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1726, \"height\": 2021, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nbjrggxlpi/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1610, \"height\": 733, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nbjrggxlpi/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1776, \"height\": 483, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nbjrggxlpi/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1778, \"height\": 485, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nbjrggxlpi/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1769, \"height\": 801, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nbjrggxlpi/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1773, \"height\": 486, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nbjrggxlpi/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1777, \"height\": 487, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nbjrggxlpi/fig-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1777, \"height\": 681, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nbjrggxlpi/fig-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 1771, \"height\": 693, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-nbjrggxlpi/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 862, \"height\": 227, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nbjrggxlpi/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 862, \"height\": 172, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nbjrggxlpi/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 846, \"height\": 268, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nbjrggxlpi/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1771, \"height\": 371, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nbjrggxlpi/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 860, \"height\": 222, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nbjrggxlpi/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 860, \"height\": 268, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nbjrggxlpi/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1599, \"height\": 240, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nbjrggxlpi/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 901, \"height\": 337, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nbjrggxlpi/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1288, \"height\": 314, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nbjrggxlpi/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1070, \"height\": 427, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nbjrggxlpi/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1168, \"height\": 498, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nbjrggxlpi/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 898, \"height\": 180, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nbjrggxlpi/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1250, \"height\": 287, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nbjrggxlpi/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1241, \"height\": 199, \"label\": \"Table\"}]"
motivation: 标准高斯先验丢弃了退化信号中的有用信息。
method: 联合学习一个信息更丰富的先验来改进条件DDPM。
result: 信号恢复性能显著提升。
conclusion: 为信号恢复提供了一种更强先验的生成框架。
---

## Abstract
Denoising diffusion probabilistic models (DDPMs) can be utilized to recover a clean signal from its degraded observation(s) by conditioning the model on the degraded signal. The degraded signals are themselves contaminated versions of the clean signals; due to this correlation, they may encompass certain useful information about the target clean data distribution. However, existing adoption of the standard Gaussian as the prior distribution in turn discards such information when shaping the prior, resulting in sub-optimal performance. In this paper, we propose to improve conditional DDPMs for signal restoration by leveraging a more informative prior that is jointly learned with the diffusion model. The proposed framework, called RestoreGrad, seamlessly integrates DDPMs into the variational autoencoder (VAE) framework, taking advantage of the correlation between the degraded and clean signals to encode a better diffusion prior. On speech and image restoration tasks, we show that RestoreGrad demonstrates faster convergence (5-10 times fewer training steps) to achieve better quality of restored signals over existing DDPM baselines and improved robustness to using fewer sampling steps in inference time (2-2.5 times fewer), advocating the advantages of leveraging jointly learned prior for efficiency improvements in the diffusion process.

---

## 论文详细总结（自动生成）

# RestoreGrad：基于联合学习先验的条件去噪扩散模型信号恢复——中文总结

## 1. 核心问题与整体含义（研究动机和背景）
- **研究动机**：去噪扩散概率模型（DDPM）在信号恢复（如语音增强、图像恢复）中通常采用**标准高斯分布**作为先验分布。然而在信号恢复任务中，退化信号（如带噪语音、下雨图像）是干净信号的“污染版本”，两者之间存在强烈相关性，标准高斯先验完全抛弃了退化信号中蕴含的关于目标干净数据分布的有用信息，导致模型训练效率低下（收敛慢）且生成质量受限。
- **整体含义**：本文提出**联合学习一个更信息化的先验分布**来替代标准高斯先验，从而提升条件DDPM在信号恢复任务中的训练和推理效率。核心思想是利用退化信号与干净信号之间的相关性，通过一个可学习的先验编码器从退化信号中提取关于目标数据分布的结构化信息，使扩散过程能更快、更准确地逼近真实数据分布。

## 2. 方法论：核心思想、关键技术细节
- **核心思想**：将条件DDPM无缝集成到变分自编码器（VAE）框架中，通过引入一个**先验编码器 \(\psi\)** 和一个**后验编码器 \(\phi\)**，联合学习扩散过程的噪声先验分布。后验编码器在训练阶段利用干净信号 \(x_0\) 和退化信号 \(y\) 提供的信息来指导先验的学习；推理阶段仅使用先验编码器从退化信号 \(y\) 估计先验分布，从而生成更高质量的信号。
- **关键技术细节**：
    1. **概率建模**：假设先验和后验均为零均值高斯分布，即  
       \(p_\psi(\epsilon|y) = \mathcal{N}(\epsilon; 0, \Sigma_{\text{prior}}(y;\psi))\)，  
       \(q_\phi(\epsilon|x_0,y) = \mathcal{N}(\epsilon; 0, \Sigma_{\text{post}}(x_0,y;\phi))\)，  
       其中协方差由轻量级ResNet-20网络估计。
    2. **ELBO推导**：推导了一个新的证据下界（ELBO），将条件DDPM的损失与VAE的先验匹配项相结合，形成联合训练目标（式10/11）。
    3. **损失函数**（简化版）：
       - **潜在正则化项** \(L_{\text{LR}}\)：约束后验协方差避免过大。
       - **去噪匹配项** \(L_{\text{DM}}\)：训练DDPM预测噪声（加权范数为 \(\|\cdot\|^2_{\Sigma^{-1}_{\text{post}}}\)）。
       - **先验匹配项** \(L_{\text{PM}}\)：KL散度形式，对齐先验和后验分布。
       - 超参数 \(\eta\) 控制正则化强度，\(\lambda\) 控制先验匹配权重。
    4. **端到端训练**：通过重参数化技巧采样 \(\epsilon \sim q_\phi\)，联合优化 \(\theta, \psi, \phi\)。
    5. **推理**：仅需先验编码器 \(\psi\) 和DDPM \(\theta\)，后验编码器不再使用。

## 3. 实验设计
- **数据集与场景**：
  - **语音增强（SE）**：VoiceBank+DEMAND（16kHz波形，11,572训练/824测试）。评估指标：PESQ、SI-SNR、SSNR、CSIG、CBAK、COVL。
  - **图像恢复（IR）**：RainDrop（861训练/58测试）、AllWeather（18,069训练，含Snow100K、Outdoor-Rain、RainDrop子集）。评估指标：PSNR、SSIM、LPIPS、FID。
  - **泛化测试**：真实数据集RainDS-Real、Snow100K-Real（NIQE），OOD数据CHiME-3（SE）。
- **基准方法对比**：
  - SE：基线CDiffuSE（标准高斯先验）、PriorGrad（手工设计数据相关先验）。
  - IR：RainDropDiff、WeatherDiff（标准高斯先验）；对比最新模型DTPM、RDDM等。
  - 消融：是否使用后验编码器、不同\(\eta\)与\(\lambda\)、不同编码器大小、不同推理步数。
- **实验充分性**：在语音和图像两个模态上进行验证，覆盖合成数据、真实数据、OOD数据；包含多种度量指标和多个SOTA对比；进行了丰富的消融和超参数分析。

## 4. 资源与算力
- **SE实验**：1块NVIDIA Tesla V100 32GB GPU，训练96 epoch约1天。
- **IR实验**：2块NVIDIA Tesla V100 32GB GPU：RainDrop训练9,261 epoch约12天；AllWeather训练887 epoch约21天；其他任务（去模糊、超分辨）训练数天至数周。
- **编码器复杂度**：SE中编码器（93K参数）仅占DDPM（4.28M）的2.2%延时和10.3%内存；IR中编码器（0.27M）占DDPM（82-110M）的<1.3%延时和<30%内存。

## 5. 实验数量与充分性
- **实验数量**：论文包含14张表格和21张图，涵盖：
  - 3个主要任务（SE, IR on RainDrop, IR on AllWeather）+ 2个扩展任务（去模糊、超分辨）
  - 3类对比（标准DDPM、PriorGrad、其他SOTA）
  - 4种消融（后验有无、编码器大小、\(\eta/\lambda\)参数、推理步数）
  - 2项泛化测试（NIQE真实图像、CHiME-3 OOD语音）
- **充分性与公平性**：
  - 对比方法采用作者公开的基线代码或报告结果，训练配置保持一致。
  - 所有模型在相同epoch或推理步数下比较，并报告多次采样的均值±标准差。
  - 消融实验系统性地探讨了关键超参数和组件的影响。
  - 局限：部分对比使用了其他论文报告的固定结果（非复现），但总体公平。

## 6. 主要结论与发现
- **训练效率大幅提升**：RestoreGrad在SE和IR任务中达到同等性能所需的训练步数仅为标准DDPM的1/5~1/10（例如PESQ 2.4时约10 epoch vs 96 epoch）。
- **推理鲁棒性更强**：将推理步数从6降至3（SE）或从25降至10（IR），性能几乎不降，而基线DDPM显著退化。
- **生成质量更优**：在SE所有指标上超越CDiffuSE和PriorGrad；在IR的多天气模型上超越WeatherDiff，且在与专用模型对比中达到同等水平。
- **后验编码器有效**：移除后验编码器后性能下降甚至训练发散，验证了利用干净信号信息指导先验学习的重要性。
- **泛化能力良好**：在真实图像和OOD语音上保持竞争力，未牺牲生成模型的泛化性。

## 7. 优点
- **方法创新**：首次将DDPM与VAE框架融合，通过联合学习先验解决标准高斯先验丢弃信息的问题，是学习和推理两阶段的高效统一。
- **轻量高效**：编码器网络极小（参数<0.3% DDPM），额外计算开销可忽略，但带来显著的收敛加速和质量提升。
- **通用性强**：成功应用于语音和图像两种完全不同模态的信号恢复任务，且可扩展到去模糊、超分辨等多种图像恢复场景。
- **理论坚实**：推导了新的ELBO，并给出清晰的训练和推理算法伪代码。
- **实验全面**：覆盖合成/真实数据、域内/OOD场景、多类指标、多组消融，结论可靠。

## 8. 不足与局限
- **先验形式有限**：仅假设零均值高斯分布并学习协方差，未考虑更一般的先验形式（如混合高斯、非高斯分布），可能限制其对更复杂数据分布的建模能力。
- **应用范围**：本文专注于信号恢复任务（退化信号与干净信号具有强相关性），在其他类型条件生成任务（如文本到图像）中的有效性尚待验证。
- **计算资源**：IR任务训练时间仍较长（尤其AllWeather 21天），虽然比基线更快，但对大规模部署仍有一定门槛。
- **消融覆盖**：对于超参数 \(\eta, \lambda\) 的联动影响仅进行了部分组合实验，全面的网格搜索未展示；不同编码器大小的最优配置也未深入探讨。
- **对比公平性**：部分SOTA结果引自原论文（如DTPM、RDDM），可能存在训练配置或数据预处理差异带来的偏差。自身复现的PriorGrad在SE上可能与原始实现略有不同。
- **无理论保证**：虽然证明了ELBO，但未提供收敛性分析或最优性界限，多为实证结果。

（完）
