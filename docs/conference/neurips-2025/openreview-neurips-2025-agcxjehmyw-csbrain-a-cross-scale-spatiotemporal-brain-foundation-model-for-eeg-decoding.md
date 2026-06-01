---
title: "CSBrain: A Cross-scale Spatiotemporal Brain Foundation Model for EEG Decoding"
title_zh: CSBrain：面向脑电解码的跨尺度时空脑基础模型
authors: "Yuchen Zhou, Jiamin Wu, Zichen Ren, Zhouheng Yao, Weiheng Lu, Kunyu Peng, Qihao Zheng, Chunfeng Song, Wanli Ouyang, Chao Gou"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=agcXjEHmyW"
tags: ["query:eeg"]
score: 9.0
evidence: 面向脑机接口的脑电解码
tldr: 针对现有脑电基础模型忽略神经活动跨尺度时空结构的问题，本文提出CSBrain——一个跨尺度的时空脑基础模型。该方法通过显式建模不同时间与空间尺度的脑电模式，提升了脑电解码的泛化能力。实验表明，CSBrain在多种脑机接口任务上取得优异效果，为脑电信号分析与脑机接口研究提供了新范式。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-agcxjehmyw/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1365, \"height\": 627, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-agcxjehmyw/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1365, \"height\": 675, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-agcxjehmyw/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1430, \"height\": 246, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-agcxjehmyw/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1373, \"height\": 342, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-agcxjehmyw/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1375, \"height\": 341, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-agcxjehmyw/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1187, \"height\": 323, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-agcxjehmyw/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1002, \"height\": 558, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-agcxjehmyw/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1452, \"height\": 636, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-agcxjehmyw/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1435, \"height\": 408, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-agcxjehmyw/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1439, \"height\": 409, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-agcxjehmyw/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1380, \"height\": 345, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-agcxjehmyw/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 648, \"height\": 325, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-agcxjehmyw/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1386, \"height\": 334, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-agcxjehmyw/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1007, \"height\": 669, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-agcxjehmyw/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1017, \"height\": 681, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-agcxjehmyw/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1435, \"height\": 519, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-agcxjehmyw/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1435, \"height\": 526, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-agcxjehmyw/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1404, \"height\": 591, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-agcxjehmyw/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 882, \"height\": 887, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-agcxjehmyw/fig-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 882, \"height\": 887, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-agcxjehmyw/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1457, \"height\": 586, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-agcxjehmyw/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1444, \"height\": 1006, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-agcxjehmyw/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 750, \"height\": 956, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-agcxjehmyw/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 822, \"height\": 533, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-agcxjehmyw/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1313, \"height\": 516, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-agcxjehmyw/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1310, \"height\": 517, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-agcxjehmyw/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1313, \"height\": 517, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-agcxjehmyw/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1309, \"height\": 515, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-agcxjehmyw/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1308, \"height\": 515, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-agcxjehmyw/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1311, \"height\": 517, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-agcxjehmyw/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1312, \"height\": 516, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-agcxjehmyw/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1313, \"height\": 516, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-agcxjehmyw/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1313, \"height\": 516, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-agcxjehmyw/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1312, \"height\": 518, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-agcxjehmyw/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1348, \"height\": 521, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-agcxjehmyw/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1312, \"height\": 515, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-agcxjehmyw/table-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1313, \"height\": 518, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-agcxjehmyw/table-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1313, \"height\": 517, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-agcxjehmyw/table-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1312, \"height\": 516, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-agcxjehmyw/table-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1311, \"height\": 517, \"label\": \"Table\"}]"
motivation: 现有脑电基础模型采用尺度无关的密集建模范式，忽略了神经活动的跨尺度时空结构。
method: 提出跨尺度时空脑基础模型，显式编码不同时间与空间尺度的脑电模式。
result: 在多个脑电解码任务上取得优于现有方法的性能。
conclusion: 跨尺度时空建模是提升脑电基础模型能力的关键。
---

## Abstract
Understanding and decoding human brain activity from electroencephalography (EEG) signals is a fundamental problem in neuroscience and artificial intelligence, with applications ranging from cognition and emotion recognition to clinical diagnosis and brain–computer interfaces. While recent EEG foundation models have made progress in generalized brain decoding by leveraging unified architectures and large-scale pretraining, they inherit a scale-agnostic dense modeling paradigm from NLP and vision. This design overlooks an intrinsic property of neural activity—cross-scale spatiotemporal structure. Different EEG task patterns span a broad range of temporal and spatial scales, from brief neural activations to slow-varying rhythms, and from localized cortical activations to large-scale distributed interactions. Ignoring this diversity may lead to suboptimal representations and weakened generalization ability. To address these limitations, we propose CSBrain, a Cross-scale Spatiotemporal Brain foundation model for generalized EEG decoding. CSBrain introduces two key components: (i) Cross-scale Spatiotemporal Tokenization (CST), which aggregates multi-scale features within localized temporal windows and anatomical brain regions into compact scale-aware token representations; and (ii) Structured Sparse Attention (SSA), which models cross-window and cross-region dependencies for diverse decoding tasks, further enriching scale diversities while eliminating the spurious dependencies. CST and SSA are alternately stacked to progressively integrate cross-scale spatiotemporal dependencies. Extensive experiments across 11 representative EEG tasks and 16 datasets demonstrate that CSBrain consistently outperforms both task-specific models and strong foundation baselines. These results establish cross-scale modeling as a key inductive bias for generalized EEG decoding and highlight CSBrain as a robust backbone for future brain–AI research.

---

## 论文详细总结（自动生成）

# CSBrain: 跨尺度时空脑基础模型用于EEG解码 - 论文详细总结

## 1. 核心问题与整体含义（研究动机和背景）

- **问题**：现有的EEG基础模型（如BIOT、LaBraM、CBraMod）沿用了NLP和视觉领域的“尺度无关的密集建模”范式——将EEG信号分割成固定尺度的token，然后对所有token进行密集自注意力计算。然而，这种设计忽略了神经活动的内在特性：**跨尺度时空结构**。不同EEG解码任务（如运动想象、情绪识别、睡眠分期）在时间和空间尺度上差异巨大，例如运动想象涉及短暂、局部的神经活动，而情绪识别则需要广泛脑区的长时间协同。

- **后果**：尺度无关的tokenization导致token表示与任务语义不匹配；结构无关的密集注意力在噪声大的EEG信号中引入虚假依赖、降低表示质量并增加计算开销；最终限制了模型在不同BCI任务间的泛化能力。

- **意义**：提出跨尺度、结构感知的EEG基础模型范式，为构建生理一致性且可扩展的通用EEG表示学习框架奠定基础，有望推动脑机接口、临床诊断和认知科学的发展。

## 2. 方法论：核心思想、关键技术细节

### 2.1 整体架构
CSBrain采用“预处理 → 交替堆叠的CST与SSA模块 → 任务头”的流水线。预处理包括信号标准化（滤波、重采样至200Hz、归一化至100 μV）、分段、时频特征提取并融合，加上位置编码得到初始表示 \(x^{(0)} \in \mathbb{R}^{C \times n \times d}\)。

### 2.2 跨尺度时空Tokenization (CST)
- **时间Tokenization**：对每个通道的每个时间位置，使用多尺度1D卷积核集合 \(\mathcal{C}_T = \{ \text{Conv}_t^{(k)} \}_{k=1}^K\) 在局部时间窗口内提取多尺度时间特征，拼接后通过残差投影对齐维度，得到跨尺度时间token \(\hat{x}^{(l)}_{i,j}\)。
- **空间Tokenization**：将电极按国际10-20系统划分为脑区（额叶、中央、顶叶、颞叶、枕叶）。对每个电极，在其所属脑区内定义多尺度空间邻域，使用多尺度1D卷积核 \(\mathcal{C}_S\) 聚合邻域内电极特征，拼接后加残差投影，得到最终跨尺度token \(\tilde{x}^{(l)}_{i,j}\)。
- **维度分配**：采用指数衰减方案，小核分配更高维度以保留细粒度特征，大核分配较低维度用于粗粒度上下文。

### 2.3 结构化稀疏注意力 (SSA)
- **跨窗口注意力**：将token按时间窗口内相同相对位置分组（形成 \(w\) 个组），在每个组内计算自注意力，捕获长程时序依赖。复杂度线性于 \(O(N \cdot k)\)。
- **跨区域注意力**：从每个脑区按顺序采样一个代表token，并与该脑区均值池化特征相加，形成区域描述子，组合成空间组，在其上计算自注意力，建模跨脑区依赖。
- 最后经过层归一化和FFN得到输出 \(x^{(l)}_{i,j}\)。

### 2.4 预训练：掩码自编码
- 在未标注EEG上随机掩码50%的时间片段，使用可学习掩码token代替，通过CST+SSA编码重建被掩码段，损失为均方误差。
- 预训练数据集：TUEG（Temple University Hospital EEG corpus），共1,109,545个30秒片段（>9,000小时）。

### 2.5 公式流程
1. 预处理：\(E \rightarrow E_p \in \mathbb{R}^{C \times n \times t}\)
2. 初始编码：\(x^{(0)} = \text{Conv1D}(E_p) + \text{FFT-FC}(E_p) + \text{PosEnc}\)
3. 对 \(l=1..L\) 交替：
   - 时间Tokenization：\(\hat{x}^{(l)} = \text{Concat}(\{\text{Conv}_t^{(k)}(W_t^{(k)}(i))\} ) + \text{Proj}_t(x^{(l-1)}_{i,j})\)
   - 空间Tokenization：\(\tilde{x}^{(l)} = \text{Concat}(\{\text{Conv}_s^{(k)}(W_s^{(k)}(j))\} ) + \text{Proj}_s(\hat{x}^{(l)}_{i,j})\)
   - 跨窗口注意力：\(\tilde{x}^{(l,win)} = \text{Attn}(\mathcal{G}_t^{(g)})_{i,j} + \tilde{x}^{(l)}\)
   - 跨区域注意力：\(\tilde{x}^{(l,reg)} = \text{Attn}(\mathcal{G}_s^{(g)})_{i,j} + \tilde{x}^{(l,win)}\)
   - 输出：\(x^{(l)} = \text{FFN}(\text{LN}(\tilde{x}^{(l,reg)})) + \tilde{x}^{(l,reg)}\)
4. 下游任务头（分类/回归）。

## 3. 实验设计

### 3.1 数据集与任务
涵盖**11个代表性EEG解码任务**、**16个公开数据集**，具体：
- **运动想象分类**：BCIC-IV-2a、PhysioNet-MI、SHU-MI
- **情绪识别**：FACED、SEED-V
- **癫痫检测**：CHB-MIT、Siena
- **睡眠分期**：ISRUC、HMC
- **想象语音分类**：BCIC2020-3
- **警觉度估计**：SEED-VIG（回归）
- **精神压力检测**：MentalArithmetic
- **精神障碍诊断**：Mumtaz2016
- **事件类型分类**：TUEV
- **异常检测**：TUAB
- **慢波事件分类**：TUSL

### 3.2 Benchmark与对比方法
- **任务专用模型**：EEGNet、EEGConformer、SPaRCNet、ContraWR、CNN-Transformer、FFCL、ST-Transformer
- **EEG基础模型**：BIOT、LaBraM、CBraMod
- 评估指标：多类任务用Balanced Accuracy、Cohen's Kappa、Weighted F1；二类任务加AUC-PR、AUROC；回归用Pearson Correlation、R²、RMSE。

### 3.3 实验设置
- 预训练：TUEG数据集，4×NVIDIA A100 GPU，批次128，40 epoch，约101小时。
- 下游微调：每个数据集严格按官方或文献划分训练/验证/测试集，使用相同超参数模板（学习率1e-4，权重衰减1e-2等），部分数据集微调学习率和权重衰减以保证稳定训练。
- 所有结果均为5次不同随机种子平均。

## 4. 资源与算力
- **预训练硬件**：4张NVIDIA A100 GPU。
- **预训练时间**：约101小时（40 epoch，批次128）。
- **模型参数**：默认12层Transformer，隐藏维度200，参数约4.9M（从缩放实验得知2-12层对应1.4M-4.9M）。
- **下游微调**：在单GPU上训练，每数据集训练50 epoch，但未报告总时间。
- 未明确说明显存消耗或具体GPU型号（A100）。

## 5. 实验数量与充分性
- **主实验**：在16个数据集上对比10个基线，每个报告3个指标（表2），完整结果（含标准差）在附录。
- **消融与分析**：
  - Tokenization尺度对比（K=1,2,3及单次vs.交替堆叠），在4个数据集上验证。
  - 注意力机制对比（Dense、Criss-cross、SSA），在2个数据集上报告计算复杂度与性能。
  - 预训练有效性（有vs.无预训练），在4个数据集上展示。
  - 缩放分析：预训练数据量（10h→9000h）和模型参数（2→12层），各在2个数据集上报告趋势。
  - 区域描述子消融（Token only、Mean only、Random Sample、Ours），在4个数据集上验证。
- **可视化**：Grad-CAM地形图（4个任务）、t-SNE（2个数据集）、注意力热图、通道相似性矩阵。
- **充分性评价**：实验覆盖了主流EEG任务类型（分类、回归、多类、二类），数据集规模从数百到数十万样本，对比了最新最强基线，消融实验全面且设计合理。但未进行跨领域（如MEG/fMRI）迁移实验，也未在更多模型架构（如GNN、Mamba）上比较。

## 6. 主要结论与发现
1. **CSBrain在几乎所有任务上达到SOTA**：宏观平均得分0.7095，超越CBraMod（0.6760）3.35%、LaBraM（0.6697）3.98%、BIOT（0.6322）7.73%。
2. **基础模型整体优于任务专用模型**：说明统一架构+大规模预训练的有效性。
3. **交叉尺度tokenization重要性**：多尺度（K=3）优于单尺度，交替堆叠优于单次应用。
4. **结构化稀疏注意力优于密集注意力**：SSA以线性复杂度取得更好性能，减少虚假依赖。
5. **预训练带来显著增益**，尤其在数据量少的任务（如BCIC-IV-2a提升约18%平衡准确率）。
6. **缩放规律**：增加预训练数据和模型参数均能提升性能，但在数据>5000小时后收益递减。

## 7. 优点
- **方法创新**：首次将跨尺度时空结构显式引入EEG基础模型，提出CST和SSA两个互补模块，具有神经生理合理性。
- **实验全面**：在16个数据集、11类任务上验证，对比10个基线，涵盖主流与最新方法。
- **分析与可视化详尽**：tokenization、注意力、预训练、缩放、区域描述子等多角度消融，Grad-CAM和t-SNE可视化增强可解释性。
- **效率优势**：SSA在线性复杂度下取得最优性能，适合实际部署。
- **代码开源**：提供GitHub仓库（https://github.com/yuchen2199/CSBrain），便于复现。

## 8. 不足与局限
- **缩放探索有限**：最大模型仅4.9M参数，预训练数据约9000小时，未达到大规模语言/视觉模型的规模；未系统研究大模型（如>100M）的性能。
- **数据集覆盖仍有偏差**：未涉及如视觉诱发电位、P300等范式；未测试跨模态迁移（如EEG→fMRI）。
- **预训练数据单一**：仅使用TUEG数据集，其包含大量临床EEG（癫痫、异常），可能引入领域偏好。
- **训练时长未充分报告**：下游微调的总算力未列出，复现成本不透明。
- **未与其他架构（GNN、Mamba）对比**：附录中虽提到未来计划，但当前实验缺少此类对比。
- **潜在隐私与伦理风险**：模型可解码心理状态，可能用于非同意场景；论文仅在附录简要提及伦理。

（完）
