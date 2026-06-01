---
title: Inference of Whole Brain Electrophysiological Networks Through Multimodal Integration of Simultaneous Scalp and Intracranial EEG
title_zh: 通过同步头皮和颅内脑电的多模态集成推断全脑电生理网络
authors: "Shihao Yang, Feng Liu"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=6UAeCPQPwP"
tags: ["query:eeg"]
score: 7.0
evidence: 从头皮和颅内EEG联合推断全脑电生理网络
tldr: 全脑电生理网络的推断对于神经科学和临床重要，但现有方法难以融合头皮与颅内脑电。本文提出基于状态空间模型的框架，利用期望最大化算法联合推断网络状态和脑连通性，实现了更精确的全脑网络估计，为多模态EEG分析提供了新思路。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-6uaecpqpwp/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1162, \"height\": 573, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-6uaecpqpwp/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 794, \"height\": 478, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-6uaecpqpwp/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 565, \"height\": 415, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-6uaecpqpwp/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 804, \"height\": 295, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-6uaecpqpwp/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1230, \"height\": 358, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-6uaecpqpwp/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1380, \"height\": 1223, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-6uaecpqpwp/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1370, \"height\": 122, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-6uaecpqpwp/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1172, \"height\": 638, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-6uaecpqpwp/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1173, \"height\": 635, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-6uaecpqpwp/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1172, \"height\": 637, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-6uaecpqpwp/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1172, \"height\": 427, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-6uaecpqpwp/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1172, \"height\": 460, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-6uaecpqpwp/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1175, \"height\": 446, \"label\": \"Table\"}]"
motivation: 需要整合头皮和颅内脑电来更好估计全脑电生理网络。
method: 提出状态空间建模框架，利用EM算法融合头皮与颅内EEG推断脑网络。
result: 在合成和真实数据上验证了网络估计的准确性。
conclusion: 该方法为多模态EEG网络分析提供了有效框架。
---

## Abstract
Brain imaging research has transitioned over the past decades from identifying isolated regions of task-evoked activation to characterizing the spatiotemporal dynamics of large-scale brain networks. Electrophysiological signals are the direct manifestation of brain activity; thus, characterizing whole-brain electrophysiological networks (WBEN) can serve as a fundamental tool for neuroscience studies and clinical applications. In this work, we introduce a framework for integrating scalp EEG and intracranial EEG (iEEG) for WBEN estimation through a principled state-space modeling approach, where an Expectation-Maximization (EM) algorithm is designed to infer the state variables and brain connectivity simultaneously. We validated the proposed method on synthetic data, and the results revealed improved performance compared to traditional two-step methods using scalp EEG only, demonstrating the importance of including iEEG signals for WBEN estimation. For real data with simultaneous EEG and iEEG, we applied the developed framework to understand the information flows during encoding and maintenance phases of a working memory task. The information flows between subcortical and cortical regions are delineated, highlighting more significant information flows from cortical to subcortical regions during encoding than during maintenance. The results are consistent with previous research findings, but from a whole-brain perspective, which underscores the unique utility of the proposed framework.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **研究动机**：脑成像研究已从关注孤立脑区转向大规模脑网络的时空动态表征。电生理信号是脑活动的直接体现，因此准确推断**全脑电生理网络（WBEN）** 对神经科学和临床应用至关重要。然而，现有方法多采用两步法（先源成像再计算功能连接），受限于源成像的逆问题病态性，难以准确估计全脑网络。
- **核心挑战**：头皮脑电图（EEG）空间分辨率低、源定位不精确；颅内脑电图（iEEG）虽时空分辨率高但只能覆盖部分脑区（部分可观测）。如何利用两种模态互补优势，在统一的概率框架下精确推断全脑电生理网络，是亟需解决的问题。
- **核心贡献**：首次提出一个**状态空间建模框架**，融合同步记录的头皮EEG和iEEG，通过**期望最大化（EM）算法**同时推断隐状态（源活动）和脑功能连接（状态转移矩阵），实现全脑尺度、毫秒级时间分辨率的网络重建。

## 2. 论文提出的方法论

- **核心思想**：将脑源活动建模为线性离散动态系统，EEG和iEEG观测均为源活动的线性投影加噪声。通过引入**L1正则化**鼓励连接稀疏性，利用EM算法迭代求解隐状态和模型参数。
- **关键技术细节**：
  - **状态空间模型**：  
    \( x_t = \sum_{k=1}^K \Phi_k x_{t-k} + n_t \) （源动态）  
    \( y_t = L x_t + w_t \) （EEG观测）  
    \( z_t = C x_t + e_t \) （iEEG观测）  
    其中，\(\Phi\) 为状态转移矩阵（即脑连接），\(L\) 为EEG导联场矩阵，\(C\) 为iEEG选择矩阵（只观测部分源区域），\(n_t, w_t, e_t\) 均为高斯噪声。
  - **EM算法流程**：
    - **E步**：给定当前参数\(\theta^{(j)}\)，通过**固定区间平滑（FIS）** 估计隐状态\(x_{1:T}\)的后验均值和协方差。FIS包括前向卡尔曼滤波和后向卡尔曼平滑，将EEG和iEEG合并为增广观测\(y^+ = [y; z]\)，噪声协方差\(P^+ = \text{blkdiag}(P,S)\)。
    - **M步**：最大化关于\(\theta\)的Q函数，并加入L1稀疏正则化（\(\lambda \sum \|\Phi_i\|_1\)），通过**快速自适应收缩/阈值算法（FASTA）** 求解，更新\(\Phi\)和噪声协方差\(Q\)。
  - **正则化**：假设每个脑区的入边连接稀疏，减轻逆问题病态性。
- **算法流程**（文字描述）：  
  输入EEG、iEEG、导联场矩阵、噪声协方差估计；初始化参数（如MNE源定位结果）；迭代执行E步（FIS平滑获得源后验统计量）和M步（FASTA优化稀疏连接），直至收敛。

## 3. 实验设计

- **数据集/场景**：
  - **合成数据**：基于FreeSurfer真实头部模型和128通道BioSemi EEG生成逼真EEG信号，使用柏林脑连接基准（BBCB）生成因果时间序列，源信号经巴特沃斯滤波（0.1–40 Hz）。通过改变可观测脑区比例（0%–60%）、EEG信噪比（-10dB至5dB，iEEG SNR固定30dB）、网络复杂度（激活区域数10/15/20，节点入度1–4）评估性能。
  - **真实数据**：15名癫痫患者进行Sternberg言语工作记忆任务时同步记录的头皮EEG（10-20系统）和iEEG（深度电极）。数据来自公开数据集（doi:10.18112/openneuro.ds004752.v1.0.1）。分析编码阶段（1-3s）和维持阶段（3-6s，取最后2s）。源空间基于Harvard-Oxford图谱（69个区域）聚合，iEEG电极映射到对应脑区。
- **Benchmark**：对比方法包括两步法：先用经典源成像算法（MNE, dSPM, sLORETA, eLORETA）或深度学习源成像（ALCMV, ASTAR, VSSI-ARD）重建源信号，再用格兰杰因果/传递熵/偏定向相干计算连接。同时对比仅用EEG（0% iEEG观测）的情况。
- **评估指标**：敏感性（Sen=正确连接数/真实连接总数）、准确率（Acc=正确连接数/预测连接总数）、假阳性率（FPR）。对真实数据还进行了被试内/被试间一致性分析。

## 4. 资源与算力

- **计算平台**：Windows 11 Pro台式机，32GB内存，Intel i9-12900KF CPU，NVIDIA A6000 GPU（48GB显存）。
- **计算时间**：对于69个源区域、1000个时间点，全脑网络估计约需**3分钟**（壁钟时间），未提及具体训练轮次或GPU利用率。

## 5. 实验数量与充分性

- **实验数量**：合成数据上进行了多组全因子设计：
  - 可观测比例实验（7个水平：0%–60%），每个水平10次重复。
  - SNR实验（4个水平：-10dB到5dB），对比多种基准方法。
  - 网络复杂度实验（不同激活区域数、不同入度）。
  - 因果分析对比（格兰杰因果、传递熵、偏定向相干）。
- **充分性**：统计上，进行了组t检验验证差异显著性（如30% iEEG观测与0%的显著差异）。实验设计较为全面，覆盖了噪声、覆盖率、复杂度等关键因素。但也存在不足：
  - 真实数据仅15名癫痫患者，样本量较小，且患者本身可能存在异常脑网络，可能影响结果泛化性。
  - 对比方法未进行超参数调优（如正则化参数），可能不利于两步法性能。
  - 未在多个独立数据集上验证（如不同任务、健康受试者）。
- **客观性**：直接对比一步法与两步法，在几乎所有条件下一步法+30% iEEG观测性能更优，但两步法在低SNR时FPR极高，可能部分源于源成像方法的默认参数设置未优化。

## 6. 论文的主要结论与发现

- **合成数据结论**：
  - 随着iEEG可观测脑区比例增加（>20%），WBEN估计的**准确性（Acc）和敏感性（Sen）显著提升**，30%时出现跳跃式改善（Acc从0.189升至0.545）。
  - 在低EEG SNR条件下，仅用EEG的一步法性能急剧下降，而**融合iEEG后性能相对稳定**，凸显iEEG对噪声鲁棒性的贡献。
  - 相比所有两步法（包括eLORETA等最佳源成像方法），所提一步法+30% iEEG在**Sen、Acc、FPR**上全面占优。
- **真实数据结论**：
  - 编码阶段**皮层→皮层下**信息流更强（尤其是额叶、颞叶、顶叶到丘脑和基底节），维持阶段方向逆转，**皮层下→皮层**连接更活跃。
  - 整体连接强度编码阶段强于维持阶段，组t检验显著（p<0.001）。
  - 结果与文献一致（如海马-听觉皮层信息流），但首次从**全脑尺度**刻画了皮层-皮层下交互。

## 7. 优点

1. **方法创新性**：首次提出统一的状态空间框架整合头皮EEG和iEEG，规避了两步法中源成像误差累积问题，实现了端到端的连接估计。
2. **理论严谨性**：基于贝叶斯状态空间模型和EM算法，提供了完整的概率推导；加入L1正则化应对高维病态问题，并通过FIS平滑获得精确后验统计量。  
3. **实验验证充分**：合成数据上系统评估了可观测比例、信噪比、网络复杂度的影响，并与多种主流两步基准方法对比，证实融合iEEG的显著优势。
4. **真实应用价值**：在言语工作记忆任务中成功提取皮层-皮层下动态连接模式，结果与已知神经机制吻合，展现了临床和认知神经科学的潜在应用价值。
5. **计算效率**：基于图谱（69个区域）的源空间，算法运行时间可接受（约3分钟/1000时间点），具备实用可行性。

## 8. 不足与局限

1. **样本与数据局限**：真实数据仅来自15名癫痫患者，且iEEG电极位置由临床需求决定，并非全脑均匀覆盖；结果可能受患者脑病理性影响，推广至健康人需谨慎。
2. **模型假设较强**：假设源噪声和观测噪声均为高斯分布且协方差已知（通过空房间测量）；在实际中噪声协方差难以精确获得，模型对偏差可能敏感。
3. **虚假连接风险**：作者明确承认存在“信号泄漏”导致的**鬼影交互（ghost interactions）** 问题，即由于源定位不唯一产生假阳性连接；虽用稀疏正则化抑制，但未在附录中展示具体缓解措施。
4. **对比方法公平性存疑**：两步法的源成像算法未经过充分调优（如正则化参数），可能导致其性能低于潜在最优表现；此外，一步法中iEEG观测占比30%在真实场景中难以达到（仅能覆盖少数脑区）。
5. **未考虑时频动态**：模型仅使用时域VAR模型，未纳入不同频段（θ、γ等）的特定连接差异，而工作记忆中的神经振荡具有频率特异性。
6. **消融实验不足**：未单独分析iEEG噪声协方差S的估计误差对结果的影响，也未比较融合不同数量iEEG通道的效果。

（完）
