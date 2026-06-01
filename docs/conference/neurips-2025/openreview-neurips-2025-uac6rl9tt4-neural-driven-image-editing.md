---
title: Neural-Driven Image Editing
title_zh: 神经驱动图像编辑
authors: "Pengfei Zhou, Jie Xia, Xiaopeng Peng, Wangbo Zhao, Zilong Ye, Zekai Li, Suorong Yang, Jiadong Pan, Yuanxiang Chen, Ziqiao Wang, Kai Wang, Qian Zheng, Xiaojun Chang, Gang Pan, Shurong Dong, Kaipeng Zhang, Yang You"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=UAc6RL9Tt4"
tags: ["query:eeg-latent"]
score: 4.0
evidence: 使用EEG信号和潜在空间表示进行生成任务
tldr: "该论文提出LoongX，一种基于EEG等多模态生理信号的无手图像编辑方法。利用扩散模型和跨尺度状态空间模块从EEG信号中提取潜在表示，实现用户意图捕捉。方法涉及EEG信号的深度学习处理和潜在空间编码，但目标为图像编辑而非EEG信号重建或通道补全。在包含EEG的23,928对图像编辑数据集上训练，验证了方法的有效性。"
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-uac6rl9tt4/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1241, \"height\": 591, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uac6rl9tt4/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1413, \"height\": 743, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uac6rl9tt4/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1388, \"height\": 712, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uac6rl9tt4/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 669, \"height\": 597, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uac6rl9tt4/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 696, \"height\": 666, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uac6rl9tt4/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 810, \"height\": 789, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uac6rl9tt4/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1439, \"height\": 1251, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uac6rl9tt4/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1386, \"height\": 544, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uac6rl9tt4/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1443, \"height\": 418, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uac6rl9tt4/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1434, \"height\": 2103, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uac6rl9tt4/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1443, \"height\": 2092, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uac6rl9tt4/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1437, \"height\": 1933, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uac6rl9tt4/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1447, \"height\": 1058, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uac6rl9tt4/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1445, \"height\": 928, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-uac6rl9tt4/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1453, \"height\": 308, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-uac6rl9tt4/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1420, \"height\": 337, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-uac6rl9tt4/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1470, \"height\": 657, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-uac6rl9tt4/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1443, \"height\": 701, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-uac6rl9tt4/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1364, \"height\": 492, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-uac6rl9tt4/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1335, \"height\": 301, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-uac6rl9tt4/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1259, \"height\": 300, \"label\": \"Table\"}]"
motivation: 传统图像编辑依赖手动提示，对运动障碍者不友好，亟需基于脑信号的交互方式。
method: 构建LoongX框架，使用扩散模型结合EEG等多模态信号，通过跨尺度状态空间模块提取潜在表示驱动图像编辑。
result: 在包含EEG的大规模数据集上训练，实现了有效的脑驱动图像编辑，展示了EEG潜在表示的能力。
conclusion: 该工作开拓了EEG潜在表示在生成任务中的应用，但非直接针对通道补全。
---

## Abstract
Traditional image editing typically relies on manual prompting, making it labor-intensive and inaccessible to individuals with limited motor control or language abilities. Leveraging recent advances in brain-computer interfaces (BCIs) and generative models, we propose LoongX, a hands-free image editing approach driven by multimodal neurophysiological signals. 
LoongX utilizes state-of-the-art diffusion models trained on a comprehensive dataset of 23,928 image editing pairs, each paired with synchronized electroencephalography (EEG), functional near-infrared spectroscopy (fNIRS), photoplethysmography (PPG), and head motion signals that capture user intent.
To effectively address the heterogeneity of these signals, LoongX integrates two key modules. The cross-scale state space (CS3) module encodes informative modality-specific features. The dynamic gated fusion (DGF) module further aggregates these features into a unified latent space, which is then aligned with edit semantics via fine-tuning on a diffusion transformer (DiT).
Additionally, we pre-train the encoders using contrastive learning to align cognitive states with semantic intentions from embedded natural language.
Extensive experiments demonstrate that LoongX achieves performance comparable to text-driven methods (CLIP-I: 0.6605 vs. 0.6558; DINO: 0.4812 vs. 0.4637) and outperforms them when neural signals are combined with speech (CLIP-T: 0.2588 vs. 0.2549). These results highlight the promise of neural-driven generative models in enabling accessible, intuitive image editing and open new directions for cognitive-driven creative technologies. The code and dataset are released on the project website: https://loongx1.github.io.

---

## 论文详细总结（自动生成）

## 论文详细中文总结

### 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：传统图像编辑高度依赖手动提示（如文本指令、鼠标拖拽、掩码绘制等），不仅劳动强度大，而且对运动或语言障碍人群极不友好。能否直接利用脑电等神经信号实现“无手”图像编辑，从而提升交互的直观性和包容性？
- **整体含义**：该工作首次探索将多模态神经生理信号（EEG、fNIRS、PPG、头部运动）作为唯一或补充条件，驱动扩散模型完成图像编辑，开辟了“脑控生成”的新方向，有望为BCI辅助创意工具奠定基础。

### 2. 论文提出的方法论：核心思想、关键技术细节、公式或算法流程

- **核心思想**：构建一个端到端的神经网络系统LoongX，从用户的多模态神经信号中提取意图特征，并将其作为条件注入扩散Transformer（DiT），以生成符合用户期望的编辑结果。
- **关键技术细节**：
  - **数据预处理**：EEG（4通道：Pz, Fp2, Fpz, Oz，250Hz）经1-80Hz带通+48-52Hz陷波滤波；fNIRS（6通道，735/850nm）通过修正Beer-Lambert定律转换为HbO/HbR/HbT浓度，经0.01-0.5Hz带通滤波；PPG（4通道，0.5-4Hz）提取心率变异性；运动数据（6轴，12.5Hz）直接使用。
  - **跨尺度状态空间编码（CS3）**：针对每类信号，使用自适应金字塔池化（5层，d=64）提取多尺度特征，并结合两个并行结构化状态空间模型（S3M，O(L log L)复杂度）分别沿时间维和通道维编码，最后通过跨金字塔聚合得到统一嵌入。
  - **动态门控融合（DGF）**：对任意一对内容嵌入和条件嵌入，先通过门控网络混合实例层与层级的统计量（均值/方差）进行归一化，再通过条件特征驱动的仿射变换（γ, β）调制，最后使用动态掩码保留top‑k通道，得到融合潜变量。
  - **条件扩散**：以融合特征为条件，使用DiT（基于FLUX.1-dev骨架）预测速度场v_θ，通过流匹配优化目标（最小化速度均方误差）进行微调。
  - **两阶段训练**：先利用公开认知数据集（Thinking out loud等）和L-Mind对CS3编码器进行对比学习（NT‑Xent损失），对齐神经特征与文本语义；再联合微调编码器和DiT。

### 3. 实验设计：数据集、基准、对比方法

- **数据集**：自建L-Mind数据集，包含23,928个图像编辑对（原始图+目标图+文字指令），每个样本同步记录EEG、fNIRS、PPG、头部运动和语音信号。12名被试在自然室内环境采集（22,728训练，1,200测试）。额外收集5名新被试（500+200+100）用于跨被试评估。
- **基准方法**：采用OminiControl（基于DiT的指令式图像编辑基线），分别以文本提示、语音转录文本作为条件。
- **对比方法**：
  - LoongX（仅神经信号）
  - LoongX（神经信号+语音）
  - 与上述两个OminiControl变体对比。
- **评估指标**：L1距离、L2距离、CLIP-I（编辑图与目标图语义相似度）、DINO（结构相似度）、CLIP-T（编辑图与文本指令语义相似度）。

### 4. 资源与算力

- 所有模型在8块NVIDIA H100 GPU上训练。
- 使用FLUX.1-dev预训练权重，通过LoRA（学习率1.0，权重衰减0.01）微调。
- 推理时8步，无分类器引导权重w=4。

### 5. 实验数量与充分性

- **实验组数**：包括主对比实验（2个条件×2个基线）、消融实验（信号组合6组、脑区通道5组、模块消融5种配置）、跨被试评估、编辑类型分解分析等，总计超过20组独立实验。
- **充分性**：实验设计较为全面：不仅对比了文本/语音/神经信号，还深入分析了各模态贡献、脑区功能对应性、模块必要性，并补充了跨被试泛化测试。所有结果均报告95%置信区间，统计严谨。
- **客观公平**：基线方法采用相同OminiControl框架，仅替换条件来源；消融实验严格控制变量；评估指标覆盖像素级、语义级和结构级，减少偏差。

### 6. 论文的主要结论与发现

- 神经信号可单独驱动图像编辑：LoongX（神经信号）在CLIP-I（0.6605 vs 0.6558）和DINO（0.4812 vs 0.4636）上优于文本基线，表明其能捕捉丰富视觉语义。
- 多模态信号互补：EEG提供判别性，fNIRS增强鲁棒性，PPG与运动提升稳定性；全模态融合效果最优。
- 脑区功能验证：Oz（枕叶）主导全局视觉编辑，Fpz（额极）擅长语义对齐，与神经解剖学一致。
- 神经+语音混合同优于纯文本：CLIP-T达0.2588，证明二者信息互补。
- 神经信号在低层次视觉编辑（如色相、物体移除）上表现突出，文本在高层次语义（如风格迁移）上有优势。

### 7. 优点

- **方法创新性**：首次全面整合EEG、fNIRS、PPG、运动四种信号用于指令式图像编辑，提出CS3和DGF模块有效应对异构数据。
- **数据集价值**：L-Mind是首个大规模、多模态、真实场景下的脑控图像编辑数据集，包含同步语音，促进跨模态研究。
- **实验可靠性**：多维度消融、脑区分析、跨被试验证，结果稳健且解释性强。
- **开放性与可复现性**：代码和数据集将公开，有助于社区复现与拓展。
- **应用前景**：对无障碍创作、VR/XR自然交互具有重要启示。

### 8. 不足与局限

- **被试多样性有限**：仅12名健康年轻人（外加5名），缺乏老年群体和神经疾病患者数据，泛化性待验证。
- **空间分辨率限制**：采用低密度EEG（4通道）和fNIRS（6通道），虽便于部署但可能丢失精细脑区信息。
- **复杂语义处理能力**：对抽象指令（如“科幻生物”）或非标准尺寸图像（全景图）仍有失败案例。
- **鲁棒性测试不足**：未系统评估运动伪影、传感器缺失、环境干扰等真实场景下的性能下降。
- **可解释性欠缺**：学到的潜变量与具体认知状态（如注意力水平、情感）的对应关系未明确揭示。
- **用户自适应**：当前模型为固定参数，未探索快速微调或在线适应新用户。

（完）
