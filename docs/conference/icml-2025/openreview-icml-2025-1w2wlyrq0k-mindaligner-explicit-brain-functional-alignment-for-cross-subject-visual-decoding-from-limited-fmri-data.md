---
title: "MindAligner: Explicit Brain Functional Alignment for Cross-Subject Visual Decoding from Limited fMRI Data"
title_zh: MindAligner：基于显式脑功能对齐的有限fMRI数据跨被试视觉解码
authors: "Yuqin Dai, Zhouheng Yao, Chunfeng Song, Qihao Zheng, Weijian Mai, Kunyu Peng, Shuai Lu, Wanli Ouyang, Jian Yang, Jiamin Wu"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=1W2WlYRq0K"
tags: ["query:eeg-latent"]
score: 4.0
evidence: 脑信号潜空间对齐用于跨被试解码
tldr: 论文提出显式功能对齐框架MindAligner，通过脑迁移矩阵将新被试的fMRI信号映射到已知被试的潜空间，实现跨被试视觉解码，有效应对数据有限和个体差异问题。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-1w2wlyrq0k/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1720, \"height\": 632, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-1w2wlyrq0k/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1719, \"height\": 729, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-1w2wlyrq0k/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1602, \"height\": 575, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-1w2wlyrq0k/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 769, \"height\": 832, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-1w2wlyrq0k/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 820, \"height\": 690, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-1w2wlyrq0k/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 833, \"height\": 414, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-1w2wlyrq0k/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 835, \"height\": 559, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-1w2wlyrq0k/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1720, \"height\": 1106, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-1w2wlyrq0k/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1577, \"height\": 716, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-1w2wlyrq0k/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1508, \"height\": 243, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-1w2wlyrq0k/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 731, \"height\": 171, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-1w2wlyrq0k/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1073, \"height\": 446, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-1w2wlyrq0k/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 967, \"height\": 360, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-1w2wlyrq0k/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1611, \"height\": 377, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-1w2wlyrq0k/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1610, \"height\": 1000, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-1w2wlyrq0k/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1622, \"height\": 232, \"label\": \"Table\"}]"
motivation: 现有脑解码局限于单被试范式，跨被试泛化弱且训练成本高，fMRI数据有限加剧挑战。
method: 学习脑迁移矩阵将任意新被试的脑信号投影到已知被试的潜空间，利用已知被试的解码器。
result: 在有限数据下实现跨被试视觉解码，显著优于单被试基线且降低训练代价。
conclusion: 显式功能对齐可有效桥接个体差异，推动脑解码的泛化应用。
---

## Abstract
Brain decoding aims to reconstruct visual perception of human subject from fMRI signals, which is crucial for understanding brain's perception mechanisms.  Existing methods are confined to the single-subject paradigm due to substantial brain variability, which leads to weak generalization across individuals and incurs high training costs, exacerbated by limited availability of fMRI data. To address these challenges, we propose MindAligner, an explicit functional alignment framework for cross-subject brain decoding from limited fMRI data. The proposed MindAligner enjoys several merits. First, we learn a Brain Transfer Matrix (BTM) that projects the brain signals of an arbitrary new subject to one of the known subjects, enabling seamless use of pre-trained decoding models. Second, to facilitate reliable BTM learning, a Brain Functional Alignment module is proposed to perform soft cross-subject brain alignment under different visual stimuli with a multi-level brain alignment loss, uncovering fine-grained functional correspondences with high interpretability. Experiments indicate that MindAligner not only outperforms existing methods in visual decoding under data-limited conditions, but also provides valuable neuroscience insights in cross-subject functional analysis. The code will be made publicly available.

---

## 论文详细总结（自动生成）

# 论文《MindAligner: Explicit Brain Functional Alignment for Cross-Subject Visual Decoding from Limited fMRI Data》详细中文总结

## 1. 核心问题与整体含义（研究动机和背景）

- **核心问题**：现有的fMRI脑视觉解码方法大多局限于单被试范式，即对每个被试单独训练解码模型。由于不同个体之间的大脑结构、认知模式存在巨大差异（大脑变异性），单被试模型无法直接跨被试泛化，导致：  
  - 每增加一个新被试就需要从头训练，训练成本高；  
  - 实际应用中（如脑机接口、临床诊断）fMRI数据获取昂贵且有限，进一步加剧了跨被试泛化的困难。  
- **研究动机**：如何利用有限的新被试数据（例如仅1小时的fMRI扫描）实现有效的跨被试视觉解码，同时保持高解码质量和可解释性。  
- **整体含义**：论文提出**显式功能对齐**框架MindAligner，学习一个“脑迁移矩阵”（BTM），将新被试的fMRI信号直接映射到已知被试的脑空间，从而无缝复用预训练解码模型。这避免了隐式对齐方法中普遍存在的“多被试共用一个潜空间导致对齐不充分、缺乏可解释性”的问题。

## 2. 方法论：核心思想、关键技术细节、算法流程

- **核心思想**：通过显式线性变换（BTM）将新被试的fMRI信号在体素级别对齐到已知被试的脑信号，使对齐后的信号可以直接输入已知被试的预训练解码模型。  
- **关键技术细节**：  
  - **脑迁移矩阵（Brain Transfer Matrix, BTM）**：表示为两个低秩矩阵的乘积 `M = A × B`，其中 `A ∈ R^{n×h}`，`B ∈ R^{h×k}`，n和k分别为新、已知被试的体素维度，h为隐藏维度（默认4096）。这一分解降低了参数量，便于有限数据下的学习。  
  - **脑功能对齐模块（Brain Functional Alignment, BFA）**：由于现有数据集缺乏两位被试观看完全相同的图片（严格配对），BFA设计了一个**跨刺激神经映射器（Cross-stimulus Neural Mapper）**，利用视觉刺激差异作为条件，将新被试的fMRI潜变量变换到已知被试的刺激对应的潜变量，从而生成近似配对的fMRI对。  
  - **多级脑对齐损失**：  
    - 信号级重建损失 `L_rec`：对齐生成的fMRI与真实fMRI的L2距离。  
    - KL散度损失 `L_KL`：保证生成分布与真实分布一致。  
    - 潜空间对齐损失 `L_latent`：基于CLIP视觉语义相似度，约束两被试的fMRI嵌入相似度与对应图像相似度一致，实现细粒度的功能对齐。  
    - 总损失为 `L_align = L_dec + α_rec L_rec + α_KL L_KL + α_la L_latent`，其中 `L_dec` 是基础解码模型的损失。  
- **算法流程**（文字说明）：  
  - 训练阶段：预训练基础解码模型（如MindEye2）在已知被试的完整数据上；冻结解码模型；对新被试，使用BFA模块联合学习BTM、映射器和功能嵌入器，优化上述多级损失。  
  - 推理阶段：仅保留BTM，将新被试的fMRI线性变换到已知被试空间，然后送入预训练解码模型生成图像。

## 3. 实验设计

- **数据集**：Natural Scenes Dataset (NSD) – 最大规模公开fMRI视觉数据集，含4名被试（subj1,2,5,7）观看MSCOCO图片的脑活动记录。  
- **场景与benchmark**：  
  - 数据有限场景（1小时数据 ≈ 2.5% 完整数据集）下的跨被试解码。  
  - 预训练解码模型采用MindEye2（隐式对齐基线）的结构，在其上添加MindAligner对齐模块。  
- **对比方法**：  
  - MindEye2（Scotti et al., 2024b）– 隐式共享潜空间对齐基线。  
  - MindBridge（Wang et al., 2024）– 生成伪刺激来对齐的跨被试方法。  
- **评估指标**：  
  - 低层指标：PixCorr, SSIM, AlexNet(2), AlexNet(5)  
  - 高层指标：Inception, CLIP, EfficientNet-B, SwAV  
  - 检索指标：Image retrieval（图像检索）和Brain retrieval（脑检索）的Top-1准确率  
  - 功能对齐指标：fMRI Spatial Correlation (fSC) 和 Transfer Quantity (TQ)

## 4. 资源与算力

- 论文明确说明：训练在**单个NVIDIA A100 GPU**上完成，收敛时间约为**12小时**。  
- 参数规模：BTM仅占解码模型总参数的约**5.2%**（139.23M vs 2.21G），加上映射器和嵌入器共约**6.2%**。  
- 推理时间：每张图像约5.056秒，与基线MindEye2（5.000秒）几乎持平。

## 5. 实验数量与充分性

- **主要定量对比**（表1）：对4名被试（subj1,2,5,7）作为新被试，分别进行跨被试解码，报告平均值和单被试结果。  
- **消融实验**（表2）：分别移除 `L_rec`, `L_KL`, `L_latent`，验证各损失的必要性。  
- **效率对比**（表3）：与MindEye2的参数量和推理时间比较。  
- **隐藏大小消融**（附录表D）：从64到4096步进，验证性能与参数平衡。  
- **不同已知被试对齐影响**（表7、图4、图8）：固定新被试，对齐不同已知被试，显示结果稳定。  
- **功能对齐分析**（图5-7）：TQ热图、fSC对比、有限数据 vs 全数据对齐效果。  
- **非线性架构对比**（附录表F）：替换线性模块为Transformer，验证线性假设的有效性。  
- **实验充分性评价**：  
  - 覆盖了主要对比方法和多种消融，实验设计完整。  
  - 使用NSD标准数据集，评估指标全面（8个指标 + 检索）。  
  - 对神经科学可解释性进行了专门分析，实验客观且公平。

## 6. 主要结论与发现

- MindAligner在数据有限条件下（1小时数据）显著优于MindEye2和MindBridge，在脑检索指标上提升**17.9%**。  
- 显式对齐比隐式对齐更有效，能避免多被试潜空间冲突，产生更准确的跨被试映射。  
- 对齐后的信号可直接复用预训练解码模型，仅需学习解码模型6%的参数量。  
- 功能对齐分析揭示：早期视觉皮层（EarlyVis）跨被试一致性高，而高级视觉区（如FFA, PPA, OPA）变异性大；腹侧通路个体差异最大，与高级语义处理相关。  
- 仅用1小时数据即可稳定捕获与全数据相似的跨被试映射模式，展现鲁棒性。

## 7. 优点

- **显式对齐的创新性**：不同于现有隐式对齐方法，MindAligner在原始脑空间（体素级）建立明确映射，可解释性强，且避免了共享潜空间的信息损失。  
- **高效轻量**：BTM仅占解码模型6%参数量，训练快（12小时 A100），推理几乎无额外开销。  
- **无需严格配对刺激**：通过跨刺激神经映射器和语义引导损失，在仅有相似刺激而未配对数据下实现可靠对齐，极具实用性。  
- **神经科学可解释性**：通过TQ和fSC热图，定量揭示跨被试脑功能差异，与已知神经科学原理一致，为后续研究提供工具。  
- **实验验证充分**：多指标、多被试、多消融、超参数分析、功能分析一应俱全。

## 8. 不足与局限

- **依赖预训练解码器**：BTM对齐后的信号需送入已知被试的解码模型，因此解码性能上限受限于预训练模型质量，且要求已知被试有完整解码模型。  
- **仅评估视觉解码**：方法专门针对fMRI→图像重建，未测试对其他模态或任务的泛化性。  
- **线性假设的局限**：虽然线性变换在视觉皮层建模中有效，但复杂认知过程可能需要非线性映射，附录实验显示线性优于Transformer（可能因数据有限），在更多数据或更高级任务下非线性可能更优。  
- **数据集单一**：仅在NSD上评估，涉及4名被试和自然场景图片，未在更多被试、不同刺激类型（如视频、文字）上验证。  
- **忽略时间动态**：当前使用单时刻fMRI，未利用时序信息，可能丢失动态脑活动特征。  
- **潜在偏差**：可能对脑区可解释性分析局限于预先定义的ROI，未进行全脑探索性分析。  
- **应用限制**：对于脑损伤或疾病患者，大脑变异性可能更大，线性对齐可能不够鲁棒；需要更多临床验证。

（完）
