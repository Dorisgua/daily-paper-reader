---
title: Are Large Brainwave Foundation Models Capable Yet ? Insights from Fine-Tuning
title_zh: 大型脑波基础模型的能力如何？来自微调的见解
authors: "Na Lee, Konstantinos Barmpas, Yannis Panagakis, Dimitrios Adamos, Nikolaos Laskaris, Stefanos Zafeiriou"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=J5SbLoq7Uv"
tags: ["query:eeg"]
score: 7.0
evidence: 系统评估大型脑波基础模型在包括EEG的BCI基准任务上的性能
tldr: "该文对现有大型脑波基础模型在多个脑机接口基准任务（包括记忆任务和睡眠阶段分类）上进行了系统性微调评估。结果表明，这些LBM相比传统深度架构仅获得0.5%的边际提升，却需要数百万参数，远多于传统模型的数千参数。这一发现质疑了大型脑波基础模型在当前BCI任务中的效率和必要性，为未来脑电模型设计提供了重要参考。"
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-j5sbloq7uv/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 707, \"height\": 266, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-j5sbloq7uv/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 700, \"height\": 315, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-j5sbloq7uv/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 884, \"height\": 522, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-j5sbloq7uv/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 816, \"height\": 622, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-j5sbloq7uv/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1778, \"height\": 424, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-j5sbloq7uv/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1448, \"height\": 207, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-j5sbloq7uv/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1456, \"height\": 206, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-j5sbloq7uv/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 870, \"height\": 355, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-j5sbloq7uv/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1592, \"height\": 673, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-j5sbloq7uv/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1780, \"height\": 812, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-j5sbloq7uv/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1164, \"height\": 280, \"label\": \"Table\"}]"
motivation: 大型脑波基础模型在BCI任务上的实际能力尚不明确。
method: 对现有大型脑波基础模型进行系统性微调实验，在多个BCI基准任务上评测。
result: "大型脑波基础模型性能提升微小（0.5%）且参数巨大，效率远低于传统架构。"
conclusion: 当前大型脑波基础模型的效率低下，其在BCI中的适用性值得重新思考。
---

## Abstract
Foundation Models have demonstrated significant success across various domains in Artificial Intelligence (AI), yet their capabilities for brainwave modeling remain unclear. In this paper, we comprehensively evaluate current Large Brainwave Foundation Models (LBMs) through systematic fine-tuning experiments across multiple Brain-Computer Interface (BCI) benchmark tasks, including memory tasks and sleep stage classification. Our extensive analysis shows that state-of-the-art LBMs achieve only marginal improvements (0.5\%) over traditional deep architectures while requiring significantly more parameters (millions vs thousands), raising important questions about their efficiency and applicability in BCI contexts. Moreover, through detailed ablation studies and Low-Rank Adaptation (LoRA), we significantly reduce trainable parameters without performance degradation, while demonstrating that architectural and training inefficiencies limit LBMs' current capabilities. Our experiments span both full model fine-tuning and parameter-efficient adaptation techniques, providing insights into optimal training strategies for BCI applications. We pioneer the application of LoRA to LBMs, revealing that performance benefits generally emerge when adapting multiple neural network components simultaneously. These findings highlight the critical need for domain-specific development strategies to advance LBMs, suggesting that current architectures may require  redesign to fully leverage the potential of foundation models in brainwave analysis.

---

## 论文详细总结（自动生成）

# 大型脑波基础模型足够胜任吗？微调带来的启示

## 1. 论文的核心问题与整体含义（研究动机和背景）

**研究动机**：基础模型在自然语言处理和计算机视觉等领域取得了巨大成功，但其在脑波建模（尤其是脑机接口 BCI）上的能力尚不明确。研究者开始开发大型脑波基础模型（Large Brainwave Models, LBMs），但缺乏系统评估。

**核心问题**：当前最先进的LBMs（LaBraM、NeuroGPT）是否真的优于传统深度学习方法？它们的参数效率、泛化能力和微调策略是否合理？

**整体含义**：论文通过严格的微调实验发现，LBMs相比传统深度学习模型（如EEGNet、EEG-Inception）仅带来0.9%~1.2%的平均准确率提升，却需要数百万甚至上亿的可训练参数（传统模型仅需数千）。这质疑了当前LBM在BCI领域的实用性和效率，并指出需要领域特定的架构设计和训练策略。

## 2. 论文提出的方法论：核心思想、关键技术细节

### 核心思想
系统比较两种代表性LBM（LaBraM和NeuroGPT）与两种传统深度学习模型；并探索参数高效微调技术LoRA在LBM上的应用。

### 关键技术细节

- **LaBraM**：
  - 使用向量量化神经频谱预测训练神经码本（neural codebook）。
  - 预训练：预测掩码EEG通道块的原始神经码本。
  - 微调时添加简单的分类头：线性层 + Dropout(0.5)。

- **NeuroGPT**：
  - 基于EEGConformer的编码器 + GPT风格的自回归训练（预测下一个掩码token）。
  - 微调时添加三层MLP分类头（1024→256→32→n_cls），使用ELU激活和Dropout。

- **LoRA（Low-Rank Adaptation）**：
  - 将权重更新分解为低秩矩阵：ΔW = A·B，其中A∈R^{d×r}, B∈R^{r×k}, r远小于d,k。
  - 原始权重W冻结，仅训练A、B，可训练参数从d×k减至r×(d+k)。
  - 应用于注意力层的Q、K、V（视为单一矩阵Wqkv）、全连接层和卷积层。
  - 缩放因子α设为8，不调整偏置项。

- **多种LoRA配置**：
  - 固定卷积层秩rc=4（LaBraM）或8（NeuroGPT），变动注意力/全连接层秩r∈{1,2,4,8,16}。
  - 消融实验：仅调整注意力/全连接/卷积层或两两/三组合。
  - 在LoRA适配器中引入dropout（概率0.5）研究正则化效果。

## 3. 实验设计

### 数据集与基准任务
五个BCI下游分类任务：

| 任务 | 数据集 | 说明 |
|------|--------|------|
| 运动想象 | High Gamma (Schirrmeister) | 运动范式 |
| 事件相关电位(ERP) | Korean University (Hong-Kyung) | ERP范式 |
| 工作记忆 | Pavlov et al. | 记忆任务（未出现在预训练中） |
| 睡眠分期 | Sleep-EDF (Kemp) | 物理网睡眠数据集 |
| 睁眼/闭眼 | Physionet Motor (Schalk) | 简单二元分类 |

所有数据集经过预处理（统一采样率、滤波、去噪、公共平均参考）。使用subject-independent的10折交叉验证（按受试者划分，确保训练/验证集无重叠）。每个模型训练20个epoch。

### 对比方法

- **传统深度学习基线**：
  - EEGNet（2,394参数）
  - EEG-Inception（22,366参数）

- **LBM基线**：
  - LaBraM base（5,854,288参数）
  - NeuroGPT 全模型（78,536,146参数）
  - NeuroGPT 编码器仅（717,958参数）

- **微调方案**：
  1. 全模型微调（所有参数可训练）
  2. 冻结预训练权重，仅训练分类头
  3. LoRA参数高效微调（多种秩和层组合）
  4. LoRA + Dropout

## 4. 资源与算力

**论文未明确说明使用的GPU型号、数量、训练时长等具体硬件信息。** 仅提及每个配置训练20个epoch、10折交叉验证。模型参数量在表1给出（最大NeuroGPT全模型约7853万参数，LaBraM约585万）。无计算时间或能耗数据。

## 5. 实验数量与充分性

### 实验数量
共进行了**至少7组主要实验**：

1. **全模型微调性能对比**（表1）：5个模型×5个任务 = 25个结果。
2. **统计显著性检验**（表2）：配对t检验，3个比较。
3. **冻结预训练权重性能**（表3）：3个模型×5个任务 = 15个结果。
4. **LoRA不同秩实验**（表5）：3个模型×5个秩×4个任务（除motor外？实际表5有4个任务：ERP、Memory、Sleep、Eyes）≈ 60个结果。
5. **LoRA层组合消融**（表6）：3个模型×7种层组合×4个任务 ≈ 84个结果。
6. **LoRA dropout实验**（表7）：LaBraM的5个秩×4个任务 = 20个差异值。
7. **模型结构细节**（表4）：分类头设计。

### 充分性与公平性

- **优点**：使用了多种任务、多种模型配置；subject-independent交叉验证避免了受试者泄漏；统计检验支持结论；消融实验覆盖了LoRA的关键维度（秩、层类型、dropout）。
- **不足**：
  - 仅使用准确率作为唯一指标（未报告F1、AUC等）。
  - 统一20个epoch可能未使所有模型充分收敛（尤其大模型需要更多epoch）。
  - 未对传统基线进行超参数调优（公平性存疑）。
  - 仅包含分类任务，未评估回归或生成任务。
  - 消融实验仅对每个模型使用其最佳秩r'，未交叉验证其他秩下的层组合效果。

总体而言，实验设计较为全面且客观，但仍有改进空间。

## 6. 论文的主要结论与发现

1. **性能边际提升**：LBMs在精细微调后平均准确率仅比传统深度学习模型高0.9%~1.2%（最高NeuroGPT编码器0.745 vs EEG-Inception 0.733），但参数量大出数十至数百倍。

2. **冻结训练效果差**：冻结预训练权重、仅训练分类头时，平均准确率降至0.635~0.663，远低于传统基线（0.731~0.733），说明需要全模型微调。

3. **LoRA有效性**：LoRA能显著减少可训练参数（如LaBraM从585万降至约3.4万）且性能几乎不变（甚至略优）。

4. **最佳LoRA层组合**：同时调整卷积层与全连接层或注意力层时效果最好；仅调整单一层型（如仅注意力）性能较低。

5. **注意力层重要性存疑**：消融表明注意力层可能不如时间编码部分重要（两者组合与仅全连接+卷积性能相当）。

6. **LoRA dropout收益**：对LaBraM在LoRA适配器中加入dropout（0.5）可进一步提升性能，尤其在高秩时对记忆和睡眠任务改善明显。

7. **当前LBM缺陷**：架构和训练效率限制了其潜力，需要领域特定的重新设计（如更优的预训练策略、掩码方法、多模态融合）。

## 7. 优点

- **系统性与完整性**：首次在同一框架下对两个代表性LBM进行全面微调评估，涵盖全量微调、冻结、LoRA、消融、dropout等。
- **首次应用LoRA于脑波基础模型**：提供了参数高效微调的详细指南，包括层选择、秩选择、dropout影响。
- **公平的评估设计**：使用subject-independent交叉验证，避免数据泄漏；统计检验验证显著性。
- **揭示重要见解**：指出当前LBM的“大而无当”问题，呼唤领域定制架构。
- **清晰的可复现性**：详细说明了预处理步骤、模型结构、训练超参数，有利于后续研究复现。

## 8. 不足与局限

- **模型覆盖有限**：仅评估两个LBM（LaBraM、NeuroGPT），其他LBM（如NeuroLM、CBramod）未纳入。可能遗漏性能更优的模型。
- **任务覆盖不足**：仅5个分类任务，未包含回归（如连续脑电预测）、生成（如数据增强）、重构等LBM的潜在优势应用。
- **预训练数据重叠问题**：LaBraM和NeuroGPT的预训练数据包含运动、ERP、睡眠、眼睛等，但记忆任务未出现，导致性能差距（传统模型反而更好）。需要更多未见任务测试。
- **未比较其他PEFT方法**：只用了LoRA，未比较Adapter、Prefix Tuning、Prompt Tuning等，结论的普适性受限。
- **超参数选择粗糙**：所有模型固定20个epoch、学习率未知、LoRA缩放因子固定8、dropout概率固定0.5，未做充分调优。可能对某些模型不公平。
- **缺乏鲁棒性分析**：未探讨噪声、设备差异、受试者间变异等实际挑战。
- **计算资源未报告**：无法评估训练成本，不利于实际部署决策。
- **统计检验仅针对部分比较**：表2只比较了EEG-Inception与LBM，未比较EEGNet与LBM。
- **LoRA消融单一秩**：仅基于每个模型的最佳秩r'进行层组合消融，未验证其他秩下层组合是否同样有效。
- **未讨论模型容量与数据规模关系**：BCI数据量通常较小，过拟合风险高，论文未深入分析该问题。

（完）
