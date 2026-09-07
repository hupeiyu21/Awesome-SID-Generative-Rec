# 语义标识生成式推荐方法总表

仅收录在线阶段能够直接生成完整语义标识并确定推荐物品的方法；边界与排除方法见[单独列表](boundary-and-excluded-methods.md)。

| 方法 | 年份 | 语义标识构建 | 生成模型 | 核心贡献 | 适用场景 | 相关资源 |
|---|---:|---|---|---|---|---|
| [TIGER](../papers/tiger.md) | 2023 | RQ-VAE残差量化 | 编码器—解码器 | 将内容表示转为可生成的层次化SID | 序列推荐、冷启动 | [论文](https://papers.neurips.cc/paper_files/paper/2023/hash/20dcab0f14046a5c6b02b61da9f13229-Abstract-Conference.html) |
| [EAGER](../papers/eager.md) | 2024 | 行为/语义层次聚类 | 双流编码器—解码器 | 联合生成行为码与语义码 | 多源序列推荐 | [论文](https://doi.org/10.1145/3637528.3671775) |
| [LC-Rec](../papers/lcrec.md) | 2024 | 协同—语言语义量化 | LLM生成器 | 把协同语义注入LLM物品索引 | LLM推荐 | [论文](https://arxiv.org/abs/2311.09049) |
| [ColaRec](../papers/colarec.md) | 2024 | GNN表示层次聚类 | 编码器—解码器 | 用协同图结构学习GID | 内容增强推荐 | 未报告 |
| [LETTER](../papers/letter.md) | 2024 | RQ-VAE加三类正则 | LLM生成器 | 联合语义、协同和码多样性 | 生成式推荐 | [代码](https://github.com/Honghuibao2000/LETTER) |
| [TokenRec](../papers/tokenrec.md) | 2024 | 多码本向量量化 | LLM生成器 | 学习可组合的协同ID token | LLM推荐 | 未报告 |
| [GNPR-SID](../papers/gnprsid.md) | 2025 | RQ-VAE与多样性损失 | LLM生成器 | 将语义、地理、时间和协同信息构造成可生成 SID | 下一 POI 推荐 | [论文](https://arxiv.org/abs/2506.01375)<br>[代码](https://github.com/wds1996/GNPR-SID) |
| [OneLoc](../papers/oneloc.md) | 2025 | 视频—地理联合 token 化 | 编码器—解码器 | 用地理感知生成和偏好优化统一本地生活目标 | 本地生活推荐 | [论文](https://arxiv.org/abs/2508.14646) |
| [LGSID](../papers/lgsid.md) | 2025 | 地理属性索引与残差量化 | LLM生成器 | 用地理对齐和层次化分词增强空间一致性 | 本地生活推荐 | [论文](https://arxiv.org/abs/2511.14221) |
| [ROS](../papers/ros.md) | 2026 | 地理前缀、语义锚点与后缀 | 大语言模型 | 用移动思维链和空间奖励显式执行地理推理 | 下一 POI、跨城市迁移 | [论文](https://arxiv.org/abs/2601.04562) |
| [GeoGR](../papers/geogr.md) | 2026 | 时空协同表示与 RQ-KMeans | LLM生成器 | 面向工业规模结合时空 SID 与多阶段 LLM 对齐 | 导航与工业 POI 推荐 | [论文](https://arxiv.org/abs/2602.10411) |
| [ProGEO](../papers/progeo.md) | 2026 | RQ-KMeans与地理码本 | LLM生成器 | 用局部坐标和 Geo-RoPE 将邻近关系写入 SID | 本地生活与配送推荐 | [论文](https://arxiv.org/abs/2604.23156) |
| [Gwhere](../papers/gwhere.md) | 2026 | 多模态对比残差量化 | LLM生成器 | 融合多模态 SID 与暴露感知偏好优化实现工业部署 | 高德下一 POI 推荐 | [论文](https://arxiv.org/abs/2607.26073)<br>[代码](https://github.com/alibaba/SimCIT) |
| [LGRID](../papers/lgrid.md) | 2026 | 解耦槽位与双流残差量化 | LLM生成器 | 将地理与语义属性解耦为可解释的双流 SID | 本地生活与可解释推荐 | [论文](https://arxiv.org/abs/2607.27944) |
| [Think2Go](../papers/think2go.md) | 2026 | 沿用层次化 POI SID | 大语言模型 | 统一 SFT、推理、自纠错与自适应强化学习 | 下一 POI 推荐 | [论文](https://arxiv.org/abs/2607.28997) |
| [MiniOneRec](../papers/minionerec.md) | 2025 | 三级RQ-VAE | 仅解码器LLM | 统一规模扩展、对齐与偏好优化 | 序列与跨域推荐 | [论文](https://arxiv.org/abs/2510.24431) |
| [Align3GR](../papers/align3gr.md) | 2025 | 语义/协同双编码器与RQ-VAE | LLM生成器 | 在三层面统一对齐 | 公共与工业推荐 | [论文](https://arxiv.org/abs/2511.11255) |
| [FORGE](../papers/forge.md) | 2025 | 多模态RQ-VAE与碰撞处理 | 生成式检索器 | 提供工业SID构建与评估流程 | 工业生成式检索 | [项目](https://huggingface.co/AL-GR) |
| [RPG](../papers/rpg.md) | 2025 | 长SID与相似图 | 并行生成器 | 并行生成长语义标识 | 长SID推荐 | [论文](https://arxiv.org/abs/2506.05781) |
| [GRID](../papers/grid.md) | 2025 | RQ-VAE等分词器 | 自回归生成器 | 统一SID生成推荐实践流程 | 研究与工程实践 | 未报告 |
| [ETEGRec](../papers/etegrec.md) | 2025 | 可学习RQ-VAE | Transformer编码器—解码器 | 端到端对齐tokenizer与推荐器 | 序列推荐 | [论文](https://arxiv.org/abs/2409.05546) |
| [GFlowGR](../papers/gflowgr.md) | 2025 | 沿用现有SID | 自回归生成器 | 用生成流网络进行偏好微调 | 偏好对齐 | 未报告 |
| [GRAM](../papers/gram.md) | 2025 | 层次语义索引 | 编码器—解码器 | 多粒度语义后融合 | 语义增强推荐 | [论文](https://arxiv.org/abs/2506.01673) |
| [LLaDA-Rec](../papers/lladarec.md) | 2025 | 多头离散量化 | 离散扩散模型 | 并行去噪生成SID | 低延迟推荐 | 未报告 |
| [MMQ-v2](../papers/mmqv2.md) | 2025 | 稀疏MoE自适应量化 | 生成式推荐器 | 自适应融合行为与内容 | 多模态推荐 | 未报告 |
| [OneRec](../papers/onerec.md) | 2025 | 平衡K-means | 列表生成模型 | 统一召回与排序 | 工业会话推荐 | 未报告 |
| [SIDReasoner](../papers/sidreasoner.md) | 2026 | 语义离散量化 | 大语言模型 | 在SID生成前进行偏好推理 | 跨域与冷启动 | 未报告 |
| [S2GR](../papers/s2gr.md) | 2026 | 协同平衡RQ-VAE | 自回归生成模型 | 逐步语义引导潜空间推理 | 工业推荐 | 未报告 |
| [V-STAR](../papers/vstar.md) | 2026 | 沿用层次化SID | LLM生成器 | 按价值分配搜索预算 | 高效解码 | 未报告 |
| [GREAM](../papers/gream.md) | 2025 | RQ-KMeans残差量化 | 大语言模型 | 将显式推理与可验证强化学习结合 | 可解释推荐 | [论文](https://arxiv.org/abs/2510.20815) |
| [HiD-VAE](../papers/hidvae.md) | 2025 | 层次监督RQ-VAE | Transformer编码器—解码器 | 学习可解释且低碰撞的SID | 可解释推荐 | [论文](https://arxiv.org/abs/2508.04618) |
| [IDGenRec](../papers/idgenrec.md) | 2024 | 文本生成式ID | T5编码器—解码器 | 以文本ID对齐LLM与推荐器 | 序列推荐 | [论文](https://arxiv.org/abs/2403.19021) |
| [OneRec-Think](../papers/onerecthink.md) | 2025 | itemic token | 大语言模型 | 在生成物品标识前加入文本内推理 | 工业推荐 | [论文](https://arxiv.org/abs/2510.11639) |
| [MACRec](../papers/macrec.md) | 2025 | 跨模态RQ-VAE | 编码器—解码器 | 在量化阶段建模跨模态交互 | 多模态推荐 | [论文](https://arxiv.org/abs/2511.15122) |
| [MQL4GRec](../papers/mql4grec.md) | 2025 | 多模态RQ-VAE | 编码器—解码器 | 以量化语言促进跨域迁移 | 多模态跨域 | 未报告 |
| [GenCDR](../papers/gencdr.md) | 2025 | 共享RQ-VAE与动态路由 | 编码器—解码器 | 自适应融合通用与域特定语义 | 跨域推荐 | [论文](https://arxiv.org/abs/2511.08006) |
| [GMC](../papers/gmc.md) | 2025 | 共享多级RQ-VAE | 编码器—解码器 | 以共享SID统一多目标跨域推荐 | 多目标跨域 | [论文](https://arxiv.org/abs/2507.12871) |
