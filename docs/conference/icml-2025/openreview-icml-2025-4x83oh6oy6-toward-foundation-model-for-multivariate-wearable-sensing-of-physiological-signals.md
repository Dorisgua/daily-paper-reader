---
title: Toward Foundation Model for Multivariate Wearable Sensing of Physiological Signals
title_zh: 迈向多变量可穿戴生理信号感知的基础模型
authors: "Yunfei Luo, Yuliang Chen, Asif Salekin, Tauhidur Rahman"
date: 2025-01-23
pdf: "https://openreview.net/pdf?id=4x83oH6Oy6"
tags: ["query:eeg"]
score: 4.0
evidence: 基础模型在EEG等信号上预训练，可用于EEG表示学习
tldr: 可穿戴感知数据因模式和频带变化难以学习通用表示。本文提出NormWear，在PPG、ECG、EEG等多样生理信号上预训练的基础模型，能够提取可迁移的波形表示。评估表明其在多任务上表现优异，为EEG信号处理与分析提供了通用工具。
source: ICML-2025-Rejected-Public
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-4x83oh6oy6/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1675, \"height\": 769, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4x83oh6oy6/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1689, \"height\": 945, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4x83oh6oy6/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1695, \"height\": 623, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4x83oh6oy6/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1658, \"height\": 445, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4x83oh6oy6/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1610, \"height\": 811, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4x83oh6oy6/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1626, \"height\": 1260, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4x83oh6oy6/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 972, \"height\": 238, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4x83oh6oy6/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 746, \"height\": 735, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4x83oh6oy6/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1758, \"height\": 555, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4x83oh6oy6/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1681, \"height\": 1006, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4x83oh6oy6/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1394, \"height\": 754, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4x83oh6oy6/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1379, \"height\": 752, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4x83oh6oy6/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1391, \"height\": 763, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4x83oh6oy6/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1890, \"height\": 2192, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-4x83oh6oy6/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1891, \"height\": 2181, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-4x83oh6oy6/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 918, \"height\": 940, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-4x83oh6oy6/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 730, \"height\": 991, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-4x83oh6oy6/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1677, \"height\": 1235, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-4x83oh6oy6/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1688, \"height\": 590, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-4x83oh6oy6/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 821, \"height\": 785, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-4x83oh6oy6/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1724, \"height\": 1297, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-4x83oh6oy6/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 456, \"height\": 405, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-4x83oh6oy6/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1730, \"height\": 1149, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-4x83oh6oy6/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1739, \"height\": 1153, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-4x83oh6oy6/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1762, \"height\": 435, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-4x83oh6oy6/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1762, \"height\": 578, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-4x83oh6oy6/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1725, \"height\": 1284, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-4x83oh6oy6/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 763, \"height\": 301, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-4x83oh6oy6/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1216, \"height\": 370, \"label\": \"Table\"}]"
motivation: 可穿戴感知数据异构性强，缺乏通用表示。
method: 提出在多模态生理信号上预训练的基础模型NormWear。
result: 在多种评估任务上表现良好，表示可迁移。
conclusion: NormWear可作为EEG信号分析的基础特征提取器。
---

## Abstract
Time-series foundation models excel at tasks like forecasting across diverse data types by leveraging informative waveform representations. Wearable sensing data, however, pose unique challenges due to their variability in patterns and frequency bands, especially for healthcare-related outcomes. The main obstacle lies in crafting generalizable representations that adapt efficiently across heterogeneous sensing configurations and applications. To address this, we propose NormWear, a foundation model designed to extract generalized and informative representations from wearable sensing data. NormWear is pretrained on a diverse set of physiological signals, including PPG, ECG, EEG, GSR, and IMU, from various public datasets. For evaluation, we benchmark its performance across 11 public wearable sensing datasets, spanning 18 applications in mental health, body state inference, biomarker estimation, and disease risk evaluation, demonstrating superior performance compared to competitive baselines. Additionally, using a novel representation-alignment-match method, we align physiological signal embeddings with text embeddings, enabling zero-shot inference for unseen wearable signal-based health applications.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 核心问题与整体含义（研究动机和背景）

- **问题**：可穿戴生理信号（PPG、ECG、EEG、GSR、IMU等）在模式、频带、采样率等方面高度异构，现有时间序列基础模型（如Chronos、TF-C、CLAP）要么依赖固定的传感器类型（对比学习），要么只能处理单变量序列，无法有效捕捉多变量、多通道之间的复杂关系，也缺乏统一的预处理管道，导致在可穿戴健康监测场景下泛化能力不足。
- **意义**：需要一种能够处理任意数量、任意类型的多变量生理信号的基础模型，以提取通用且信息丰富的表征，服务于心理健康、身体状态推断、生命体征估计、疾病风险评估等多种下游任务，并实现零样本推理。

## 2. 方法论

### 核心思想
提出 **NormWear**，基于掩码自编码器（MAE）框架，采用**连续小波变换（CWT）** 将多通道时间序列转换为RGB-like图谱，并用Vision Transformer（ViT）架构进行预训练，同时引入通道感知融合机制处理任意输入通道数。此外，设计了记忆流启发的时序融合模块（MSiTF），将生理信号嵌入与文本嵌入对齐，实现零样本推理。

### 关键技术细节

- **分词化（Tokenization）**：
  - 对每个单变量信号计算一阶和二阶导数，与原始信号一起分别计算CWT（使用Mexican Hat小波，尺度1~64），得到三张标量图（scalogram），堆叠为RGB-like图像（3通道）。
  - 将标量图划分为不重叠的patch（核大小9×5，步长9×5），每个patch作为token，通过卷积层投影到768维embedding。

- **模型架构与预训练策略**：
  - 编码器：12个标准Transformer块，每两个块后插入一个**通道感知融合层**，共6个融合层。
  - 融合策略：采用**[CLS]-Attention**——从每个通道取出[CLS] token堆叠后做自注意力，融合后的[CLS]再放回原通道。该方法兼顾跨通道信息与计算效率。
  - 掩码策略：在频率轴和时间轴上独立进行结构化掩码（时间掩码率0.6，频率掩码率0.5），总体掩码率约80%。
  - 轻量解码器：2个Transformer块 + 2个Conv1D层，重建成原始时间序列，损失为MSE。

- **零样本推理（MSiTF模块）**：
  - 针对人体感知的三个挑战：信号与任务的相关性、生理信号的时间动态性（近期更相关）、弱标签与稀疏有效段。
  - **相关性分数**：查询文本嵌入与每个时间步patch嵌入的交叉注意力。
  - **新近分数**：指数衰减函数，越近权重越高。
  - **重要性分数**：可学习的二值门控（Gumbel-Softmax），决定每个patch是否保留。
  - 三者加权求和得到每个patch的聚合权重，最终得到固定长度嵌入（768维），再通过VAE风格采样引入随机性。
  - **对齐器**：冻结的文本编码器（TinyLlama）将标签转为句子嵌入，与信号嵌入比较，损失函数结合曼哈顿距离和余弦相似度（式2）。
  - 预训练时用GPT-3.5对句子进行数据增强（每个标签生成20种变体）。

## 3. 实验设计

### 数据集

- **预训练**：9个公开数据集（Cuff-Less-BP、PPG-DaLiA、Auditory-EEG、PhyAAt、MAUS、Mendeley-YAAD、Brain-Cognitive、EPHNOGRAM、BIDMC），共230,962段（385小时），通过启发式数据增强（时间序列混洗）扩展到2,576,418段（4,294小时）。包含PPG、ECG、EEG、GSR、PCG、IMU。
- **下游评估**：11个未见过的公开数据集（WESAD、UCI-HAR、DriverFatigue、Epilepsy、GAMEEMO、ECG-Abnormal、PPG-BP、PhysioNet EMG、Noninvasive-BP、PPG-Hgb、Fetal-fPCG），涵盖18个任务，分四类：活动识别、EEG主任务（癫痫状态/情绪）、疾病风险评估（高血压/糖尿病/心脏病/肌肉疾病）、生命体征估计。

### 基准方法

- **统计方法**：手工提取时域和频域特征（均值、标准差、偏度、峰度、频率质心等）。
- **TF-C**：时间序列自监督SoTA，同时建模时域和频域。
- **CLAP**：基于频谱的音频建模SoTA（将信号转为频谱图）。
- **Chronos**：基于LLM的时序预测SoTA。

### 评估方式

- **线性探测（Linear Probing）**：冻结NormWear编码器，用逻辑回归（分类）或岭回归（回归）在下游训练集上微调，报告AUC ROC、相对准确率等。数据按训练/测试8:2分层划分（以subject ID分层）。
- **零样本**：直接用MSiTF对齐模块进行标签检索（最近邻句子），报告AUC ROC。

## 4. 资源与算力

- **论文中未明确说明预训练使用的GPU型号、数量和总训练时长**。
- 附录A提到：预训练45,000步，batch size 256，优化器AdamW，学习率1e-3。
- 附录E（表13）给出了单次推理的硬件需求：NVIDIA RTX 3090推断时间0.18秒，VRAM 732.82 MB；Jetson Nano 4GB GPU推断34.87秒。
- 消融实验在较小的子集（37k样本）上进行。

## 5. 实验数量与充分性

- **实验量**：线性探测覆盖18个下游任务；零样本覆盖15个任务；消融实验包括：融合策略（4种）、掩码策略（4种）、输入表示（CWT vs 原始序列）、预训练数据规模缩放（从37k到2.5M）、重要性分数和文本增强的消融、人口统计学信息合并分析、统计显著性检验（排列检验、Friedman检验、Conover后验、CD图）。
- **充分性**：覆盖了多种传感器类型和任务领域，基准方法多样（统计、自监督、频谱、LLM），消融实验系统。但零样本部分仅对比了CLAP（两个版本），缺少与其他对齐方法的比较。整体实验设计较为充分、客观（报告了多次运行与统计检验）。
- **公平性**：所有方法使用相同预处理（统一65Hz，6秒窗口），线性探测统一训练方式，确保公平。

## 6. 主要结论与发现

- **NormWear在所有任务组上均达到最佳性能**：宏平均AUC ROC较TF-C提升3.9%，较CLAP提升5.3%，较Chronos提升6.1%，较统计基线提升5.2%。
- **零样本能力**：NormWear+MSiTF在所有下游任务上优于CLAP（微平均59.9% vs 50.4%/51.7%），验证了对齐模块的有效性。
- **缩放定律**：随着预训练数据量从37k增加到2.5M，下游性能持续提升，说明模型具有可扩展性。
- **模型对信号类型敏感**：t-SNE显示同类传感器嵌入聚集，跨类分离。
- **可部署性**：可在Jetson Nano上运行（GPU推理35秒），具备边缘部署潜力。

## 7. 优点

- **方法论创新**：
  - CWT多尺度标量图作为通用分词化方式，无需传感器特定预处理。
  - 通道感知[CLS]-Attention融合，平衡计算效率与跨通道建模。
  - 首次实现可穿戴信号的零样本推理，MSiTF模块针对人体感知设计的三个分数（相关性、新近、重要性）具有实际意义。
- **实验覆盖广泛**：18个多样化下游任务，对比4种代表性基线，统计检验充分。
- **开源**：代码、数据、模型权重公开，可重复。
- **可解释性探索**：通过非线性动力学分析（Lyapunov指数、Hurst指数、持久熵）揭示各层特征变化规律；t-SNE可视化展示类间分离。

## 8. 不足与局限

- **零样本基线薄弱**：仅与CLAP对比，缺少与更通用的多模态对齐方法（如CLIP-style）或直接微调方法的对比。
- **计算资源信息不完整**：未说明预训练的总算力消耗（GPU数量、时长），不利于社区复现和公平比较。
- **数据预处理固定**：统一重采样至65 Hz，可能丢失高频（如EMG、部分EEG gamma波）信息；6秒窗口长度可能不适用于某些事件检测。
- **数据集局限**：预训练和下游数据均来自公开数据集，样本量有限（如生命体征估计任务仅有240段），且可能存在偏差（如受试者群体单一）。
- **未在真实临床环境验证**：所有任务均为公开基准，实际部署中的噪声、缺失、设备差异等未考虑。
- **可解释性深度不足**：仅通过t-SNE和混沌理论分析，未提供归因或注意力可视化，无法准确判断模型决策依据。
- **与其他基础模型的直接比较有限**：未对比近年其他生理信号基础模型（如Abbaspourazad等的工作），因为作者声称其“依赖固定传感器类型”而未纳入。
- **消融实验在子集上进行**：由于计算限制，消融仅在37k样本子集上完成，结果可能不完全反映完整数据上的行为。

（完）
