---
title: "The Brain's Bitter Lesson: Scaling Speech Decoding With Self-Supervised Learning"
title_zh: 大脑的痛苦教训：用自监督学习扩展语音解码
authors: "Dulhan Jayalath, Gilad Landau, Brendan Shillingford, Mark Woolrich, Oiwi Parker Jones"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=pFqUNiwC7Z"
tags: ["query:eeg"]
score: 7.0
evidence: 使用自监督学习从MEG脑活动解码语音，类似EEG脑机接口
tldr: 基于个体差异和数据集异构性，脑活动解码难以跨被试泛化。本文提出神经科学启发的自监督学习架构，在400小时MEG数据和900名被试上训练，实现了跨被试、跨数据集和跨任务的语音解码。其结果比以往方法有显著提升，且首次在MEG上展示了大规模预训练的有效性。该工作的自监督预训练范式可直接指导EEG脑机接口信号处理。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-pfquniwc7z/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 756, \"height\": 507, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-pfquniwc7z/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1326, \"height\": 526, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-pfquniwc7z/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1576, \"height\": 577, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-pfquniwc7z/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1559, \"height\": 577, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-pfquniwc7z/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 858, \"height\": 1099, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-pfquniwc7z/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 876, \"height\": 720, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-pfquniwc7z/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 761, \"height\": 237, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-pfquniwc7z/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1094, \"height\": 894, \"label\": \"Table\"}]"
motivation: 脑活动解码因个体差异和数据异构性难以跨被试泛化。
method: 提出神经科学启发的自监督学习架构和模型，在大规模MEG数据上预训练。
result: 在900名被试上实现了跨被试、跨数据集和跨任务的语音解码，性能大幅提升。
conclusion: 展示了大规模自监督学习在脑信号处理中的潜力，为EEG脑机接口提供了新范式。
---

## Abstract
The past few years have seen remarkable progress in the decoding of speech from brain activity, primarily driven by large single-subject datasets. However, due to individual variation, such as anatomy, and differences in task design and scanning hardware, leveraging data across subjects and datasets remains challenging. In turn, the field has not benefited from the growing number of open neural data repositories to exploit large-scale deep learning. To address this, we develop neuroscience-informed self-supervised objectives, together with an architecture, for learning from heterogeneous brain recordings. Scaling to nearly **400 hours** of MEG data and **900 subjects**, our approach shows generalisation across participants, datasets, tasks, and even to *novel* subjects. It achieves **improvements of 15-27%** over state-of-the-art models and **matches *surgical* decoding performance with *non-invasive* data**. These advances unlock the potential for scaling speech decoding models beyond the current frontier.

---

## 论文详细总结（自动生成）

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：语音解码（从脑活动中解码语音）严重受限于无法跨被试、跨数据集和跨任务泛化。主要原因包括个体大脑解剖差异、任务设计不同、扫描硬件异构等。这使得该领域无法像AI其他领域一样通过扩大数据规模和计算量来持续提升性能（即“苦涩教训”未得到应用）。
- **整体含义**：论文探索了自监督学习（SSL）在MEG脑活动解码中的应用，提出神经科学启发的预训练任务和网络架构，使模型能够从大量无标签、跨被试、跨数据集的脑信号中学习通用表征，从而显著提升下游语音解码任务性能，并首次在非侵入性MEG上实现与侵入性手术级的解码效果匹配。

## 2. 论文提出的方法论：核心思想、关键技术细节、公式或算法流程

- **核心思想**：利用无标签MEG数据的丰裕性，设计三类基于神经科学原理的自监督前文本任务（pretext tasks），训练一个编码器学习通用的脑信号表征；然后在冻结编码器的情况下，用少量有标签数据训练线性分类器进行语音检测和发声分类。
- **关键技术细节**：
  - **网络架构**：包含一个“皮层编码器”（cortex encoder），基于SEANet（卷积神经网络），类似神经音频编解码器。支持异构数据集：通过`dataset-conditional linear layer`将不同数量传感器投影到统一维度（`d_shared=512`）。引入`subject conditioning`（特征线性调制，FiLM）处理个体差异。预训练后，使用线性分类器/线性探针进行微调，编码器冻结。
  - **三类前文本任务**：
    1. **频段预测（Band prediction）**：对输入信号随机应用一个带阻滤波器（去除某一功能频段，如δ、θ、α、β、γ、γ_high_lower、γ_high_upper），让网络预测哪个频段被滤除。损失为交叉熵。
    2. **相位偏移预测（Phase shift prediction）**：随机选择0-50%的传感器，施加离散的相位偏移（8种之一），让网络预测偏移量。损失为交叉熵。
    3. **幅度缩放预测（Amplitude scale prediction）**：随机选择0-50%的传感器，施加离散的幅度缩放因子（16种，范围[-2,2]），让网络预测缩放系数。损失为交叉熵。
  - **组合损失**：`L_SSL = w1*L_band + w2*L_phase + w3*L_amplitude`，权重均为1.0。
  - **预训练-微调流程**：先用无标签数据预训练整个模型（包括编码器和三个预测头），然后冻结编码器，在少量有标签数据上训练新的线性分类器（语音检测或发声分类）。

## 3. 实验设计：数据集、场景、基准和对比方法

- **数据集**：
  - **预训练数据**：Cam-CAN（641名被试，约160小时，包括静息和感觉运动任务）为主；MOUS（204名被试，约160小时，视觉和听觉任务）；两者合并共约320小时。总计约400小时、近900名被试（含下游）。
  - **下游有标签数据**：
    - Armeni et al. (2022)：3名被试，每人10小时听故事录音（共30小时）。
    - Gwilliams et al. (2023)：27名被试，每人2小时（共54小时），无头套固定，噪声大，用于测试新被试泛化。
  - **任务**：语音检测（Speech detection，二分类：语音是否存在）和发声分类（Voicing classification，按音素始发判断是否浊音）。
- **基准方法**：
  - 随机选择（AUC=0.5）
  - 线性模型直接使用MEG信号
  - 无预训练（随机初始化编码器）
  - 独立使用单一前文本任务（相位、幅度、频段）
  - 未使用任何前文本任务
  - 对比的SOTA自监督方法：
    - BrainBERT（基于掩码头图谱填充，原用于颅内记录）
    - BIOT（跨数据生物信号变换器，预训练在EEG上）
    - EEGPT（预训练变压器，用于EEG）
  - 手术级结果：引用Wang et al. (2023)使用颅内数据的结果。
- **评估指标**：ROC AUC（受试者工作特征曲线下面积），随机水平0.5。报告早期停止时的测试AUC，并给出超过5个种子的标准误。

## 4. 资源与算力

文中附录C明确给出：
- **硬件**：NVIDIA V100和A100 GPU，最多40 GiB GPU显存，系统RAM最多1 TiB。
- **训练时长**：单次预训练（最大数据量）约200小时（8.3天），微调另需最多12小时。
- **总算力**：最终实验（含超参数搜索）约3000小时GPU计算；整个项目从构思到成文约10,000小时GPU计算。
- 所有实验在牛津大学高级研究计算（ARC）设施进行。

## 5. 实验数量与充分性

- **实验组数**：论文包含多组系统实验：
  - 基准对比（表2，11组/行）
  - 消融实验：单独前文本任务（3、4、5）与组合（6）
  - 与SOTA方法对比（C部分，4种方法）
  - 数据规模扩展（图3，两个任务+两个数据集，共4条曲线）
  - 新被试泛化实验（图4，同样4条曲线）
  - 数据集聚合实验（表3，3行）
  - 超参数搜索（附录B，对ρ等参数进行搜索）
- **充分性与公平性**：
  - 每实验使用多种子（最多5个）报告均值和标准误，较为严谨。
  - 与BrainBERT对比时因计算限制缩小了数据规模，但明确说明，并保证公平（使用相同架构调整）。
  - 与新基线（BIOT、EEGPT）比较使用了对方公开的预训练权重，未见不公平偏倚。
  - 数据集划分明确：验证集和测试集严格分离，新被试泛化实验单独留出3名被试。
  - 结论有统计显著性检验（单侧t检验，p<0.05）。
  - 总体实验覆盖了主要变量（数据量、被试泛化、数据集聚合、不同任务），消融充分，结论可信。

## 6. 论文的主要结论与发现

- 提出的自监督方法（组合三类神经科学启发的前文本任务）在语音检测任务上**比当前最佳自监督模型（BrainBERT、BIOT、EEGPT）提升15-27%**（表2C）。
- **首次在非侵入性MEG上匹配侵入性手术级解码性能**（AUC 0.705 vs 0.71±0.06，表2行12）。
- 预训练数据量增加时，下游性能呈现**对数或对数-线性可扩展性**（Figure 3），尚未饱和，表明可通过继续增大数据获得持续收益。
- 预训练模型**可跨数据集泛化**（Cam-CAN无语言任务→Armeni/Gwilliams有语言任务；不同扫描仪）；且**可泛化到从未见过的新被试**（Figure 4，正向对数-线性趋势），这在MEG语音解码中是首次。
- **聚合多个未标记数据集（Cam-CAN + MOUS，共320小时）可进一步提升性能**（表3，AUC从0.630提升至0.638），且优于单独使用任何一个数据集。
- 使用无语言内容的预训练数据（Cam-CAN只有静息/运动任务）就能显著提升语言语音解码任务，说明前文本任务**捕获了通用神经特征**。

## 7. 优点：方法或实验设计上的亮点

- **创新性**：首次将神经科学的功能频带、相位耦合和幅度差异知识融入自监督前文本任务，实现更有效的表征学习。
- **架构设计**：引入了数据集条件层和主题条件层，统一异构数据；卷积编码器借鉴音频编解码，适应多通道脑信号。
- **大规模验证**：使用了近400小时MEG数据、900名被试，是此前MEG工作数据量的约5倍，验证了数据扩展的可行性。
- **泛化能力**：不仅跨被试、跨数据集，还跨任务（从非语言任务预训练到语音任务微调），并且**实现了新被试的零样本泛化**，对脑机接口（BCI）实际部署意义重大。
- **公平比较**：与三种不同的自监督基线（BrainBERT、BIOT、EEGPT）进行了直接对比，并包含了多种消融。
- **透明度**：明确报告了算力消耗、超参数、数据集划分，重视实验可重复性。

## 8. 不足与局限

- **任务覆盖有限**：只进行了语音检测和发声分类两个下游任务，未能实现完整的“脑信号到文本”（brain-to-text）解码，这是最终目标。
- **未覆盖所有语音类型**：仅研究了“听到的语音”（heard speech），未包括“想象语音”或“尝试说话”的语音，虽然作者假设方法可泛化但未验证。
- **未充分利用空间信息**：MEG传感器位置与脑区强相关，但论文未显式利用传感器几何空间特征。
- **前文本任务非穷尽**：作者承认可能还有其他更有用的前文本任务（如空间特征等）未被探索。
- **数据质量影响未深究**：MOUS数据集比Cam-CAN更嘈杂（相同扫描仪但任务含语音），其性能反而更低，说明数据质量对预训练有显著影响，但未系统分析。
- **计算资源需求较高**：单次预训练达200小时，总体算力约1万GPU小时，对资源有限团队不够友好。
- **实验外推性**：尽管展示了扩展趋势，但最大数据量仅320小时，更大量级的（例如数千小时）是否继续提升仍未确定。
- **风险讨论中**：虽然限制只解码听到的语音以减少隐私风险，但随着技术进步，对内心语音的潜在解码仍可能带来伦理风险。

（完）
