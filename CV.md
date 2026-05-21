<div align="center">

<h1>王鸿铖 · Hongcheng Wang</h1>

北京大学计算机科学与技术博士研究生（预计 2027 届）<br>
中国 · 北京 ｜ [whc.1999@pku.edu.cn](mailto:whc.1999@pku.edu.cn) ｜ [whcpumpkin.github.io](https://whcpumpkin.github.io) ｜ [GitHub](https://github.com/whcpumpkin)

**求职意向**：具身大脑 / 具身智能 VLA 算法研究员

</div>

---

## 研究概述

我的研究聚焦于**具身大脑（Embodied Brain）/ VLA 模型**，核心目标是让具身 Agent 在行动前能够稳定地“想”，并在开放家庭场景中真正“懂人”。

- **思维链推理与 RL 后训练**：研究面向 VLA / VLM 的 System 2 慢思考训练，重点关注 GRPO、Chain-of-Thought RL、verifiable reward、credit assignment 与 rollout 预算分配。
- **以人为中心的具身决策**：研究机器人如何显式建模用户需求、偏好、习惯和长期记忆，用于个性化任务规划、物体搜索与导航。
- **关键词**：VLA · Embodied Brain · GRPO · RL Post-training · Object Navigation · Demand-driven Navigation · Human-centered Embodied AI

---

## 教育背景

- **北京大学** ｜ 计算机科学与技术，博士研究生 ｜ 2022.09 — 2027.06（预计）
  - 导师：董豪 副教授
  - 研究方向：具身大脑与 VLA、思维链 RL 后训练、以人为中心的具身决策

- **北京大学** ｜ 智能科学与技术，理学学士 ｜ 2018.09 — 2022.07
  - 辅修：心理学

---

## 代表性研究

### Why Tree-Style Branching Matters for Thought Advantage Estimation in GRPO

Hongcheng Wang\*, Yinuo Huang\*, Sukai Wang, Guanghui Ren, Hao Dong（\* equal contribution）<br>
**ICML 2026** · [arXiv:2509.24494](https://arxiv.org/abs/2509.24494)

- 分析大模型 RL post-training 中 `<think>` / `<answer>` 之间 credit assignment 不稳定的问题，定位 thought-level advantage estimation 的主要方差来源。
- 提出 tree-style branching 采样视角，证明仅增加 sampled thoughts 存在方差下界，而在每个 thought 下增加 answers 采样可以持续降低估计方差。

### User-Centric Object Navigation: A Benchmark with Integrated User Habits for Personalized Embodied Object Search

Hongcheng Wang\*, Jinyu Zhu\*, Hao Dong（\* equal contribution）<br>
**ICRA 2026** · [arXiv:2602.06459](https://arxiv.org/abs/2602.06459)

- 提出 UcON 基准，将用户的物品摆放习惯作为目标搜索任务的一等输入，补足传统物体导航只依赖通用场景先验的问题。
- 设计 habit retrieval 模块，使 Agent 能基于新用户的习惯条件推断目标物体的高概率位置，并据此规划探索路径。

### MO-DDN: A Coarse-to-Fine Attribute-based Exploration Agent for Multi-Object Demand-driven Navigation

Hongcheng Wang\*, Peiqi Liu\*, Wenzhe Cai, Mingdong Wu, Zhengyu Qian, Hao Dong（\* equal contribution）<br>
**NeurIPS 2024** · [arXiv:2410.03488](https://arxiv.org/abs/2410.03488)

- 将需求驱动导航扩展到多物体场景，使 Agent 能把开放式需求分解为一组可执行目标物体，并考虑用户个人偏好。
- 提出 coarse-to-fine 属性探索框架，将“属性理解、候选目标筛选、导航探索”拆分为可解释的决策模块。

### Find What You Want: Learning Demand-conditioned Object Attribute Space for Demand-driven Navigation

Hongcheng Wang, Andy Guan Hong Chen, Xiaoqi Li, Mingdong Wu, Hao Dong<br>
**NeurIPS 2023** · [arXiv:2309.08138](https://arxiv.org/abs/2309.08138)

- 首次提出 Demand-driven Navigation 任务：Agent 接收“我渴了”这类需求指令，而非固定物体类别名称，主动搜索能满足该需求的对象。
- 利用 LLM 抽取物体常识属性，并通过 CLIP 对齐文本属性与视觉属性，使导航策略能够借助属性先验完成开放目标搜索。

---

## 其他论文

**[Learning Semantic-Agnostic and Spatial-Aware Representation for Generalizable Visual-Audio Navigation](https://arxiv.org/abs/2304.10773)**<br>
Hongcheng Wang\*, Yuxuan Wang\*, Fangwei Zhong, Mingdong Wu, Jianwei Zhang, Yizhou Wang, Hao Dong（\* equal contribution）<br>
**IEEE RA-L 2023**

- 研究视觉-声音导航中对未见声音类别的零样本泛化，提出语义无关、空间感知的多模态表示。

---

## 技能与工程能力

- **具身智能与 VLA**：熟悉 RT-2 / OpenVLA / π0 / GR00T / Helix / RDT 等 VLA 工作，理解高层规划模块与低层动作执行器的双系统架构。
- **RL 后训练与推理优化**：熟悉 GRPO / PPO 风格 policy optimization、Chain-of-Thought RL、verifiable reward 与训练稳定性分析。
- **机器人学习与仿真环境**：熟悉 Object Navigation、Demand-driven Navigation、Visual-Audio Navigation；有 AI2-THOR / ProcTHOR / Habitat 下的 benchmark 构建、Agent 训练与评测经验。
- **多模态与表示学习**：熟悉 CLIP / VLM / LLM 常识抽取与视觉-语言对齐，能将自然语言需求转化为可执行的感知与决策条件。
- **工程实现**：Python、PyTorch、多机多卡分布式训练、wandb / hydra 实验管理、ablation 与 benchmark metric 设计；多篇顶会论文均亲自完成代码与实验复现。

---

## 学术服务

审稿人：ICRA（2023）、IROS（2024）、NeurIPS（2024、2025）、ACM MM（2025）、ICLR（2025、2026）、ICML（2025、2026）、IEEE RA-L（2026）

---

## 教学与技术分享

- 北京大学《人工智能基础》课程助教，2023、2024、2025、2026 春季学期（连续 4 届）
- 北京大学《计算概论 A》课程助教，2025 秋季学期
- 知乎技术博客：《Deepseek 技术积累解读：R1 模型之前都经历了什么？》
