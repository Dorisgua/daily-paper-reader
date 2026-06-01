---
title: Human-Aligned Image Models Improve Visual Decoding from the Brain
title_zh: 人类对齐的图像模型改善脑视觉解码
authors: "Nona Rajabi, Antonio H. Ribeiro, Miguel Vasco, Farzaneh Taleb, Mårten Björkman, Danica Kragic"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=i6uxIAAMje"
tags: ["query:eeg"]
score: 4.0
evidence: 从脑活动解码视觉图像用于脑机接口
tldr: "本文针对脑活动视觉解码任务，引入与人类感知对齐的图像编码器，更有效地捕捉快速视觉刺激中的感知属性。实验表明，该方法将图像检索准确率相比现有最优技术提升高达21%，为脑机接口中的视觉解码提供了新方向。"
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-i6uxiaamje/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 792, \"height\": 745, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-i6uxiaamje/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1696, \"height\": 763, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-i6uxiaamje/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1732, \"height\": 696, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-i6uxiaamje/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1651, \"height\": 1281, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-i6uxiaamje/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1766, \"height\": 684, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-i6uxiaamje/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1744, \"height\": 2077, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-i6uxiaamje/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1745, \"height\": 1646, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-i6uxiaamje/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1410, \"height\": 1998, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-i6uxiaamje/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1410, \"height\": 2006, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-i6uxiaamje/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1410, \"height\": 2012, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-i6uxiaamje/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1411, \"height\": 2006, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-i6uxiaamje/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1408, \"height\": 2009, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-i6uxiaamje/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1410, \"height\": 2013, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-i6uxiaamje/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1400, \"height\": 2012, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-i6uxiaamje/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1399, \"height\": 2017, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-i6uxiaamje/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1401, \"height\": 2013, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-i6uxiaamje/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1408, \"height\": 2013, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-i6uxiaamje/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1401, \"height\": 2010, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-i6uxiaamje/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1400, \"height\": 2013, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-i6uxiaamje/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1773, \"height\": 191, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-i6uxiaamje/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1775, \"height\": 423, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-i6uxiaamje/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1775, \"height\": 252, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-i6uxiaamje/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1729, \"height\": 579, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-i6uxiaamje/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 699, \"height\": 325, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-i6uxiaamje/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1776, \"height\": 464, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-i6uxiaamje/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1772, \"height\": 273, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-i6uxiaamje/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1771, \"height\": 273, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-i6uxiaamje/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1773, \"height\": 271, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-i6uxiaamje/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1772, \"height\": 160, \"label\": \"Table\"}]"
motivation: 现有脑活动到图像的解码方法未能充分利用与人类感知对齐的表征。
method: 采用人类对齐的图像编码器将脑信号映射到图像空间，替代传统对齐策略。
result: "在多个数据集上图像检索准确率提升高达21%。"
conclusion: 人类对齐的图像编码器能更有效地捕捉脑信号中的感知信息，提升解码性能。
---

## Abstract
Decoding visual images from brain activity has significant potential for advancing brain-computer interaction and enhancing the understanding of human perception. Recent approaches align the representation spaces of images and brain activity to enable visual decoding. In this paper, we introduce the use of human-aligned image encoders to map brain signals to images. We hypothesize that these models more effectively capture perceptual attributes associated with the rapid visual stimuli presentations commonly used in visual brain data recording experiments. Our empirical results support this hypothesis, demonstrating that this simple modification improves image retrieval accuracy by up to 21\% compared to state-of-the-art methods. Comprehensive experiments confirm consistent performance improvements across diverse EEG architectures, image encoders, alignment methods, participants, and brain imaging modalities.

---

## 论文详细总结（自动生成）

## 1. 核心问题与整体含义（研究动机和背景）

- **核心问题**：从脑信号（如EEG、MEG、fMRI）解码视觉图像是脑机接口和认知科学的重要课题，但现有方法采用通用图像编码器（如CLIP、DINO）将脑信号映射到图像表示空间，性能有限（例如EEG-based方法在200图检索中top-1仅约28%）。
- **研究动机**：作者假设**人类对齐的图像模型**（即经过人类相似性判断微调的编码器）能更准确地捕捉快速视觉刺激（如100ms呈现）引发的早期感知属性（形状、颜色、纹理等），从而显著提升解码性能。

## 2. 方法论：核心思想、关键技术细节、公式或算法流程

- **核心思想**：用**人类对齐图像编码器**（如Dreamsim）替代标准预训练编码器，作为固定特征提取器；再通过对比学习训练脑信号编码器，使脑嵌入与图像嵌入在共享空间中对齐。
- **技术细节**：
  - 两个网络：图像编码器 \( f_\theta \)（冻结）、脑信号编码器 \( g_\phi \)（可训练）。
  - 输出嵌入 \( v \in \mathbb{R}^d \)（图像）、\( w \in \mathbb{R}^d \)（脑信号）。
  - 使用多模态InfoNCE损失对齐：
    \[
    \mathcal{L}_C = -\frac{1}{N} \sum_{i=1}^N \left[ \log \frac{\exp(\text{sim}(w_i,v_i)/\tau)}{\sum_{j} \exp(\text{sim}(w_i,v_j)/\tau)} + \log \frac{\exp(\text{sim}(v_i,w_i)/\tau)}{\sum_{j} \exp(\text{sim}(v_i,w_j)/\tau)} \right]
    \]
    其中 \(\text{sim}\) 为余弦相似度，\(\tau\) 为温度参数。
- **训练流程**：
  1. 预计算所有图像嵌入（使用冻结的原始/对齐编码器）。
  2. 输入脑信号（EEG/MEG/fMRI）到脑编码器，得到脑嵌入。
  3. 最小化InfoNCE损失，使匹配的（脑，图像）对嵌入更接近。
  4. 测试时，将测试脑嵌入与所有测试图像嵌入（200张）计算相似度，排序后取top-k。

## 3. 实验设计：数据集、Benchmark、对比方法

- **数据集**：
  - **THINGS-EEG2**（Gifford et al., 2022）：10位被试，EEG记录（100ms快速呈现），训练1654概念×10图片×4重复，测试200概念×1图片×80重复（重复平均后训练16540/测试200样本/被试）。
  - **THINGS-MEG2**（Hebart et al., 2023）：4位被试，MEG记录（500ms呈现），训练1854概念×12重复，测试200概念×12重复（平均后200测试样本/被试）。
  - **NSD fMRI**（Allen et al., 2022）：4位被试（1,2,5,7），7T fMRI，MS-COCO图像，训练24980样本，测试982样本（1000-way检索）。
- **Benchmark**：200-way（或1000-way）图像检索任务，评估top-1和top-5准确率。
- **对比方法**：
  - **图像编码器**：CLIP、OpenCLIP、DINO、DINOv2、SynCLR、Ensemble（六种基础编码器）及其**人类对齐版本**（Dreamsim、gLocal、Harmonization）。
  - **脑编码器**：NICE、EEGNetV4、EEGConformer、ATM-S（四种EEG架构）。
  - **对齐方法**：Dreamsim（主要使用）、gLocal、Harmonization（三种人类对齐方法）。
  - **额外对比**：跨被试泛化（9训1测）、跨模态（EEG→MEG→fMRI）、可解释性分析。

## 4. 资源与算力

**未明确说明**具体的GPU型号、数量、训练时长。仅提及计算资源来自“Knut and Alice Wallenberg Foundation’s Berzelius resource at the National Supercomputer Centre”以及“NAISS”。文中未提供各实验的具体训练时间或GPU数量。

## 5. 实验数量与充分性

- **实验数量**：
  - 主要实验（图3/表1）：对比6种图像编码器 × 4种脑编码器 × 3种对齐方法（部分组合），共数十组。
  - 跨被试实验（表2）：10位被试的跨被试泛化测试（每种编码器各5种子）。
  - 跨模态验证（表3）：MEG上4位被试结果。
  - fMRI验证（附录E）：4位被试的1000-way检索。
  - 可解释性分析（Grad-CAM）：时域、频域、空间分析，覆盖多个被试和编码器。
  - 消融/扩展：更大图像库检索（表10）、不同对齐方法（gLocal、Harmonization）对比。
- **充分性与公平性**：
  - 所有结果平均5个随机种子（不同拆分），提供标准差，统计分析（配对t检验）。
  - 对比条件一致（相同脑编码器、超参数、训练流程）。
  - 实验覆盖多种模态、架构、被试，结论稳健。

## 6. 论文的主要结论与发现

1. **人类对齐图像模型（特别是Dreamsim）显著提升脑到图像检索性能**，top-1准确率提升最高达21%（例如NICE+SynCLR: HA 58.44% vs Base 44.19%）。
2. **提升跨多种因素稳健**：不同图像编码器、脑编码器、对齐方法、被试、模态（EEG、MEG、fMRI）均观察到一致改善。
3. **可解释性分析表明**：对齐模型更关注早期视觉响应（0-200ms）和Alpha/Beta/Gamma频段，与视觉处理相关；而原始模型更集中于低频Delta。
4. **Dreamsim优于gLocal和Harmonization**，归因于其训练数据集（NIGHTS）强调中层次感知属性（颜色、形状、纹理），与RSVP范式下的脑信号更匹配。

## 7. 优点

- **方法简单有效**：仅替换图像编码器为其人类对齐版本，无需改动训练流程或模型结构，即带来显著提升。
- **实验全面系统**：涵盖多种图像编码器、脑编码器、对齐方法、模态、被试，并进行了统计检验和可解释性分析。
- **开源代码**：提供完整代码仓库，便于复现与扩展。
- **深刻洞察**：通过Grad-CAM分析揭示了人类对齐模型与脑信号早期视觉处理的关联，为视觉解码领域提供了新视角。

## 8. 不足与局限

- **任务单一**：仅评估图像检索任务，未涉及图像重建（如使用Stable Diffusion），后者是应用更广的脑解码形式。
- **跨被试泛化有限**：仅在CLIP和OpenCLIP上观察到显著提升，其他编码器的跨被试泛化收益不显著，方法尚未解决个体差异问题。
- **依赖特定人类对齐数据集**：Dreamsim高收益依赖NIGHTS数据集（聚焦中层次感知），其他对齐方法（gLocal、Harmonization）效果不佳，表明结果与数据集选择紧密相关。
- **计算资源未详述**：缺乏GPU型号、训练耗时等具体信息，不利于复现评估。
- **数据局限**：仅使用THINGS系列和NSD数据集，图像分布较为特定，泛化到其他图像数据库未见验证。
- **应用边界**：当前模型仅适用于实验室快速呈现的视觉刺激范式，对自然观看或长时间注视的场景适用性未知。

（完）
