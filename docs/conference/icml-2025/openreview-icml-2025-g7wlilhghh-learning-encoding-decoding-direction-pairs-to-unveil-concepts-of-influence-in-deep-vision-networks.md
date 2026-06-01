---
title: Learning Encoding-Decoding Direction Pairs to Unveil Concepts of Influence in Deep Vision Networks
title_zh: 学习编解码方向对以揭示深度视觉网络中的影响概念
authors: "Alexandros Doumanoglou, Kurt Driessens, Dimitrios Zarpalas"
date: 2025-01-23
pdf: "https://openreview.net/pdf?id=g7wLilhGhh"
tags: ["query:eeg-latent"]
score: 6.0
evidence: 潜空间编解码方向对
tldr: 该论文提出学习编解码方向对来揭示深度视觉网络中的概念，其中编码方向将潜在因子映射到特征分量，解码方向检索概念。这一潜空间分析方法不限于视觉，可迁移至EEG潜空间表示学习，用于理解EEG信号中的潜在特征，支持EEG缺失通道补全等任务。
source: ICML-2025-Rejected-Public
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-g7wlilhghh/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 826, \"height\": 371, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-g7wlilhghh/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 805, \"height\": 298, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-g7wlilhghh/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 798, \"height\": 640, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-g7wlilhghh/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1733, \"height\": 382, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-g7wlilhghh/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1799, \"height\": 1365, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-g7wlilhghh/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1781, \"height\": 1647, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-g7wlilhghh/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1732, \"height\": 1645, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-g7wlilhghh/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1165, \"height\": 591, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-g7wlilhghh/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1157, \"height\": 496, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-g7wlilhghh/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1161, \"height\": 492, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-g7wlilhghh/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1170, \"height\": 587, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-g7wlilhghh/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1158, \"height\": 496, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-g7wlilhghh/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1158, \"height\": 491, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-g7wlilhghh/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1166, \"height\": 590, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-g7wlilhghh/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1158, \"height\": 494, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-g7wlilhghh/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1160, \"height\": 492, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-g7wlilhghh/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1161, \"height\": 495, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-g7wlilhghh/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1871, \"height\": 1837, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-g7wlilhghh/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1877, \"height\": 1851, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-g7wlilhghh/fig-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1875, \"height\": 1281, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-g7wlilhghh/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 432, \"height\": 236, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-g7wlilhghh/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 863, \"height\": 337, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-g7wlilhghh/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1307, \"height\": 191, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-g7wlilhghh/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 792, \"height\": 305, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-g7wlilhghh/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 384, \"height\": 91, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-g7wlilhghh/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 639, \"height\": 611, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-g7wlilhghh/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 926, \"height\": 168, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-g7wlilhghh/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 584, \"height\": 235, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-g7wlilhghh/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1389, \"height\": 488, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-g7wlilhghh/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 899, \"height\": 237, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-g7wlilhghh/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 923, \"height\": 235, \"label\": \"Table\"}]"
motivation: 深度网络概念以叠加方式编码在特征空间方向中，但缺乏显式的编解码方向对。
method: 通过对比自编码器和字典学习，学习每个概念的编码方向和解码方向对。
result: 在多个视觉网络上成功提取了有意义的编解码方向，提升了可解释性。
conclusion: 编解码方向对提供了一种通用的潜空间概念解析工具，可应用于EEG等领域。
---

## Abstract
Latent space directions have played a key role in understanding, debugging, and improving deep learning models, since concepts are encoded in directions of the feature space as superpositions. The encoding direction of a concept maps a latent factor to a feature component, while the decoding direction retrieves it. These encoding-decoding direction pairs unlock significant potential to open the black-box nature of deep networks. Decoding directions help attribute meaning to latent codes, while encoding directions help assess the influence of the concept on the predictions, and both directions may assist in unlearning irrelevant concepts. Compared to previous autoencoder and dictionary learning approaches, we offer a different perspective in learning these direction pairs. We base the decoding direction on unsupervised interpretable basis learning and introduce signal vectors to estimate encoding directions. Meanwhile, we empirically prove that the uncertainty region of the model is informative and can be used to effectively reveal meaningful and influential concepts that impact model predictions. Tests on synthetic data show the approach's efficacy in recovering the underlying encoding-decoding direction pairs in a controlled setting, while experiments on state-of-the art deep image classifiers show notable improvements, or competitive performance, in interpretability and influence, compared to previous unsupervised and even supervised direction learning approaches.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 核心问题与整体含义（研究动机和背景）

- **研究动机**：深度神经网络（DNN）的特征空间中，概念以叠加方式编码在方向（directions）上。现有工作通常孤立地学习概念的解码方向（decoding direction，用于从特征中提取概念）或编码方向（encoding direction，用于评估概念对预测的影响），且大多未明确区分两者。这限制了它们在不同任务（如可解释性、影响评估、概念遗忘）中的适用性。
- **整体目标**：提出一种无监督方法，联合学习概念在潜空间中的编解码方向对（encoding-decoding direction pairs），同时揭示网络中具有影响力的概念。该方法不依赖特征重建或矩阵分解，而是基于可解释性基学习、信号向量估计以及不确定性区域对齐，以提升方向的可解释性和影响力。

## 2. 论文提出的方法论

- **核心思想**：
  - 将概念分解为编码方向（信号方向，signal direction）和解码方向（滤波器方向，filter direction）。解码方向通过内积提取潜在因子（信号值），编码方向映射潜在因子到特征分量。
  - 基于无监督可解释基学习（Doumanoglou et al., 2023）建模解码方向，引入信号向量（signal vectors）估计编码方向。
  - 利用网络的“不确定性区域”（uncertainty region）——即预测最不确定的子空间，将其与概念检测器的决策超平面交集区域对齐，从而引导出更有意义且对预测有显著影响的概念。

- **关键技术细节**：
  1. **多概念信号-干扰数据模型**（Section 4.1）：将特征表示表示为多个概念信号方向 S 和干扰方向 D 的线性组合，并假设每个空间位置的语义标签是稀疏的（仅有少量概念）。
  2. **可解释性损失**（Section 4.2）：
     - Self-Weighted Reduction (RSW)：一种自适应加权方法，近似实现最大操作，用于优化损失的上界。
     - 过分活跃分类器损失 (Leac)：惩罚过大的聚类，防止平凡解。
     - 稀疏性上界损失 (Lsb)：对每个像素的稀疏性损失取上界。
  3. **信号向量估计**（Section 4.3）：利用滤波器权重作为信号值的回归器，并优化滤波器-信号向量正交性损失 (Lfso)，确保解码方向只提取对应概念的信息。
  4. **不确定性区域对齐**（Section 4.4）：
     - 无约束对齐 (Luur)：通过伪逆计算将每个特征点移到所有分类器决策超平面交集处。
     - 约束对齐 (Lcur)：限制移动方向在信号向量张成的子空间内，以防止特征偏离概念编码流形。
     - 两者均最大化移动后特征在网络输出上的熵（不确定性），从而对齐模型的不确定性区域与概念检测器的不确定性区域。
  - **学习流程**（Appendix D）：分四步：a) 使用 Luur 初始化解码方向；b) 去除正交性等约束，加入可解释性损失；c) 用滤波器初始化信号向量；d) 联合优化所有参数，加入 Lcur 和 Lfso。

## 3. 实验设计

- **数据集/场景**：
  - **合成数据**：生成 D=16, I=3 概念，F=2 干扰，三类图像（基于不同概念组合），训练一个两层网络并达到99%准确率。
  - **真实图像分类器**：
    - ResNet18 在 Places365 上训练，使用 Broden 数据集进行概念标签和评估。
    - ResNet50 在 Moments in Time (MiT) 上训练，使用 Broden Action 数据集。
  - **玩具实验**：Chess Pieces 数据集，清洁/投毒（添加水印）场景，用于证明模型纠正能力。

- **Benchmark**（对比方法）：
  - **解码方向（可解释性）对比**：与无监督方法 UIBE (Doumanoglou et al., 2023)、CBE (Doumanoglou et al., 2024) 比较 S1/S2 分数。与有监督 IBD (Zhou et al., 2018) 比较精确率、召回率等。
  - **编码方向（影响力）对比**：与有监督 Pattern-CAVs (Pahde et al., 2024) 比较 RCAV 敏感性分数。
  - **合成数据**：与稀疏自编码器 (Bricken et al., 2023)、Pattern-CAVs 比较余弦相似度。
  - **消融实验**：逐步加入 Lsb, Leac, Lfso, Lcur 等损失，观察对 S1, S2, SDC, SCDP 的影响。

## 4. 资源与算力

- **文中未明确说明 GPU 型号、数量、总训练时长等具体信息**。仅提及参考批量大小为4096，当改变批量时按比例缩放学习率。步骤 (a) 800 轮，(b) 2000 轮，(d) 2000 轮，且启用了学习率衰减（k 0.5, patience 10/50）。未给出具体硬件的性能指标。

## 5. 实验数量与充分性

- **实验组数**：
  - 合成数据：1 组（恢复编解码方向、IoU、RMSE、余弦相似度对比）。
  - 真实图像分类器：
    - 消融研究（表2）：包含多组配置（共 8 行）。
    - 与无监督方法对比（表5）：在两组模型（ResNet18/Places365, ResNet50/MiT）上报告 S1, S2。
    - 与有监督方法对比（表3, 表4, 图4-7）。
  - 玩具实验（Chess Pieces）：1 组（显示模型纠正效果，表10）。
  - 附录中还包括更多定性分割图（图12-13）和影响图（图8-11）。
- **充分性**：实验覆盖了合成验证、真实图像分类、模型错误纠正，并进行了全面的消融和对标。但仅在两种主流网络结构和两个数据集上进行可解释性评估，规模相对有限。此外，没有在更现代的模型（如 Vision Transformer）上测试。整体上实验设计较为客观，消融充分，对比基线包括有监督和无监督方法。

## 6. 主要结论与发现

- 所提出的方法能够无监督地学习到与真实概念对应的编解码方向对，在合成数据上准确恢复（IoU>0.92，信号向量余弦相似度远高于 Pattern-CAVs 和稀疏自编码器）。
- 不确定性区域对齐 (Luur/Lcur) 显著提高了概念的可解释性和影响力，相比先前工作 (UIBE/CBE) 在 S1/S2 上提升可达 22.56%（表5）。
- 信号向量比 Pattern-CAVs 更能揭示网络对概念的敏感性（S3<0.5，表4），表明信号向量是对编码方向的更好估计。
- 在可解释性方面，所提方法达到与有监督方法相当的精度，但召回率较低（因稀疏性目标）；组合具有相同标签的检测器可提升召回率。
- 玩具实验验证了该方法可用于模型纠正：通过抑制水印信号方向有效去除网络对虚假特征的依赖，准确率从34%提升至69%（表10）。

## 7. 优点

- **方法创新**：首次联合无监督学习编码和解码方向对，区分了两种方向的用途，并基于不确定性区域对齐进行引导，形成系统化的框架。
- **理论严谨**：扩展了信号-干扰数据模型至多概念场景，并推导了信号值的提取公式（Appendix C）。
- **实验全面**：包含合成数据、真实图像分类和模型纠正等多种场景，消融研究充分，对比基线涵盖有监督和无监督。
- **实用性**：无需概念标注，可应用于发现模型偏见（如水印问题）并辅助模型修正。
- **可迁移性**：虽然应用于视觉，但方法论依赖潜空间方向，可迁移到其他模态（如 EEG）的潜空间表示学习。

## 8. 不足与局限

- **实验规模有限**：仅在 ResNet18/50 两类网络上评估，未在更大模型（如 ViT）或更多数据集上测试，泛化性有待验证。
- **没有报告计算资源**：缺乏 GPU 型号、训练时间等具体信息，不利于复现和比较效率。
- **可解释性召回率低**：受稀疏性限制，单个检测器召回率低，需要后处理（如 OR 组合）提升。
- **超参数依赖**：方法涉及多个损失权重和超参数（如 ρ, τ, γ, ν, κ），调优成本较高，文中未提供充分的灵敏度分析。
- **未处理时序/序列数据**：目前仅适用于图像卷积特征，扩展到序列模型（如 Transformer, LSTM）需要额外处理。
- **不确定性对齐假设的局限性**：假设网络在概念不确定时预测也困惑，这一假设在复杂任务中未必始终成立（例如存在高度非线性决策边界）。
- **缺少与其他无监督方法（如 NMF, PCA）的可解释性定量对比**：文中指出这些方法因缺少分类规则而无法直接评估，但未设计替代评估方案。

（完）
