# 王鸿铖 (Hongcheng Wang)

中国 · 北京 ｜ 邮箱：whc.1999@pku.edu.cn ｜ 个人主页：whcpumpkin.github.io ｜ GitHub：whcpumpkin

**求职意向**：具身大脑 / 具身智能 VLA 算法研究员（预计 2027 届博士毕业）

**关键词**：VLA (Vision-Language-Action) · 具身大脑 (Embodied Brain) · Chain-of-Thought for Embodied Agents · RL Post-training · GRPO · 长程任务规划 · Object / Demand-driven Navigation · Human-centered Embodied Decision Making

---

## 研究方向与岗位匹配

研究兴趣聚焦于**具身大脑（Embodied Brain）/ VLA 模型**：让具身 Agent 既"**会想**"——具备稳定的思维链与长程规划能力，又"**懂人**"——能够理解并适配用户的需求、偏好与习惯。围绕这一目标形成两条互补的研究主线：

**主线一 · 具身大脑的思维链推理与 RL 后训练**
研究面向具身大脑 / VLA 的 System 2 慢思考训练：在做动作之前先稳定地"想"。重点关注 GRPO 等 RL post-training 范式在 `<think>` / `<answer>` 之间的 credit assignment、思维优势估计的方差控制与 rollout 预算分配。目标是让 VLA 的高层规划模块在长程任务、复杂指令分解与可验证奖励训练下更稳、更省样本，对接 RT-2 / OpenVLA / π0 / GR00T / Helix 等 VLA 工作中"高层大脑 + 低层执行"的双系统架构。

**主线二 · 以人为中心的具身 VLA 决策**
从认知行为理论的视角出发，研究 VLA 大脑如何显式建模并利用人的潜在需求、偏好、习惯与规范，完成开放家庭场景下的个性化任务规划、物体搜索与导航。把"用户画像 / 长期记忆 / 偏好检索"作为 VLA 决策的一等条件，而非只依赖通用场景先验。该方向直接对应家庭服务机器人、人形机器人具身大脑在"千人千面"场景下的语言理解、任务分解与动作落地。

---

## 教育背景

**北京大学**，计算机科学与技术，博士研究生，2022.09 — 2027.06（预计）
导师：董豪 副教授（PKU AGIBot Lab）
研究方向：具身大脑与 VLA、思维链 RL 后训练、以人为中心的具身决策

**北京大学**，智能科学与技术，工学学士，2018.09 — 2022.07
辅修：心理学

---

## 代表性研究项目

### 1. GRPO 思维链优势估计中的树状分支策略 — *主线一*

**Paper**: *Why Tree-Style Branching Matters for Thought Advantage Estimation in GRPO*
Hongcheng Wang\*, Yinuo Huang\*, Sukai Wang, Guanghui Ren, Hao Dong (\* equal contribution)
ICML 2026, arXiv:2509.24494

- 针对大模型 RL post-training 中 `<think>` / `<answer>` 之间 credit assignment 不稳定的问题，定量分析了 GRPO 在 thought-level advantage estimation 上的方差来源。
- 提出树状分支（tree-style branching）采样视角，从理论与实验上证明：仅增加 sampled thoughts 存在方差下界，而在每个 thought 下增加 answers 采样可以持续降低方差，从而给出更稳定的 advantage 估计。
- **工业可迁移价值**：直接对应具身大脑 / VLA 在动作之前的 System 2 慢思考训练——长程任务规划、子目标拆解与"先想后动"的 RL 后训练；同样适用于 VLM / VLA 在可验证奖励下的训练稳定性与 rollout 预算分配问题。

### 2. 用户中心的个性化物体导航（UcON）— *主线二*

**Paper**: *User-Centric Object Navigation: A Benchmark with Integrated User Habits for Personalized Embodied Object Search*
Hongcheng Wang\*, Jinyu Zhu\*, Hao Dong (\* equal contribution)
ICRA 2026, arXiv:2602.06459

- 提出 UcON 基准，将"用户的物品摆放习惯"显式作为目标搜索任务的一等输入，弥补主流物体导航只用通用场景先验、忽略用户个性化信息的缺陷。
- 设计 habit retrieval 模块，使 Agent 在面对新用户时能够基于该用户的习惯条件，推断目标物体的高概率位置并据此规划探索路径。
- **工业可迁移价值**：对应家庭服务机器人 / 人形机器人具身大脑在"千人千面"场景下的个性化适配——把用户长期记忆与画像作为 VLA 决策条件，是 VLA 走向家庭真实部署的关键能力。

### 3. 多物体需求驱动导航（MO-DDN）— *主线二*

**Paper**: *MO-DDN: A Coarse-to-Fine Attribute-based Exploration Agent for Multi-Object Demand-driven Navigation*
Hongcheng Wang\*, Peiqi Liu\*, Wenzhe Cai, Mingdong Wu, Zhengyu Qian, Hao Dong (\* equal contribution)
NeurIPS 2024, arXiv:2410.03488

- 将单物体需求驱动导航扩展到多物体场景，研究 Agent 如何把一句开放式需求（如"我想喝点东西并坐下休息"）分解为一组可执行的目标物体，并考虑用户的个人偏好。
- 提出 coarse-to-fine 基于属性的探索框架，把"属性理解 → 候选目标筛选 → 导航探索"拆分为可解释的决策模块。
- **工业可迁移价值**：对应具身大脑把一句开放语言指令拆解为多个可执行 sub-goal 并交给低层执行器的能力，是 VLA 在长程、组合任务上落地的核心能力。

### 4. 需求驱动导航（DDN）— *主线二*

**Paper**: *Find What You Want: Learning Demand-conditioned Object Attribute Space for Demand-driven Navigation*
Hongcheng Wang, Andy Guan Hong Chen, Xiaoqi Li, Mingdong Wu, Hao Dong
NeurIPS 2023, arXiv:2309.08138

- 首次提出 Demand-driven Navigation 任务：Agent 接收"我渴了"这类需求指令，而非固定的物体类别名称，主动搜索能满足该需求的对象。
- 利用 LLM 抽取物体的常识属性，并通过 CLIP 对齐文本属性与视觉属性，使导航策略可以借助属性先验完成开放目标搜索。
- **工业可迁移价值**：对应 VLA "Language → Vision → Action" 链路最前端的视觉语言落地问题——从用户的自然需求出发，做语义对齐与目标 grounding，是具身大脑能否"听懂人话"的底层能力。

---

## 其他论文

- ***Learning Semantic-Agnostic and Spatial-Aware Representation for Generalizable Visual-Audio Navigation***
  Hongcheng Wang\*, Yuxuan Wang\*, Fangwei Zhong, Mingdong Wu, Jianwei Zhang, Yizhou Wang, Hao Dong (\* equal contribution)
  IEEE RA-L 2023, arXiv:2304.10773
  研究视觉-声音导航中对未见声音类别的零样本泛化，提出语义无关、空间感知的多模态表示。

---

## 技能与工程能力

- **具身大脑与 VLA**：持续跟进 RT-2 / OpenVLA / π0 / GR00T / Helix / RDT 等主流 VLA 工作；熟悉"高层具身大脑 + 低层动作执行器"双系统架构、长程任务规划与子目标拆解的研究脉络。
- **大模型 RL 后训练**：熟悉 GRPO / PPO 风格 policy optimization、verifiable reward、Chain-of-Thought RL；具备从理论方差分析、采样策略设计到训练稳定性诊断的完整研究经验，可迁移至 VLA / VLM 的 RL 后训练。
- **具身智能与机器人学习**：熟悉 Object Navigation、Demand-driven Navigation、Visual-Audio Navigation 等任务；有 AI2-THOR / ProcTHOR / Habitat 等具身模拟环境下的 benchmark 构建、Agent 训练与评测经验。
- **多模态与表示学习**：熟悉 CLIP / VLM / LLM 常识抽取与视觉-语言对齐，能将自然语言需求转化为可执行的感知与决策条件，对应 VLA 大脑的"语言-视觉"落地链路。
- **工程实现**：Python，PyTorch，多机多卡分布式训练，wandb / hydra 实验管理，ablation 与 benchmark metric 设计；多篇顶会论文均亲自完成代码与实验复现。

---

## 学术服务

担任以下顶级会议 / 期刊审稿人：
ICRA（2023）、IROS（2024）、NeurIPS（2024、2025）、ACM MM（2025）、ICLR（2025、2026）、ICML（2025、2026）、IEEE RA-L（2026）

---

## 教学与技术分享

- 北京大学《人工智能基础》课程助教，2023、2024、2025、2026 春季学期（连续 4 届）
- 北京大学《计算概论 A》课程助教，2025 秋季学期
- 知乎技术博客：《Deepseek 技术积累解读：R1 模型之前都经历了什么？》（与主线一直接相关）

---

## 联系方式

- 邮箱：whc.1999@pku.edu.cn
- 个人主页：whcpumpkin.github.io
- GitHub：github.com/whcpumpkin
- Google Scholar 用户名：Hongcheng Wang（北京大学）
