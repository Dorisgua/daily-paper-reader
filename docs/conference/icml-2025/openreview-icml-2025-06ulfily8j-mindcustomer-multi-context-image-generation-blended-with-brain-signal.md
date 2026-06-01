---
title: "MindCustomer: Multi-Context Image Generation Blended with Brain Signal"
title_zh: MindCustomer：多上下文图像生成与脑信号融合
authors: "Muzhou Yu, Shuyun Lin, Lei Ma, Bo Lei, Kaisheng Ma"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=06UlFIly8J"
tags: ["query:eeg"]
score: 4.0
evidence: 脑信号生成，与脑机接口相关
tldr: 本文针对脑信号在图像生成中的应用挑战，提出MindCustomer框架，通过共享神经数据增强和跨模态融合管道，将视觉脑信号融入多上下文图像生成。实验表明该方法能有效融合图像和脑语义，生成定制化图像，为脑机接口应用提供了新思路。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-06ulfily8j/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1756, \"height\": 1053, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-06ulfily8j/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1712, \"height\": 849, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-06ulfily8j/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 829, \"height\": 790, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-06ulfily8j/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 816, \"height\": 764, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-06ulfily8j/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1686, \"height\": 574, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-06ulfily8j/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1753, \"height\": 715, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-06ulfily8j/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1747, \"height\": 637, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-06ulfily8j/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 834, \"height\": 966, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-06ulfily8j/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1718, \"height\": 496, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-06ulfily8j/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 800, \"height\": 632, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-06ulfily8j/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1682, \"height\": 1857, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-06ulfily8j/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1676, \"height\": 1549, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-06ulfily8j/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1695, \"height\": 1142, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-06ulfily8j/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1713, \"height\": 809, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-06ulfily8j/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1690, \"height\": 1455, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-06ulfily8j/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1708, \"height\": 921, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-06ulfily8j/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1700, \"height\": 2112, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-06ulfily8j/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1497, \"height\": 634, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-06ulfily8j/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1417, \"height\": 1271, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-06ulfily8j/fig-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1715, \"height\": 1454, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-06ulfily8j/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 629, \"height\": 194, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-06ulfily8j/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 513, \"height\": 165, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-06ulfily8j/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 491, \"height\": 240, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-06ulfily8j/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 843, \"height\": 180, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-06ulfily8j/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1622, \"height\": 254, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-06ulfily8j/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1418, \"height\": 181, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-06ulfily8j/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1417, \"height\": 264, \"label\": \"Table\"}]"
motivation: 脑信号直接反映用户意图，但现有方法在脑信号解释和跨模态融合上存在挑战。
method: 设计Image-Brain Translator实现跨主体脑嵌入，并提出无掩码跨模态信息融合管道。
result: 成功实现了基于脑信号的图像生成，验证了方法的有效性。
conclusion: MindCustomer为脑信号驱动的图像生成提供了可行方案，拓展了脑机接口在创意领域的应用。
---

## Abstract
Advancements in generative models have promoted text- and image-based multi-context image generation. Brain signals, offering a direct representation of user intent, present new opportunities for image customization. However, it faces challenges in brain interpretation, cross-modal context fusion and retention. In this paper, we present MindCustomer to explore the blending of visual brain signals in multi-context image generation. We first design shared neural data augmentation for stable cross-subject brain embedding by introducing the Image-Brain Translator (IBT) to generate brain responses from visual images. Then, we propose an effective cross-modal information fusion pipeline that mask-freely adapts distinct semantics from image and brain contexts within a diffusion model. It resolves semantic conflicts for context preservation and enables harmonious context integration. During the fusion pipeline, we further utilize the IBT to transfer image context to the brain representation to mitigate the cross-modal disparity. MindCustomer enables cross-subject generation, delivering unified, high-quality, and natural image outputs. Moreover, it exhibits strong generalization for new subjects via few-shot learning, indicating the potential for practical application. As the first work for multi-context blending with brain signal, MindCustomer lays a foundational exploration and inspiration for future brain-controlled generative technologies.

---

## 论文详细总结（自动生成）

# 论文总结：MindCustomer：多上下文图像生成与脑信号融合

## 1. 核心问题与整体含义（研究动机和背景）

- **研究动机**：现有文本/图像驱动的多上下文图像生成模型（如DreamBooth、Custom Diffusion）已取得显著进展，但依赖用户显式提供文本或图像提示。脑信号（如fMRI）能够直接反映用户意图，为图像定制提供全新途径。然而，脑信号在图像生成中面临三大挑战：①跨主体脑编码（不同个体的脑信号不一致且数据稀缺）；②多模态融合（图像、文本、脑信号隐含表示难以协调）；③多上下文保持（融合时防止某一上下文语义丢失或被干扰）。
- **整体含义**：本文首次探索将脑信号作为语义模态融入多上下文图像生成，提出了MindCustomer框架，旨在实现跨主体、无掩码、单张图像输入的脑控定制化生成，为脑机接口与生成式AI的结合奠定基础。

## 2. 方法论

### 核心思想
MindCustomer基于扩散模型（Versatile Diffusion, VD）实现多模态条件生成。核心思想是：先通过Image-Brain Translator (IBT)对脑数据进行跨主体增强和语义对齐，再通过分阶段微调（先基于图像上下文微调扩散模型，再轻量优化脑嵌入）实现跨模态和谐融合。

### 关键技术细节（按四阶段描述）
1. **脑表示预训练（Brain Representation Pre-training）**：
   - **IBT（Image-Brain Translator）**：用简单的3层MLP，以图像CLIP嵌入为输入，预测对应的fMRI体素（固定大小为8192）。用MSE损失训练，生成的虚假fMRI用于数据增强。
   - **跨主体脑嵌入器**：由浅层主体特定嵌入器（Subject-wise Embedder）和深层共享嵌入器（Shared Embedder）组成。将真实fMRI和IBT生成的虚假fMRI一起输入，使用SoftCLIP损失和MSE损失对齐到CLIP图像/文本空间。
   - **语义提取器（Semantic Extractor）**：引入ClipCap mapper作为监督，学习从脑嵌入中提取文本级语义，同样使用SoftCLIP+MSE损失。

2. **扩散模型微调（Diffusion Fine-tuning）**：
   - 将图像上下文I通过IBT转换为脑体素，再经脑嵌入器得到嵌入e<sub>p</sub>。用该嵌入作为条件微调VD模型（L<sub>img</sub>损失），让扩散模型学会从“脑信号形式”的图像表示中重建图像，弥合模态差异。

3. **脑嵌入优化（Brain Embedding Optimization）**：
   - 冻结已微调的VD模型，对真实脑上下文嵌入e<sub>b</sub>进行轻量优化（100步），使其引导扩散模型生成与图像上下文相似的结果，从而减少语义冲突。优化目标为L<sub>brain</sub>损失（类似扩散重建损失）。

4. **嵌入融合与生成（Embedding Integration & Generation）**：
   - 双上下文（图像+脑）：直接拼接e<sub>p</sub>和优化后的e<sub>b</sub>。
   - 三上下文（图像+脑+文本）：因VD模型容量限制，采用线性插值 e<sub>c</sub> = (1-α)·e<sub>p</sub> + α·e<sub>b</sub>，α ∈ [0,1]；文本嵌入送入文本流。
   - 生成时使用微调后的VD模型，结合组合嵌入，实现无掩码、单图像融合。

## 3. 实验设计

### 数据集
- **NSD（Natural Scenes Dataset）**：7T fMRI数据，8名被试观看MS-COCO图片。实验使用4名被试（Subj1,2,5,7），每人有8859张训练图片，共同观看的982张作为测试集。

### Benchmark与对比方法
- 由于传统图像定制方法需掩码或多张图像，本文设计了两种基于VD的基线：
  - **Baseline-1**：用图像上下文代替脑上下文，直接多模态融合。
  - **Baseline-2**：用SOTA fMRI重构模型（MindEye）将脑信号转为图像，再融合。
- 对比指标：CLIP-I、DINOv2（语义相似性）、CLIP-IQA（图像质量）。另用PixCorr、SSIM、AlexNet(2/5)、Inception、CLIP评估脑解码性能。
- 用户研究：22名参与者对110对生成图像评分（1-3分），基于质量和上下文一致性。

### 实验类型
1. **跨主体多上下文生成**：定性展示（图3、图4、图6），展示不同被试的融合效果及插值过程。
2. **定量对比**（表1）：Ours vs. Baseline-1 vs. Baseline-2，Ours在CLIP-I、DINOv2、CLIP-IQA上均最高。
3. **用户研究**（表2）：Ours在质量和一致性上显著优于Baseline-1。
4. **少样本泛化**：用Subj1的10%/20%/40%数据微调，测试生成效果（图8、表3），指标持续提升。
5. **消融实验**（图9、表4）：分别去除IBT、微调、优化、ClipCap，展示各组件贡献。
6. **脑解码性能**（表7、图10）：与MindBridge、UMBRAE对比，Ours达到可比或更优的脑重构性能。
7. **附录扩充**：不同种子生成、插值与拼接对比、有无文本上下文对比、IBT Pearson相关系数分析等。

## 4. 资源与算力

- 文中明确提到：每张图像生成约需6分钟（单张Tesla A100 GPU）。训练阶段：IBT 200 epochs（lr=5e-5，batch 50），脑嵌入器600 epochs（lr=3e-3），VD微调200 epochs（lr=5e-8），脑嵌入优化100 epochs（lr=1e-5）。训练在单卡A100上完成。
- **未说明**：训练总时长、使用的GPU数量（从描述看可能单卡即可）、数据并行策略等细节。

## 5. 实验数量与充分性

- **数量**：主要定量结果表4张（Table1-4、Table7），消融实验5组变体，脑解码与少样本实验。附录包含大量定性对比、可视化、参数分析。
- **充分性**：实验设计较全面：语义保持（CLIP-I/DINOv2）、质量（CLIP-IQA）、用户偏好、少样本泛化、组件消融、脑解码对比。但存在不足：缺乏与更多传统图像定制方法（如Custom Diffusion、DreamBooth）的直接对比，因这些方法不支持脑信号输入，但作者通过设计基于VD的基线做了“对齐”；此外，实验仅在NSD一个数据集上验证（fMRI数据稀缺，但可增加EEG或其他脑模态）；未讨论不同α值的系统调优分析（仅定性图5）。总体而言，实验公平且具说服力。

## 6. 主要结论与发现

- MindCustomer成功实现首项脑信号与多上下文（图像、文本、脑）融合的图像生成，生成图像自然且保持各上下文语义。
- IBT能有效模拟跨主体脑信号（Pearson平均0.426，中等正相关），显著增强脑表示预训练。
- 设计的融合管道（微调+优化+IBT映射）比直接融合或单纯重构更优，能缓解语义冲突。
- 方法在少样本（<20%数据）下即可泛化到新被试，具备实用潜力。
- 脑解码性能与SOTA方法（UMBRAE、MindBridge）相当或更优，验证了预训练的有效性。

## 7. 优点

- **首创性**：首个融合脑信号的多上下文图像生成工作。
- **实用性强**：无需掩码、无需多张图像，单张输入即可实时生成；支持跨主体和少样本泛化。
- **方法设计合理**：IBT解决数据稀缺；分步微调+优化解决语义冲突；线性插值控制融合比例。
- **实验充分**：涵盖定性、定量、用户研究、消融、脑解码、少样本等，验证全面。
- **可解释性好**：通过α插值可视化融合过程，体现模型行为可控。

## 8. 不足与局限

- **脑信号质量限制**：当前fMRI信噪比低、信息粗糙，导致生成的细节可能不如纯文本/图像生成丰富。
- **数据集单一**：仅使用NSD（fMRI），未验证在其他脑模态（如EEG、MEG）或更大规模/多样化数据上的表现。
- **对比方法有限**：传统图像定制方法无法直接对比，虽设计了基线，但缺少与端到端脑信号驱动生成方法（如MindEye+Custom Diffusion）的更细致比较。
- **计算效率**：每张图像生成需6分钟，对于实际实时应用可能偏慢。
- **超参数敏感**：α取值（0.4-0.7）依赖经验，缺少自动调优机制。
- **实验偏差风险**：用户研究中问卷数量（220份）尚未达到大规模统计检验效力；脑解码定量结果与SOTA差距很小，但未提供显著性检验。

（完）
