---
title: EEG-Language Pretraining for Highly Label-Efficient Clinical Phenotyping
title_zh: 脑电图-语言预训练用于高标签效率的临床表型分析
authors: "Sam Gijsen, Kerstin Ritter"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=yaI2ZYFmeD"
tags: ["query:eeg"]
score: 6.0
evidence: 脑电图-语言预训练用于临床表型分析；直接处理脑电图信号
tldr: 本文率先提出脑电图-语言模型（ELM），在15000份脑电图和临床报告上训练多模态对齐模型。通过时间序列裁剪和文本分割及多实例学习，解决了脑电图与文本片段不匹配的问题。模型在四项临床评估中显著优于纯脑电图模型，并首次实现零样本分类和神经信号与报告的检索。该工作为脑电图信号处理和分析提供了新的多模态框架，属于脑电图主题下的重要进展。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-yai2zyfmed/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1734, \"height\": 546, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yai2zyfmed/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1412, \"height\": 818, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yai2zyfmed/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 834, \"height\": 311, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yai2zyfmed/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1570, \"height\": 747, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yai2zyfmed/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1394, \"height\": 668, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yai2zyfmed/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1765, \"height\": 760, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yai2zyfmed/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 886, \"height\": 762, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yai2zyfmed/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1320, \"height\": 407, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yai2zyfmed/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 867, \"height\": 540, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yai2zyfmed/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 871, \"height\": 1057, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yai2zyfmed/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1321, \"height\": 547, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yai2zyfmed/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1572, \"height\": 775, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yai2zyfmed/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1043, \"height\": 621, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yai2zyfmed/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1227, \"height\": 617, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yai2zyfmed/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1225, \"height\": 618, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yai2zyfmed/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1227, \"height\": 616, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yai2zyfmed/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1228, \"height\": 618, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yai2zyfmed/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1418, \"height\": 723, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-yai2zyfmed/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 835, \"height\": 425, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-yai2zyfmed/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1504, \"height\": 550, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-yai2zyfmed/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 725, \"height\": 428, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-yai2zyfmed/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 874, \"height\": 639, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-yai2zyfmed/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 400, \"height\": 311, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-yai2zyfmed/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 466, \"height\": 278, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-yai2zyfmed/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 836, \"height\": 479, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-yai2zyfmed/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 388, \"height\": 245, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-yai2zyfmed/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1185, \"height\": 228, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-yai2zyfmed/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1500, \"height\": 226, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-yai2zyfmed/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 567, \"height\": 227, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-yai2zyfmed/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 825, \"height\": 270, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-yai2zyfmed/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1110, \"height\": 376, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-yai2zyfmed/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1106, \"height\": 203, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-yai2zyfmed/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 772, \"height\": 357, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-yai2zyfmed/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1313, \"height\": 877, \"label\": \"Table\"}]"
motivation: 脑电图多模态语言建模尚未探索，现有模型需要大量标注数据且泛化性差。
method: 提出脑电图-语言模型，利用多实例学习对齐时间序列与文本片段，实现跨模态预训练。
result: 在四个临床任务上显著优于纯脑电图基线，并实现了零样本分类和跨模态检索。
conclusion: 脑电图-语言预训练能有效利用临床报告提升脑电图分析的标签效率和泛化能力。
---

## Abstract
Multimodal language modeling has enabled breakthroughs for representation learning, yet remains unexplored in the realm of functional brain data for clinical phenotyping. This paper pioneers EEG-language models (ELMs) trained on clinical reports and 15000 EEGs. We propose to combine multimodal alignment in this novel domain with timeseries cropping and text segmentation, enabling an extension based on multiple instance learning to alleviate misalignment between irrelevant EEG or text segments. Our multimodal models significantly improve over EEG-only models across four clinical evaluations and for the first time enable zero-shot classification as well as retrieval of both neural signals and reports. In sum, these results highlight the potential of ELMs, representing significant progress for clinical applications.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：临床脑电图（EEG）数据标注极为稀缺且成本高昂，导致深度学习在EEG临床表型分析（如病理检测、癫痫、睡眠障碍）中进展缓慢。传统的自监督学习（SSL）受限于数据增强难度和低信噪比，难以学到鲁棒的表征。
- **整体含义**：受计算机视觉中视觉-语言模型（如CLIP）在多模态预训练中成功的启发，本文首次将EEG信号与对应的临床报告文本进行对齐预训练，旨在利用自然语言监督信号来学习更丰富的EEG表征，从而实现**高度标签高效**（label-efficient）的临床表型分析，并首次支持零样本分类和双向检索。

### 2. 论文提出的方法论

- **核心思想**：构建EEG-语言模型（ELM），通过对比学习对齐EEG片段和临床报告文本。EEG是长时序，报告是多段落，因此提出**子单元对齐**策略：将EEG裁剪成多个非重叠的短片段（如5-60秒），将报告分割为段落或句子。针对不同片段与文本相关性差异，进一步引入**多实例学习扩展（MIL-InfoNCE）**，允许每个EEG片段与多个文本段落对齐（双向），放松了严格匹配的假设。
- **关键技术细节**：
  - **EEG编码器**：残差CNN（约0.93M参数），可处理不同长度。
  - **文本编码器**：使用冻结的预训练医学语言模型MedCPT，避免训练不稳定和隐空间坍缩。
  - **对齐策略**：两种变体：
    - **ELM_e,l**：同时投影EEG和文本到共享隐空间，使用InfoNCE损失。
    - **ELM_l**：仅投影EEG嵌入到文本编码器的输出空间，使用均方误差对齐加正交正则化（M-FLAG风格）。
  - **MIL-InfoNCE**：在InfoNCE基础上，对每个正样本对，使用多个正样本（多个EEG裁剪或文本段落）取平均后的相似度，有效处理跨模态局部不匹配。
- **公式/算法流程**（文字描述）：
  1. 对每个EEG-报告对，从EEG中随机采样N个非重叠裁剪，从报告中随机采样M个段落/句子。
  2. 通过编码器获得EEG嵌入和文本嵌入。
  3. 计算双向MIL-InfoNCE损失：对于每个EEG裁剪，其正样本是所有来自同一报告的所有文本段落；对于每条文本段落同理。损失函数在batch内最大化正对平均相似度，最小化负对相似度。
  4. 训练结束时，EEG编码器可输出可用于下游任务的嵌入。

### 3. 实验设计

- **数据集与场景**：
  - **TUEG**：最大公开EEG数据库（n=26846），大部分无标注，但附有临床报告。用作预训练（约15000份EEG-报告对）。
  - **TUAB**：TUEG的子集，二分类病理检测（正常/异常），提供训练/测试集。
  - **NMT**：独立外部验证数据集（南亚人群），同样二分类病理检测，用于检验OOD泛化。
  - **TUSZ**：癫痫发作检测数据集，二分类（发作/背景），5秒片段级别。
  - **TUEV**：6类事件检测（3类临床事件+眼动/伪迹/背景），1秒+两侧2秒上下文。
- **Benchmark方法**：
  - **EEG-only SSL**：BYOL、VICReg、ContraWR、Relative Positioning (RP)、Temporal Shuffling (TS)、Contrastive Predictive Coding (CPC)。
  - **有监督基线**：在相同EEG编码器上直接端到端训练。
  - **大规模预训练模型**：LaBraM（Base/Large/Huge，参数量5.8M-369M），对比线性探测性能。
  - **其他SOTA**：CEREBrO、BIOT、SPaRCNet等（仅表4对比）。
- **评估方式**：
  - **线性探测**：在冻结的EEG编码器上训练逻辑回归，使用1%、10%、100%标注数据。
  - **零样本分类**：使用21种提示词模板，计算EEG嵌入与“normal/abnormal”提示嵌入的余弦相似度。
  - **双向检索**：报告→EEG和EEG→报告，Top-K准确率。

### 4. 资源与算力

- 文中明确说明：
  - 使用Nvidia GeForce GTX 3090或Tesla V100（单卡），显存小于24GB。
  - EEG-language模型预训练约9小时，EEG-only预训练约18小时（因需数据增强）。
  - 所有实验在50个epoch内完成。
  - 整体计算需求较低，远小于LaBraM-Huge等大模型。

### 5. 实验数量与充分性

- **实验数量**：
  - 在5个数据集上执行4种下游任务（TUAB、NMT、TUSZ、TUEV），每种任务测试不同标注比例（零样本、1%、10%、100%）。
  - 进行了多项消融实验：
    - 文本聚合方式（Max、Attn、Sum vs. MIL-InfoNCE）。
    - 正样本数量（N=2/4/8/16/32, M=2/4/8）。
    - 温度参数τ（0.1~1.0）。
    - 文本内容簇（临床历史、描述、用药、解释、LLM摘要）。
    - 对齐策略（ELM_e,l vs. ELM_l vs. MIL变体）。
    - 输入EEG裁剪长度（5~60秒）。
    - 语言模型对比（BiomedBERT、Bio-ClinicalBERT、MedCPT）。
    - 数据泄漏检查（在TUAB测试集上使用未见于预训练的子集重复实验）。
- **充分性**：实验设计全面，涵盖了标签效率、OOD泛化、多尺度事件检测、模型复杂度对比。所有结果均报告5次重复的均值和标准差，统计可信度高。
- **公平性**：所有方法使用相同EEG编码器架构和预训练数据，对比合理。对于LaBraM等大模型，只进行线性探测（未finetune），但仍展示了ELM的优势。

### 6. 论文的主要结论与发现

- **主要结论**：ELM在四个临床评估中显著优于所有EEG-only SSL方法，尤其在极低标注比例（1%）下，AUROC提升高达9.7%，平衡准确率提升8.7%。
- **关键发现**：
  - 多模态对齐有效利用了临床报告中的语义信息，实现了零样本病理检测（AUROC最高91.56%）。
  - MIL-InfoNCE通过处理局部不匹配进一步提升了检索和分类性能。
  - 文本内容的选择至关重要：包含医生解释（interpretation）和LLM摘要的模型性能最好；仅用临床历史或用药信息效果差。
  - 子单元对齐策略本身（即使报告随机打乱）也有助于编码被试间差异，提升病理检测，而语言语义进一步提升了标签效率。
  - 小模型（0.93M参数）的ELM在同等线性探测条件下优于超大型模型（LaBraM-Huge 369M）约0.83%平均性能，且无需finetune。

### 7. 优点

- **方法创新**：首次将多模态语言建模引入EEG领域，并针对EEG-文本的对齐难题提出了子单元对齐和MIL扩展，解决了长时序与多段落不匹配问题。
- **标签高效**：在极少标注（1%）下性能大幅提升，对临床现实（标注稀缺）有直接价值。
- **零样本能力**：首次实现EEG的零样本分类和双向检索，展示了模型对语义的深刻理解。
- **可解释性**：通过时序对齐可视化（图4），发现模型能自动定位与文本描述对应的临床事件（如癫痫放电），即使没有时间标签。
- **计算经济**：模型仅0.93M参数，训练成本低，推理快，容易部署。

### 8. 不足与局限

- **数据局限**：公开可用的EEG-报告配对数据集仅有TUEG一家，限制了预训练规模。作者提到未来可考虑用临床元数据生成合成文本。
- **偏差风险**：临床报告本身存在医师主观性和记录差异；LLM摘要可能引入额外偏差；文本内容过滤（如过滤掉技术问题段）可能丢失部分信息（实验发现模型对伪迹/眼动分类性能下降，可能与此有关）。
- **模型规模未充分缩放**：受限于计算资源，未系统探索更大EEG编码器或多模态融合架构（如跨模态注意力）的效果。
- **评估覆盖**：仅针对病理检测（二分类）和事件检测，未涉及其他常见任务（如睡眠分期、认知状态）。零样本分类仅验证了正常/异常二元提示，未测试多类或开放场景。
- **不可控因素**：温度参数τ对检索和分类影响不同，需按任务手动调节；MIL的正样本数量需根据任务调整，缺少自适应策略。

（完）
