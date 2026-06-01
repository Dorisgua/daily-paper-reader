---
title: "ProDiff: Prototype-Guided Diffusion for Minimal Information Trajectory Imputation"
title_zh: ProDiff：基于原型引导的扩散模型实现最小信息轨迹插补
authors: "Tianci Bu, Le Zhou, Wenchuan Yang, Jianhong Mou, Kang Yang, Suoyi Tan, Feng Yao, Jingyuan Wang, Xin Lu"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=9rG2oAWj0s"
tags: ["query:eeg-latent"]
score: 5.0
evidence: 基于扩散模型的原型学习轨迹插补，可迁移至EEG通道补全
tldr: ProDiff提出仅利用起点和终点作为最小信息的轨迹插补框架，结合原型学习嵌入人类移动模式与去噪扩散概率模型实现鲁棒时空插补。在多个轨迹数据集上优于基线，其扩散生成范式为EEG缺失通道生成提供了可借鉴的方法。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-9rg2oawj0s/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 857, \"height\": 487, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-9rg2oawj0s/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1763, \"height\": 649, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-9rg2oawj0s/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 849, \"height\": 650, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-9rg2oawj0s/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1763, \"height\": 510, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-9rg2oawj0s/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1666, \"height\": 1008, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-9rg2oawj0s/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 758, \"height\": 941, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-9rg2oawj0s/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1777, \"height\": 1040, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-9rg2oawj0s/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 859, \"height\": 336, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-9rg2oawj0s/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 860, \"height\": 373, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-9rg2oawj0s/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 858, \"height\": 219, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-9rg2oawj0s/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 864, \"height\": 334, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-9rg2oawj0s/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 807, \"height\": 408, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-9rg2oawj0s/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 933, \"height\": 275, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-9rg2oawj0s/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 956, \"height\": 477, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-9rg2oawj0s/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1697, \"height\": 282, \"label\": \"Table\"}]"
motivation: 现有轨迹插补依赖稀疏轨迹信息，对数据采集要求高且忽视大规模嵌入。
method: 提出ProDiff，整合原型学习和去噪扩散概率模型，仅用两个端点进行插补。
result: 在真实轨迹数据集上以少量信息达到甚至超越完整信息方法的性能。
conclusion: ProDiff验证了扩散模型在极稀疏信息下进行时空插补的有效性。
---

## Abstract
Trajectory data is crucial for various applications but often suffers from incompleteness due to device limitations and diverse collection scenarios. Existing imputation methods rely on sparse trajectory or travel information, such as velocity, to infer missing points. However, these approaches assume that sparse trajectories retain essential behavioral patterns, which place significant demands on data acquisition and overlook the potential of large-scale human trajectory embeddings.
To address this, we propose ProDiff, a trajectory imputation framework that uses only two endpoints as minimal information. It integrates prototype learning to embed human movement patterns and a denoising diffusion probabilistic model for robust spatiotemporal reconstruction. Joint training with a tailored loss function ensures effective imputation.
ProDiff outperforms state-of-the-art methods, improving accuracy by 6.28\% on FourSquare and 2.52\% on WuXi. Further analysis shows a 0.927 correlation between generated and real trajectories, demonstrating the effectiveness of our approach.

---

## 论文详细总结（自动生成）

# 论文《ProDiff: Prototype-Guided Diffusion for Minimal Information Trajectory Imputation》详细总结

## 1. 核心问题与整体含义（研究动机和背景）

- **研究动机**：轨迹数据在疾病控制、人类行为分析、城市规划等领域至关重要，但由于设备限制（如基站覆盖缺口、信号不稳定、环境干扰）和多样化的采集场景，轨迹数据经常不完整。现有插补方法（如线性插值、VAR、深度学习模型）通常假设稀疏轨迹仍保留了关键行为模式（例如利用速度等额外信息），这给数据采集带来了较高要求，且忽略了大规模未标记轨迹数据中蕴含的宏观行为模式潜力。
- **核心问题**：能否在仅提供轨迹的两个端点（起点和终点）作为最小信息的情况下，高精度地重建中间缺失点？这比传统方法更宽松地放松了“稀疏轨迹需保留行为模式”的假设。
- **整体含义**：本文证明了结合原型学习（捕捉人类移动模式）与去噪扩散概率模型（DDPM）可以在极稀疏信息下实现有效轨迹插补，为低信息条件下的时空数据生成提供了新范式。

## 2. 方法论：核心思想、关键技术细节、公式或算法流程

- **核心思想**：提出ProDiff框架，包含两个关键组件：
  1. **原型条件提取器（Prototype Condition Extractor, PCE）**：通过自监督学习将大量未标记轨迹嵌入到向量空间，并学习一组原型（prototypes）代表宏观移动模式。在推理时，根据已知端点作为查询，从原型空间中提取条件特征。
  2. **扩散生成模型（Denoising Diffusion Probabilistic Model）**：使用1D-UNet作为主干网络，以端点为基本条件（base condition），结合原型条件（prototype condition），通过迭代去噪生成完整的轨迹点。
- **关键技术细节**：
  - **基础条件**：仅保留轨迹的起点和终点，其他点被掩码（mask）掉，作为扩散模型的基本引导。
  - **原型条件提取**：对每段轨迹进行编码得到特征表示，通过全连接层生成原型，并利用距离函数（如欧氏距离）将查询特征映射到原型空间，得到原型条件特征。
  - **联合条件**：使用Wide & Deep网络将基础条件和原型条件相加，得到最终条件 \(J_c\)。
  - **联合训练损失函数**：包括扩散损失 \(L_J\)、聚类一致性损失 \(L_{C1}\)（使K-means聚类标签与原型分配标签对齐）、对比损失 \(L_{C2}\)（促进原型间分离），总损失为加权和：\(L = \lambda_1 L_J + \lambda_2 L_{C1} + \lambda_3 L_{C2}\)。
  - **推理过程**：给定两个端点，生成基础条件，查询训练好的原型得到原型条件，融合后从标准高斯噪声开始逐步去噪，得到全轨迹。
- **算法流程**（文字说明）：
  - **训练**：对每批数据，计算基础条件 \(B_c\)，通过PCE获得原型条件 \(P_c\)，融合得到 \(J_c\)。采样原始轨迹 \(Z_0\)，加噪得到 \(Z_t\)，训练网络预测噪声 \(\epsilon\)，同时优化原型损失。
  - **采样**：给定两个端点，生成 \(B_c\)，用PCE获取 \(P_c\)，融合得 \(J_c\)。从标准正态噪声开始，按扩散步骤反向去噪，输出重构轨迹。

## 3. 实验设计

- **数据集**：
  - **WuXi**：中国无锡市手机信号数据（2013.10–2014.03），选取10天子集，约33000活跃用户（训练30000，测试3000），含671,124条位置记录。
  - **Foursquare**：纽约和东京的签到数据（2012.04–2013.02），仅使用东京数据，共2293活跃用户（训练1834，测试459），573,703条位置记录。
- **基准方法（Baselines）**：
  - 时间序列插补方法：VAR、SAITS、TimesNet、Diffusion-TS、DiffTraj。
  - 轨迹专用方法：RNTrajRec、TS-TrajGen、MM-STGED、AttnMove、DiffTraj。
  - 论文还对比了使用条件VAE（cVAE）和条件GAN（cGAN）替换扩散模块的版本。
- **评估指标**：
  - **主指标**：轨迹覆盖率（Trajectory Coverage, \(TC@\tau\)），计算生成点与真实点距离小于阈值的比例，阈值从2km到10km。
  - **附加指标**：密度（Density）、距离（Distance）、段距离（Segment Distance）、半径（Radius）、MAE、RMSE。

## 4. 资源与算力

- 论文中**未明确说明**使用的GPU型号、数量、训练时长等具体算力信息。仅在实现细节中提到使用Adam优化器，学习率2e-4，扩散步数500，原型数量20等超参数。未提供训练时间或硬件资源描述。

## 5. 实验数量与充分性

- **实验数量**：
  - 主实验（表1）：在2个数据集上，对4种窗口长度（k=4,6,8,10）分别报告5个阈值下的TC@τ，对比7种方法（VAR、SAITS、TimesNet、Diff-TS、DiffTraj、Diff+Mask、ProDiff），共4×2×7=56个数值结果。
  - 消融实验（表3）：去掉PCE、L_{C1}、L_{C2}，在k=6和8两个窗口上报告5个阈值，共2×4×5=40个数值。
  - 泛化性实验（表4）：将原型条件与cVAE、cGAN结合，在k=6窗口上报告5个阈值。
  - 超参数敏感性（表5、表7）：原型数量（15,20,25）和扩散步数（100,300,500,700）的影响。
  - 加速实验（表9）：使用DDIM和线性注意力加速，对比性能和吞吐量。
  - 额外信息实验（表8）：在k=10下给出2/3/4/5个固定点或随机点时的性能。
  - 可解释性分析（图5）：对原型嵌入空间进行可视化聚类，展示6个簇的典型轨迹形态。
  - 下游任务验证（图6）：使用生成的轨迹做交通流分析，计算相关系数（0.927）。
- **充分性与公平性**：
  - 实验较为充分：涵盖了不同窗口长度、不同阈值、多种基线（包括传统方法和最新扩散方法）、多种消融组件、跨生成模型泛化、超参数分析、加速验证、可解释性分析以及下游任务应用。
  - 公平性：基线方法尽量移除依赖额外信息的模块；使用统一的轨迹覆盖率和空间分布指标；在两个真实世界数据集上验证。
  - 但缺乏对计算资源消耗（内存、时间）的公平比较（如模型参数量、推理时间等），且未在高噪声或极端稀疏场景下（如窗口极大或极小）进行测试。

## 6. 主要结论与发现

- **性能优势**：ProDiff在所有窗口长度和阈值下均优于现有方法。在WuXi数据集（k=4）上，TC@2k达71.55%，比第二好的方法（DiffTraj 69.58%）高1.97%；在FourSquare上，ProDiff将轨迹覆盖TC@2k从DiffTraj的59.45%提升至66.44%（提升6.99%）。在指标上提升6.28%（FourSquare）和2.52%（WuXi）。
- **原型学习有效性**：去除PCE后性能显著下降（尤其是在长窗口k=8时，TC@2k从57.52%降至44.86%），且原型损失（L_{C1}和L_{C2}）进一步提升了性能。
- **泛化性**：PCE同样能提升cVAE和cGAN的性能，证明其与不同生成模型兼容。
- **生成数据可用性**：生成的轨迹与真实轨迹的相关系数达0.927，交通流分析显示空间模式高度相似。
- **可解释性**：原型嵌入空间中的聚类呈现语义明确的轨迹模式（如近距离移动、远距离迁移、折返等），说明原型成功捕捉了人类移动的宏观行为。

## 7. 优点

- **方法创新**：首次将原型学习引入轨迹插补任务，仅利用两个端点即可生成高质量轨迹，极大放松了对数据采集的要求。
- **联合训练框架**：将扩散模型损失与原型聚类损失、对比损失联合优化，避免了多阶段训练的误差累积。
- **实验全面**：涵盖多种基线、多种窗口、多种阈值、消融、泛化、超参数、加速、可解释性、下游任务，验证充分。
- **可解释性与实用性**：通过原型可视化展示了模型学到的人类移动模式，并验证了生成数据在交通流分析中的实用价值。
- **效率优化**：提供了DDIM和线性注意力加速版本，可在保持较高性能的同时实现约10倍加速。

## 8. 不足与局限

- **算力信息缺失**：未报告训练/推理时的GPU型号、时长、显存等资源消耗，不利于复现与对比。
- **场景覆盖有限**：仅测试了两个城市（无锡和东京）的数据，未在其他类型轨迹（如车辆GPS、室内轨迹）上验证泛化性；窗口长度仅到10点，未探索更长轨迹的插补表现。
- **未与最先进的轨迹专用方法对齐**：部分基线（如RNTrajRec、AttnMove）需要地图匹配等额外信息，在对比时移除相关模块可能影响其真实性能。
- **端点假设的局限性**：实际中两个端点可能也是不准确的或缺失的（如传感器故障），论文未讨论这种更现实的情景。
- **可解释性分析较浅**：虽然聚类展示了不同轨迹模式，但未定量评估这些原型对生成结果的具体贡献。
- **未考虑隐私风险**：生成轨迹可能泄露个人位置隐私，论文未讨论差分隐私或匿名化措施。

（完）
