---
title: Joint Modeling of fMRI and EEG Imaging Using Ordinary Differential Equation-Based Hypergraph Neural Networks
title_zh: 使用常微分方程超图神经网络联合建模fMRI和EEG成像
authors: "YanZhang, Yang Gao, Min Li"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=qJLPlZSdkb"
tags: ["query:eeg"]
score: 4.0
evidence: 联合建模EEG和fMRI，EEG信号分析
tldr: 针对同步fMRI-EEG数据稀少且模态差异大的问题，提出基于ODE的超图神经网络框架，同时建模血流动力学和神经振荡，实现跨模态联合表征。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-qjlplzsdkb/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1426, \"height\": 638, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-qjlplzsdkb/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1428, \"height\": 577, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-qjlplzsdkb/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1439, \"height\": 284, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-qjlplzsdkb/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1444, \"height\": 678, \"label\": \"Table\"}]"
motivation: 联合建模fMRI和EEG面临数据少和模态差异大，现有图方法忽略ROI之间多对多关系。
method: 提出基于常微分方程的超图神经网络，捕获fMRI与EEG的复杂关联。
result: 在联合建模任务上优于现有图方法。
conclusion: 超图ODE能有效融合fMRI和EEG，提升多模态脑成像分析效果。
---

## Abstract
Fusing multimodal brain imaging has been a hot topic since different modalities of brain imaging can provide complementary information. However, due to the size of simultaneous recorded fMRI-EEG dataset being limited and the substantial discrepancy between hemodynamic responses of fMRI and neural oscillations of EEG, the joint modeling of fMRI and EEG images is a rarely explored area and has not yielded satisfactory results. Existing studies have also indicated that the relationships between region of interest (ROI) are not one-to-one when synchronizing fMRI and EEG. Current graph-based multimodal modeling methods overlook those information. Based on this, we propose a hypergraph based fMRI-EEG modeling framework for asynchronous fMRI-EEG data named FE-NET. To the best of our knowledge, this is the first attempt to jointly model asynchronous EEG and fMRI data as Neural ODEs based hypergraph. Extensive experiments have demonstrated that the proposed FE-NET outperforms many state-of-the-art brain imaging modeling methods. Meanwhile, compared to simultaneously recorded fMRI-EEG data, asynchronously acquired fMRI-EEG data is less costly, which demonstrates the practical applicability of our method.

---

## 论文详细总结（自动生成）

# 论文中文总结

## 1. 核心问题与整体含义（研究动机和背景）

- **研究背景**：多模态脑成像融合是神经科学研究的热点，fMRI通过BOLD信号间接测量脑活动，EEG通过电信号直接记录神经振荡。两者结合有望弥合血流动力学响应与神经振荡之间的鸿沟，提供更全面的脑功能理解。
- **核心挑战**：
  - 同步记录的fMRI-EEG数据集规模非常有限（成本高、设备不兼容），现有研究可靠性受限。
  - fMRI（秒级）与EEG（毫秒级）的时间尺度差异巨大，数据分布高度复杂。
  - 已有研究指出，fMRI和EEG的感兴趣区域（ROI）之间并非一一对应关系，而现有基于简单图的多模态建模方法忽略了这种高阶关系。
- **整体目标**：提出一种基于超图（hypergraph）和神经常微分方程（Neural ODE）的框架FE-NET，用于异步采集的fMRI-EEG数据的联合建模，首次尝试将异步EEG和fMRI数据建模为基于Neural ODE的超图。

## 2. 方法论

### 核心思想
- **超图建模**：利用超边（hyperedge）连接多个节点，捕捉fMRI与EEG之间复杂的多对多关系，克服简单图的一对一局限。
- **GAN生成超图**：设计了一个基于GAN的fMRI-EEG超图生成模块（FEH），包括最优fMRI-EEG同构算法（OFEI）和交互式超边神经元（IHEN），以学习两种模态的联合分布，缩小模态差距。
- **动态超图嵌入**：设计了一个基于Neural ODE的动态fMRI-EEG超图嵌入模块（FED），通过微分方程学习时序依赖，自然处理不一致的采样率和时间不同步问题。

### 关键技术细节
1. **FEH模块**：
   - **OFEI算法**：计算一个与所有样本初始超图“最优同构”的超图G*，最大化Jaccard相似度均值，保证拓扑一致性。
   - **IHEN生成器**：通过多层交互式超边神经元交替更新节点和超边表示，生成多模态连接张量Mk和节点相关分数。
   - **判别器**：基于随机游走的路径概率，对抗训练生成器，使生成的超图分布逼近真实功能连接矩阵分布。
   - 损失函数包括生成器和判别器对抗损失。

2. **FED模块**：
   - **动态超图系统定义**：将节点和超边特征视为时间的函数，由ODE控制其演化。
   - **控制-扩散分解**：采用Lie-Trotter分裂，将系统分为控制步（提取时空信息，使用DSCF模块：全连接层+LSTM+注意力）和扩散步（通过超图结构传播信息，使用扩散矩阵A）。
   - 控制步独立更新fMRI和EEG特征，扩散步实现跨模态信息交互。

3. **整体流程**：先由FEH生成多个时空尺度的超图，再输入FED进行动态嵌入和下游分类。

## 3. 实验设计

### 数据集与场景
- **主要数据集**：LEMON（开源，含227名健康被试，分青年组和老年组）。包括静息态fMRI和62通道EEG，以及多项认知行为测试（TAP持续注意力、TMT认知灵活性、WST言语智商、LPS-2逻辑智商）。任务：将被试按测试成绩分为高分组和低分组，进行二分类。
- **辅助数据集**：CN-EPFL（20人同步记录fMRI-EEG数据集），用于泛化能力评估。

### 数据预处理
- fMRI使用Nipype流程，EEG使用EEGLAB进行PCA降维等。

### 对比方法
- 单人模态方法：BrainGNN、M-GAT-BC、SGP-SL。
- 多模态方法：Cross-GNN、TAN、RH-BrainFS、MCRLN、MMP-GCN。
- 以及自身消融变体：FE-NET_noFEH（去掉FEH模块）、FE-NET_noFED（去掉FED模块，用传统超图神经网络）。

### 评估指标
- 准确率（Acc）、精确率（Pre）、特异性（Spe），均报告均值±标准差。

### 实验设置
- 5折交叉验证，训练和测试细节、超参数部分给出（αv=0.05, αe=0.9, lr=10⁻², weight decay=5×10⁻⁴, dropout=0.2, 5层IHEN, η=0.6）。

## 4. 资源与算力

**论文未明确说明硬件配置**（GPU型号、数量、训练时长等）。仅在附录中提及FEH-FED算法复杂度分析和与其他方法的计算资源对比，但未给出具体数值。因此无法评估训练成本。

## 5. 实验数量与充分性

- **主实验**：在LEMON数据集上进行四项二元分类任务（高/低持续注意力、高/低认知灵活性、高/低言语智商、高/低逻辑智商），对比8种SOTA方法和2种消融变体，报告三个指标。
- **泛化实验**：在CN-EPFL上进行两种模式（从LEMON迁移、直接在CN-EPFL上训练测试），结果见附录。
- **消融实验**：分别移除FEH和FED模块；单独验证OFEI和IHEN的作用；单独验证控制过程和扩散过程的作用。
- **可视化分析**：模态嵌入空间可视化、功能连接网络分析（top-120超边）。
- **统计显著性**：报告了均值和标准差，但未提供显著性检验（如p值或置信区间）。
- **充分性评价**：实验设计较为全面，覆盖了多个任务、多种消融、泛化测试和可视化分析，但缺乏对超参数敏感性的系统分析，且未提供统计显著性检验。

## 6. 主要结论与发现

- FE-NET在所有四个任务上均显著优于所有对比方法，在准确率上提升约6-10个百分点（例如TAP任务准确率85.29% vs 次优MMP-GCN 79.42%）。
- 消融实验证明FEH和FED模块均不可或缺，去掉任一模块性能下降。
- 可视化显示Neural ODE超图有效缩小了fMRI与EEG之间的模态嵌入空间差距，增强了聚类。
- 功能连接分析发现：言语智商相关FC主要位于默认模式网络（DMN）和腹侧注意网络（VAN）；逻辑智商相关FC主要位于视觉网络（VN）。
- 使用异步数据（更易获取、成本更低）即可取得优秀性能，证明方法实用性。

## 7. 优点

- **方法创新性**：首次将Neural ODE与超图结合用于异步fMRI-EEG联合建模，系统性解决了模态时间尺度差异和非一对多关系问题。
- **技术全面性**：结合GAN生成超图、OFEI保证拓扑一致性、IHEN动态融合、Neural ODE处理异步数据，形成完整框架。
- **实验扎实**：使用大型公开数据集LEMON（227人），对比多种SOTA方法，包括多模态和单模态方法，覆盖多个认知维度。
- **可解释性**：功能连接网络分析与已知神经科学知识一致，验证了模型的可解释性。
- **实用性**：采用异步采集的低成本数据，实际应用前景好。

## 8. 不足与局限

- **未报告计算资源**：无GPU型号、训练时间等信息，难以评估复现成本和可扩展性。
- **统计检验缺失**：仅报告均值±标准差，未进行配对t检验或方差分析，无法判断差异是否统计显著。
- **超参数分析不足**：仅给出最终超参数设置，未进行超参数敏感性实验。
- **数据集局限**：LEMON为健康被试，未在神经疾病数据集上验证；CN-EPFL仅20人，泛化实验规模小。
- **方法复杂度**：FEH（GAN+OFEI+IHEN）和FED（ODE+LSTM+注意力）计算开销可能较大，但未提供详细复杂度比较。
- **未见局限性讨论**：论文未设“局限性”章节，也未讨论模型假设违反时的鲁棒性、过拟合风险等问题。

（完）
