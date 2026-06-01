---
title: Accurate Identification of Communication Between Multiple Interacting Neural Populations
title_zh: MR-LFADS：多交互神经群体通信的精确识别
authors: "Belle Liu, Jacob Sacks, Matthew D. Golub"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=O14GjxDAt3"
tags: ["query:eeg-latent"]
score: 7.0
evidence: 使用序列变分自编码器对神经群体进行潜在因子分析
tldr: 现有模型难以从局部动态中分离出脑区间通信。本文提出MR-LFADS，一个基于区域特定循环神经网络的序列变分自编码器，通过结构化信息瓶颈和数据约束通信实现潜在因子分析。该方法可无监督推断未观测输入，有效分离脑区间通信成分。虽然以神经群体为对象，但其潜在空间建模思想可直接迁移至EEG多通道信号表征与缺失通道补全。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-o14gjxdat3/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1607, \"height\": 754, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-o14gjxdat3/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 854, \"height\": 1259, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-o14gjxdat3/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 852, \"height\": 1066, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-o14gjxdat3/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1753, \"height\": 837, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-o14gjxdat3/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1773, \"height\": 658, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-o14gjxdat3/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1753, \"height\": 1144, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-o14gjxdat3/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1771, \"height\": 1263, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-o14gjxdat3/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1762, \"height\": 1251, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-o14gjxdat3/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1390, \"height\": 762, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-o14gjxdat3/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1052, \"height\": 1564, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-o14gjxdat3/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1744, \"height\": 1091, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-o14gjxdat3/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 750, \"height\": 329, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-o14gjxdat3/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1507, \"height\": 487, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-o14gjxdat3/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1749, \"height\": 755, \"label\": \"Table\"}]"
motivation: 现有模型难以从局部动态中分离出脑区间通信成分。
method: 提出MR-LFADS，利用区域特定RNN的序列变分自编码器，通过结构化信息瓶颈和数据约束通信进行潜在因子分析。
result: 在模拟和真实神经数据上优于现有方法，成功分离通信与局部动态。
conclusion: MR-LFADS为多脑区通信分析提供了可解释的潜在空间方法，并能推广至EEG信号处理。
---

## Abstract
Neural recording technologies now enable simultaneous recording of population activity across multiple brain regions, motivating the development of data-driven models of communication between recorded brain regions. Existing models can struggle to disentangle communication from the effects of unrecorded regions and local neural population dynamics. Here, we introduce Multi-Region Latent Factor Analysis via Dynamical Systems (MR-LFADS), a sequential variational autoencoder composed of  region-specific recurrent networks. MR-LFADS features structured information bottlenecks, data-constrained communication, and unsupervised inference of unobserved inputs--features that specifically support disentangling of inter-regional communication, inputs from unobserved regions, and local population dynamics. MR-LFADS outperforms existing approaches at identifying communication across dozens of simulations of task-trained multi-region networks. Applied to large-scale electrophysiology, MR-LFADS predicts brain-wide effects of circuit perturbations that were not seen during model fitting. These validations on synthetic and real neural data suggest that MR-LFADS could serve as a powerful tool for uncovering the principles of brain-wide information processing.

---

## 论文详细总结（自动生成）

# 论文详细总结

## 1. 核心问题与整体含义（研究动机和背景）

- **研究动机**：现代神经记录技术能够同时记录多个脑区的群体活动，这促使研究者开发数据驱动的模型来描述脑区间的通信。然而，现有模型在从局部神经动态和未记录脑区的输入中分离出真正的脑区间通信时存在困难，导致对通信路径和内容的推断不准确。
- **核心问题**：如何从多区域群体记录中精确识别脑区间通信，同时避免四个主要挑战：通信信号不可直接观测、未记录区域输入的存在、需要准确重建各区域活动（包括非线性、非平稳动态和试次间变异性），以及数据重建准确不等于通信推断正确。
- **整体含义**：本文提出MR-LFADS，一种基于序列变分自编码器的多区域通信模型，旨在通过结构化信息瓶颈和数据约束通信来分离通信、未观测输入和局部动态，从而更可靠地揭示脑区间信息加工的机制。

## 2. 方法论：核心思想、关键技术细节与算法流程

- **核心思想**：MR-LFADS是一种耦合的非线性动态系统集合，每个记录脑区由一个独立的序列变分自编码器（SR-LFADS）模块建模，通过受约束的通信通道相互作用，并自动推断来自未观测区域的输入信号。
- **关键技术细节**：
  - **生成模型**：每个脑区i的生成过程包括单试次初始状态 \(g_0^i\)、时变通信消息 \(m_{j \rightarrow i}^t\)（来自其他记录脑区j）、推断输入 \(u_i^t\)（来自未观测区域）。所有潜变量服从高斯先验 \(N(0, \sigma^2 I)\)。每个脑区的生成器GRU更新状态：\(g_i^t = \text{GRU}_i^{\text{gen}}(g_i^{t-1}, \{m_{j \rightarrow i}^t\}_{j \neq i}, u_i^t)\)。随后通过仿射读取得到因子 \(f_i^t\)，再映射到可观测数据分布的参数（高斯或泊松）。
  - **推理模型**：通信消息的后验从源区域的预测发放率 \(r_j^t\) 中推断（称为数据约束通信，MR-LFADS(R)），即 \(q(m_{j \rightarrow i}^t | x_j^{1:t}) = N(\mu_{m,t}^{j \rightarrow i}, \Sigma_{m,t}^{j \rightarrow i})\)，参数由 \(r_j^t\) 的仿射变换得到。初始状态使用双向编码器从过去活动 \(x_i^{-\tau:0}\) 推断；推断输入使用单向编码器逐时间步因果推断。
  - **结构化信息瓶颈**：训练时最大化ELBO，包含重建损失和KL散度项。对通信消息和推断输入的KL权重分别设置为 \(\beta_m\) 和 \(\beta_u\)，且通常设置 \(\beta_u = 10\beta_m\)，以鼓励优先使用通信而非推断输入。
  - **训练流程**：使用重参数技巧和梯度下降优化ELBO；时间步从1到T，因果推断确保所有通信消息causal。

## 3. 实验设计

- **数据集/场景**：
  - **合成数据**：共37个多区域数据集，全部由任务训练的多区域数据生成网络（DGN）生成，包括：
    - 实验1：记忆网络（3区域，每个区域收到私有刺激并需要记忆历史信息，通信携带2步延迟的刺激信号），用于测试未观测输入推断能力。
    - 实验2：传递-决策网络（2区域，上游区域AP执行恒等映射传递刺激，下游区域AD积分刺激为决策变量），用于测试数据约束通信防止计算错位。
    - 实验3：35个随机生成的DGN（3或4区域，随机连接性，训练于多种认知任务如Go、反Go、延迟决策、多感觉决策、分类等），用于评估泛化能力。
  - **真实数据**：小鼠在听觉决策任务中进行的多区域神经探针记录（5区域：ALM、MRN、SC、Thal(A)、Thal(O)），包含光抑制ALM的扰动试次。
- **Benchmark与对比方法**：
  - **现有方法**：RRR（缩减秩回归）、mp-srSLDS（多群体粘性递归切换线性动态系统）、MR-SDS（多区域切换非线性动态系统）。
  - **MR-LFADS消融变体**：
    - MR-LFADS(S)：手动指定外部输入（不自动推断输入）。
    - MR-LFADS(F)：通信从因子（factors）推断（非发放率）。
    - MR-LFADS(G)：通信从生成器状态（generator states）推断。
- **评估指标**：
  - 效果图相似度（\(S_{cos}\)）：模型推断的消息范数矩阵与真实通信矩阵的余弦相似度。
  - 消息内容准确性：线性回归预测真实消息的 \(R^2\)。
  - 数据重建质量：\(R^2\) 或泊松对数似然。

## 4. 资源与算力

- **论文未明确说明使用的GPU型号、数量、训练时长**。仅在讨论中提到MR-LFADS超参数敏感，可能需要大量计算资源进行超参数优化，类似SR-LFADS（Keshtkaran et al., 2022）。此外，实验中的超参数搜索使用了Ray Tune等工具，但未给出具体算力消耗。

## 5. 实验数量与充分性

- **实验数量**：
  - 实验1：单个记忆网络，10个随机种子（模型初始化），每个种子训练一次。
  - 实验2：单个传递-决策网络，10个随机种子。
  - 实验3：35个随机DGN（不同任务、连接性、区域数），每个DGN训练一个种子。
  - 真实数据应用：两个分析（光抑制预测、跨种子一致性），分别使用5个随机种子。
- **充分性评估**：
  - **覆盖范围广泛**：合成数据涵盖记忆、决策、随机任务等多种认知场景；真实数据包括因果扰动验证。
  - **消融实验充分**：对比了R、F、G、S四种MR-LFADS变体以及现有方法，在多个数据集上评估了效果图和消息内容。
  - **统计检验**：在实验3中使用了单侧t检验比较MR-LFADS(R)与其他方法的指标分布，结果具有统计显著性。
  - **潜在不足**：实验1和2仅基于单个DGN，结果可能受特定网络结构影响；35个随机网络每个仅一个种子，未报告种子变异性；消融变体S仅在实验1中测试，未在实验2和3中系统比较（但实验2有F、G，实验3有F、G）。总体而言，实验设计较为客观公平，但部分变体对比覆盖不全。

## 6. 主要结论与发现

- **合成数据结果**：
  - MR-LFADS(R)在识别通信路径（效果图余弦相似度）和消息内容（R²）上持续优于RRR、mp-srSLDS、MR-SDS以及消融变体。
  - 自动推断输入（MR-LFADS(R)）比手动指定输入（MR-LFADS(S)）更准确，避免模型放弃使用通信而依赖指定输入的错误模式。
  - 数据约束通信（从发放率推断）比从因子或生成器状态推断（F、G）更有效，能减少计算错位（如将积分动态错误定位到上游区域）。
  - 跨35个随机DGN的泛化结果显示，MR-LFADS(R)在消息内容恢复上全面最佳，而R和G在效果图相似度上相当。
- **真实数据结果**：
  - 仅在控制试次训练的MR-LFADS(R)能准确预测光抑制ALM后对其他脑区（Thal(A)、MRN、SC、Thal(O)）的影响程度，与实验观测模式一致。
  - 跨5个随机种子的模型比较显示，MR-LFADS(R)的推断通信内容比MR-LFADS(G)更一致（消息范数相关性更高）。

## 7. 优点

- **方法创新**：提出三种关键设计（自动推断未观测输入、数据约束通信、结构化信息瓶颈），直接针对通信建模的四个核心挑战，形成系统解决方案。
- **验证充分**：在37个合成数据集和真实电生理数据上进行评估，包含因果扰动验证和跨种子稳健性检查，结果可靠。
- **可解释性**：通信消息来源于预测发放率，直接与神经活动关联，降低潜在歧义；KL正则化自然压缩冗余潜变量维度。
- **性能领先**：在多个指标上显著优于现有模型（RRR、mp-srSLDS、MR-SDS），消融实验证实各设计特征的必要性。

## 8. 不足与局限

- **超参数敏感**：MR-LFADS对KL权重（\(\beta_u, \beta_m\)）等超参数敏感，需要大量调优才能获得最优性能，这增加了应用门槛。
- **相关-因果混淆**：模型不能解决经典的相关-因果混淆问题（例如一个未观测区域同时驱动多个记录区域），推断的输入和通信仍可能合并混淆信号。作者承认这一点，并建议结合因果扰动实验进行验证。
- **计算资源需求**：未报告具体算力，但训练多区域、大规模RNN且进行超参数搜索需要较多GPU资源，可能限制广泛应用。
- **解释性限制**：虽然推断输入被证明能反映外部刺激，但其具体表征（如维度、内容）仍需进一步解释；未来工作可关注如何解释这些潜变量。
- **应用范围**：目前主要针对离线分析，尚未探索在线或实时应用场景。此外，模型假设各区域活动可同时记录，未处理异步或不同时间分辨率的数据。

（完）
