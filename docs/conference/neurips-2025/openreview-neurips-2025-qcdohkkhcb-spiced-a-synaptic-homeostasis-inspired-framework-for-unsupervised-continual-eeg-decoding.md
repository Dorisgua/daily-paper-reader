---
title: "SPICED: A Synaptic Homeostasis-Inspired Framework for Unsupervised Continual EEG Decoding"
title_zh: SPICED：一种受突触稳态启发的无监督持续EEG解码框架
authors: "Yangxuan Zhou, Sha Zhao, Jiquan Wang, Haiteng Jiang, Shijian Li, Tao Li, Gang Pan"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=qcdoHkkHcb"
tags: ["query:eeg"]
score: 6.0
evidence: 无监督持续EEG解码
tldr: 持续学习的EEG解码面临灾难性遗忘和个体差异问题。本文受突触稳态机制启发，提出SPICED框架，通过关键记忆重激活、动态网络扩展等生物启发机制，实现无监督的持续EEG解码。实验表明该方法能在持续接纳新受试者时保持良好性能，为自适应BCI提供了新范式。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-qcdohkkhcb/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1441, \"height\": 383, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-qcdohkkhcb/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1452, \"height\": 739, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-qcdohkkhcb/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1434, \"height\": 340, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-qcdohkkhcb/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1451, \"height\": 320, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-qcdohkkhcb/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1445, \"height\": 721, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-qcdohkkhcb/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1441, \"height\": 730, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-qcdohkkhcb/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1439, \"height\": 657, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-qcdohkkhcb/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1441, \"height\": 657, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-qcdohkkhcb/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1445, \"height\": 249, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-qcdohkkhcb/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1435, \"height\": 655, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-qcdohkkhcb/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1433, \"height\": 658, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-qcdohkkhcb/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1441, \"height\": 656, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-qcdohkkhcb/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1447, \"height\": 540, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-qcdohkkhcb/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1446, \"height\": 199, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-qcdohkkhcb/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1448, \"height\": 282, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-qcdohkkhcb/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1446, \"height\": 400, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-qcdohkkhcb/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 876, \"height\": 764, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-qcdohkkhcb/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 873, \"height\": 688, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-qcdohkkhcb/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1163, \"height\": 303, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-qcdohkkhcb/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 875, \"height\": 162, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-qcdohkkhcb/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1445, \"height\": 334, \"label\": \"Table\"}]"
motivation: 持续EEG解码面临灾难性遗忘和个体差异挑战。
method: 受突触稳态启发，构建包含关键记忆重激活和动态扩展的脉冲网络。
result: 在持续接纳新受试者时保持解码性能，缓解灾难性遗忘。
conclusion: 生物启发的持续学习方法可提升EEG解码的自适应能力。
---

## Abstract
Human brain achieves dynamic stability-plasticity balance through synaptic homeostasis, a self-regulatory mechanism that stabilizes critical memory traces while preserving optimal learning capacities. Inspired by this biological principle, we propose SPICED: a neuromorphic framework that integrates the synaptic homeostasis mechanism for unsupervised continual EEG decoding, particularly addressing practical scenarios where new individuals with inter-individual variability emerge continually. SPICED comprises a novel synaptic network that enables dynamic expansion during continual adaptation through three bio-inspired neural mechanisms: (1) critical memory reactivation, which mimics brain functional specificity, selectively activates task-relevant memories to facilitate adaptation; (2) synaptic consolidation, which strengthens these reactivated critical memory traces and enhances their replay prioritizations for further adaptations and (3) synaptic renormalization, which are periodically triggered to weaken global memory traces to preserve learning capacities. The interplay within synaptic homeostasis dynamically strengthens  task-discriminative memory traces and weakens detrimental memories. By integrating these mechanisms with continual learning system, SPICED preferentially replays task-discriminative memory traces that exhibit strong associations with newly emerging individuals, thereby achieving robust adaptations. Meanwhile, SPICED effectively mitigates catastrophic forgetting by suppressing the replay prioritization of detrimental memories during long-term continual learning. Validated on three EEG datasets, SPICED show its effectiveness. More importantly, SPICED bridges biological neural mechanisms and artificial intelligence through synaptic homeostasis, providing insights into the broader applicability of bio-inspired principles.

---

## 论文详细总结（自动生成）

# SPICED：受突触稳态启发的无监督持续脑电信号解码框架——论文总结

## 1. 核心问题与整体含义（研究动机和背景）

- **核心问题**：脑电（EEG）解码模型在实际部署中面临两个关键挑战：① 新个体不断出现且存在显著个体差异（inter-individual variability），模型需要具备**可塑性**以适应每个新个体；② 长期持续学习过程中，灾难性遗忘（catastrophic forgetting）导致旧知识被破坏，需要维持**稳定性**。
- **背景动机**：人脑通过**突触稳态**（synaptic homeostasis）机制动态平衡稳定性与可塑性——突触巩固（synaptic consolidation）稳定关键记忆痕迹，突触再归一化（synaptic renormalization）周期性弱化全局突触连接以保留学习能力。受此启发，论文提出生物启发的神经形态框架 SPICED，旨在解决无监督持续EEG解码（unsupervised continual EEG decoding）中的稳定性-可塑性困境。
- **整体含义**：SPICED 通过模拟突触稳态的巩固与再归一化相互作用，实现对新个体的鲁棒适应同时抑制灾难性遗忘，为脑机接口（BCI）在真实持续场景下的应用提供了生物启发式解决方案，并搭建了生物神经机制与人工智能之间的桥梁。

## 2. 方法论：核心思想、关键技术细节、算法流程

### 2.1 核心思想
- 将每个个体视为一个**突触节点**（synaptic node），构建一个**突触网络**（synaptic network），节点之间基于初始特征相似性建立突触连接并赋予初始强度。
- 当新个体到来时，动态扩展网络，通过**关键记忆激活**（critical memory reactivation）选择任务相关节点进行重放，并通过**突触巩固**增强这些节点的连接强度，通过**突触再归一化**周期性全局降低所有节点的连接强度。
- 巩固与再归一化的协同（突触稳态）实现：强化判别性记忆痕迹，弱化冗余噪声记忆，从而平衡稳定性与可塑性。

### 2.2 关键技术细节

#### (1) 初始特征提取与网络初始化
- 从每个个体的EEG信号中提取时域、频域、时频域三个维度的手工特征，计算加权余弦相似度：
  \[
  S(x_i, x_j) = \frac{\omega_t \cdot sim(x_t^i, x_t^j) + \omega_f \cdot sim(x_f^i, x_f^j) + \omega_{tf} \cdot sim(x_{tf}^i, x_{tf}^j)}{\omega_t + \omega_f + \omega_{tf}}
  \]
- 若相似度超过阈值 $\xi$，则建立突触连接，初始强度为1。

#### (2) 关键记忆激活（Critical Memory Reactivation）
- 对当前新个体节点 $N_i$，计算所有已有节点 $N_j$ 的重要性系数：
  \[
  I(N_i, N_j) = \alpha \cdot S(x_i, x_j) + (1-\alpha) \cdot \bar{s}_j
  \]
  其中 $\bar{s}_j$ 是节点 $j$ 的平均连接强度，$\alpha$ 为权重。
- 选取 Top-K 个重要节点，将其样本（含伪标签）用于加权重放，同时利用这些节点的模型参数通过加权融合初始化当前个体的模型 $M_i$：
  \[
  M_i = \sum_{j=1}^K \frac{I(N_i, N_j)}{\sum_{k=1}^K I(N_i, N_k)} M_j
  \]
- 克隆指导模型进行自监督学习（CPC）生成高置信度伪标签，再与重放样本联合训练。

#### (3) 突触巩固（Synaptic Consolidation）
- 完成个体适应后，对 Top-K 激活节点的连接强度进行增强：
  \[
  s'_{ij} = \gamma \cdot s_{ij}, \quad \gamma > 1
  \]
- 设置强度上限为3（基线为1），模拟生物突触饱和。

#### (4) 突触再归一化（Synaptic Renormalization）
- 在每个个体适应后，所有节点的连接强度按 Ebbinghaus 遗忘曲线衰减：
  \[
  s''_{ij} = e^{-t_i / \lambda} \cdot s'_{ij}
  \]
  其中 $t_i$ 是自上次激活后的步数，$\lambda$ 为衰减因子。
- 被巩固的节点重置 $t_i = 1$，从而保留重要知识。

### 2.3 算法流程（伪代码描述）
1. **初始化**：在源域上预训练模型，构建突触网络（存储初始特征、样本、模型及连接）。
2. **循环处理每个新个体**：
   - 创建新节点，计算与所有已有节点的相似度，若超过 $\xi$ 则建立连接。
   - 计算重要性系数，选取 Top-K 节点。
   - 加权重放 Top-K 节点的样本。
   - 加权融合 Top-K 节点的模型得到 $M_i$。
   - 自监督学习生成伪标签，联合训练 $M_i$。
   - 存储伪标签样本和模型到新节点。
   - 突触巩固：增强 Top-K 节点的连接强度。
   - 突触再归一化：全局衰减所有连接强度，增加未激活节点的步数 $t$。

## 3. 实验设计

### 3.1 数据集与场景
- 三个主流EEG任务数据集（均含≥100个受试者，适合长期持续学习评估）：
  1. **ISRUC**（睡眠分期）：100人，200Hz，6个EEG+2个EOG通道，30秒epoch，5类，共89,240个样本。
  2. **FACED**（情绪识别）：123人，250Hz，32通道，10秒epoch，9类，共10,332个样本。
  3. **Physionet-MI**（运动想象）：109人，160Hz，64通道，4秒epoch，4类，共9,837个样本。
- **场景**：无监督持续学习（UICL paradigm）——源域（已知个体）上有标签，目标域（新个体）无标签且逐个连续到来。

### 3.2 基准与对比方法
- 采用不同的源域-目标域划分比例（源域占10%~50%），并随机打乱目标域个体顺序进行5次重复以统计标准差。
- 对比方法：
  - **MMD**（无监督域自适应）
  - **EWC**（正则化持续学习）
  - **UCL-GV**（对比对齐持续域适应）
  - **ReSNT**（动态记忆演化EEG持续解码）
  - **CoUDA**（持续无监督域适应）
  - **BrainUICL**（无监督持续EEG解码框架）
- 评估指标：准确率（ACC）和宏F1（Macro-F1），分别报告初始源模型 $M_0$ 和适应后模型 $M_i$ 的性能。

### 3.3 实验充分性
- 共进行了约**15组主要对比实验**（三个数据集×五种源域比例），每组含5次随机顺序重复，表2展示了平均性能与标准差。
- 超参数分析（$\lambda$ 和 $\gamma$ 的相互作用，图4；$\alpha$ 分析，图9）。
- 连接阈值 $\xi$ 的敏感性分析（附录F，表6）。
- 消融实验（去除巩固或再归一化，图13）。
- 鲁棒性实验（添加不同比例高斯噪声，表8）。
- 计算成本分析（附录J，表7）。
- 突触网络扩展过程可视化（附录H）。

**公平性**：所有方法在同一数据划分和随机顺序下评估，报告了5次重复均值和标准差。

## 4. 资源与算力

- 硬件配置：单台服务器，**Intel Core i9-10900K CPU**，**8×NVIDIA RTX 3080 GPU**。
- 平均每个个体适应时间：约 **4.2~4.4 分钟**（ISRUC 4.42±0.55，FACED 4.16±0.64，Physionet-MI 4.23±0.63）。
- 存储开销：每个个体约 **43~53 MB**（模型+重放样本）。
- 论文未明确报告完整实验（如所有数据划分、所有对比方法）的总GPU小时数，但给出了单次适应的时间，可推算总时长。

## 5. 实验数量与充分性

- 实验覆盖三个不同任务（睡眠、情绪、运动想象），每个任务使用100+受试者，且采用不同的源域比例（10%~50%），验证了框架在少样本预训练下的长期持续学习能力。
- 对比了6种现有方法（含域自适应和持续学习），并进行了消融研究。
- 超参数分析包括退化因子 $\lambda$、巩固系数 $\gamma$、相似度重要性权重 $\alpha$、连接阈值 $\xi$ 等。
- 鲁棒性实验考虑了噪声干扰。
- 多次随机顺序重复以评估统计稳定性。
- **充分性评价**：实验设计较为全面，涵盖了主流EEG任务、多方法对比、关键参数分析和消融验证，结果具有统计意义。但缺少对更大规模预训练或跨数据集迁移的测试。

## 6. 主要结论与发现

- SPICED 在所有三个数据集上均显著优于对比方法，且在不同源域比例下表现出稳定提升（ACC 提升2~12个百分点，MF1 提升3~18个百分点）。
- 突触巩固与再归一化的协同（即突触稳态）是核心——消融实验证明二者缺一不可。
- 突触网络的可视化显示：关键节点（连接密集、强度高）在持续学习中被反复巩固，而边缘节点被再归一化抑制，符合生物机制。
- 超参数分析表明，适中的 $\lambda$（约30）和 $\gamma$（约1.3）可实现最佳平衡。
- 方法对噪声输入具有鲁棒性（10%高斯噪声下性能几乎不变）。

## 7. 优点（亮点）

1. **生物启发性**：首次系统地将突触稳态的巩固与再归一化机制引入无监督持续EEG解码，理论新颖且机制完整。
2. **模型结构独立性**：突触网络作为辅助组件，不干扰主模型架构，易于集成。
3. **无监督适应性**：仅需无标签的新个体EEG数据，利用自监督学习和伪标签，符合实际部署需求。
4. **鲁棒性**：通过全局再归一化抑制噪声累积，缓解灾难性遗忘，且对输入噪声不敏感。
5. **实证充分**：在三个不同任务、多种源域比例、多种对比方法下验证了有效性，消融和参数分析详尽。
6. **计算开销可控**：每个个体适应仅需数分钟，存储合理。

## 8. 不足与局限

1. **生物机制建模的简化**：仅模拟了突触稳态的宏观原则，未涉及更深层的神经生物学细节（如LTP/LTD分子机制），是一种近似。
2. **初始特征固定**：所有任务使用统一的手工特征提取方案（时域、频域、时频域），未考虑任务间的特征差异，可能限制相似性度量的准确性。
3. **连接阈值依赖人工设定**：三个数据集使用不同的 $\xi$，需要针对每项任务调参，通用性受限；未探索自适应阈值策略。
4. **实验范围有限**：仅测试了两个源域比例范围（10%~50%），未探索更少或更多源域的情况；未进行跨数据集或真实临床场景的测试。
5. **大规模预训练未涉及**：虽使用CNN+Transformer架构，但预训练仅基于当前数据集，未利用大型公开EEG数据集进行预训练以进一步提升泛化性。
6. **伪标签质量依赖阈值**：伪标签置信度阈值 $\eta$ 设为0.9，在低信噪比数据上可能产生偏差。
7. **缺乏理论收敛性分析**：论文未提供突触巩固与再归一化动态平衡的理论保证，主要依赖实验验证。

（完）
