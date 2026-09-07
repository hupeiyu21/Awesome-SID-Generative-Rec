# Awesome Semantic-ID Generative Recommendation

面向中文研究者的语义标识生成式推荐论文整理。详细介绍见[论文卡片](papers/)，结构化字段见[方法总表](tables/all-methods.md)。

## 核心方法

### TIGER｜生成式检索推荐
[论文](papers/tiger.md) · NeurIPS 2023  ·  用 RQ-VAE 将物品内容编码为层次化 SID，再由编码器—解码器直接生成 SID。

![TIGER 方法架构图](assets/architectures/tiger.png)

### EAGER｜行为—语义协同双流生成式推荐
[论文](papers/eager.md) · KDD 2024  ·  用行为码与语义码双流生成并在内部合并候选。

![EAGER 方法架构图](assets/architectures/eager.png)

### MiniOneRec｜可扩展生成式推荐框架
[论文](papers/minionerec.md) · 2025  ·  统一 SID 对齐、语言模型扩展和推荐偏好强化学习。

![MiniOneRec 方法架构图](assets/architectures/minionerec.png)

### LC-Rec｜协同语义融合的语言模型推荐
[论文](papers/lcrec.md) · 2024  ·  将语言语义与协同语义共同编码为可生成的物品索引。

![LC-Rec 方法架构图](assets/architectures/lcrec.png)

### Align3GR｜多层统一对齐生成式推荐
[论文](papers/align3gr.md) · 2025  ·  在 token、行为建模和偏好三个层面对齐语义与协同信息。

![Align3GR 方法架构图](assets/architectures/align3gr.png)

### ColaRec｜基于内容的协同生成推荐
[论文](papers/colarec.md) · CIKM 2024  ·  用 GNN 协同表示构造 GID，并联合内容与推荐目标。

![ColaRec 方法架构图](assets/architectures/colarec.png)

### FORGE｜工业数据集语义标识构建
[论文](papers/forge.md) · 2025  ·  面向工业交互数据融合多模态内容和协同关系构造 SID。

![FORGE 方法架构图](assets/architectures/forge.png)

### RPG｜并行生成长语义标识
[论文](papers/rpg.md) · KDD 2025  ·  用多 token 预测和标识图传播降低长 SID 生成成本。

![RPG 方法架构图](assets/architectures/rpg.png)

### GRID｜语义标识生成式推荐实践框架
[论文](papers/grid.md) · 2025  ·  整理 SID 分词、生成、约束解码和评估流程。

### ETEGRec｜端到端可学习物品分词生成推荐
[论文](papers/etegrec.md) · SIGIR 2025  ·  让物品 tokenizer 接受推荐目标的端到端反馈。

![ETEGRec 方法架构图](assets/architectures/etegrec.png)

### GFlowGR｜生成流网络生成式推荐微调
[论文](papers/gflowgr.md) · 2025  ·  把 SID 生成轨迹建模为生成流网络。

![GFlowGR 方法架构图](assets/architectures/gflowgr.png)

### GRAM｜语义感知多粒度后融合生成推荐
[论文](papers/gram.md) · 2025  ·  在解码端后融合多粒度语义与协同信息。

![GRAM 方法架构图](assets/architectures/gram.png)

### LETTER｜生成式推荐的可学习物品分词
[论文](papers/letter.md) · CIKM 2024  ·  用语义、协同和多样性目标学习物品标识。

![LETTER 方法架构图](assets/architectures/letter.png)

### LLaDA-Rec｜离散扩散并行语义标识生成
[论文](papers/lladarec.md) · 2025  ·  以离散扩散迭代去噪替代逐 token 自回归生成。

![LLaDA-Rec 方法架构图](assets/architectures/lladarec.png)

### MMQ-v2｜自适应行为挖掘语义标识学习
[论文](papers/mmqv2.md) · 2025  ·  用稀疏混合专家自适应融合内容与行为信号。

![MMQ-v2 方法架构图](assets/architectures/mmqv2.png)

### OneRec｜检索排序一体化生成式推荐
[论文](papers/onerec.md) · 2025  ·  以生成列表统一召回与排序，并进行迭代偏好对齐。

![OneRec 方法架构图](assets/architectures/onerec.png)

### SIDReasoner｜基于语义标识推理的生成式推荐
[论文](papers/sidreasoner.md) · 2026  ·  在生成最终 SID 前显式推理用户偏好。

![SIDReasoner 方法架构图](assets/architectures/sidreasoner.png)

### S2GR｜潜空间逐步语义引导推理
[论文](papers/s2gr.md) · 2026  ·  在 SID 生成每一步注入语义引导信号。

![S2GR 方法架构图](assets/architectures/s2gr.png)

### V-STAR｜价值引导结构化采样与优化
[论文](papers/vstar.md) · 2026  ·  按候选价值分配生成搜索预算。

![V-STAR 方法架构图](assets/architectures/vstar.png)

### TokenRec｜面向 LLM 生成推荐的 ID 分词
[论文](papers/tokenrec.md) · 2024  ·  用多码本量化将协同 ID 学习为可组合 token。

![TokenRec 方法架构图](assets/architectures/tokenrec.png)

## POI 与本地生活推荐

### GNPR-SID｜基于语义标识的生成式下一兴趣点推荐
[论文](papers/gnprsid.md) · KDD 2025  ·  融合语义、地理、时间和协同信号构造 SID，并直接生成下一 POI。

![GNPR-SID 方法架构图](assets/architectures/gnprsid.png)

### OneLoc｜地理感知本地生活生成式推荐
[论文](papers/oneloc.md) · 2025  ·  结合地理感知 SID、位置注意力、邻域提示和多目标偏好优化。

![OneLoc 方法架构图](assets/architectures/oneloc.png)

### LGSID｜大语言模型对齐的地理物品分词
[论文](papers/lgsid.md) · 2025  ·  先进行地理 LLM 对齐，再构造层次化地理 SID。

![LGSID 方法架构图](assets/architectures/lgsid.png)

### ROS｜空间推理增强的生成式下一兴趣点推荐
[论文](papers/ros.md) · 2026  ·  通过空间 SID、移动思维链和空间强化学习进行地理约束推理。

![ROS 方法架构图](assets/architectures/ros.png)

### GeoGR｜工业规模时空感知生成式 POI 推荐
[论文](papers/geogr.md) · 2026  ·  用时空协同 SID 和多阶段 LLM 对齐支持工业级下一 POI 推荐。

![GeoGR 方法架构图](assets/architectures/geogr.png)

### ProGEO｜距离感知地理码本
[论文](papers/progeo.md) · 2026  ·  用局部坐标和 Geo-RoPE 将地理邻近关系融入 SID。

![ProGEO 方法架构图](assets/architectures/progeo.png)

### Gwhere｜高德生成式下一兴趣点推荐
[论文](papers/gwhere.md) · RecSys 2026  ·  融合多模态 SID、时空语料和暴露感知偏好优化。

![Gwhere 方法架构图](assets/architectures/gwhere.png)

### LGRID｜生成解耦的可解释本地生活推荐
[论文](papers/lgrid.md) · 2026  ·  将地理与语义属性解耦并分别量化为双流 SID。

![LGRID 方法架构图](assets/architectures/lgrid.png)

### Think2Go｜带大语言模型推理的生成式下一兴趣点推荐
[论文](papers/think2go.md) · KDD 2026  ·  统一 SFT、推理、自纠错和自适应强化学习。

![Think2Go 方法架构图](assets/architectures/think2go.png)

## 边界与排除方法

- [ActionPiece](papers/actionpiece.md)：压缩动作序列 token，不构建并直接生成完整物品 SID。
- [LIGER](papers/liger.md)：生成 SID 后仍依赖稠密检索和最终排序。
- [GRLM](papers/grlm.md)：Term ID 无法精确匹配时仍依赖候选库结构化评分。
- [VQ-Rec](papers/vqrec.md)：量化 code 只作为表示，最终通过全物品评分排序。

## 新增论文

### GREAM｜基于大语言模型的生成式推理推荐
[论文](papers/gream.md) · 2025  ·  将协同—语义对齐、推理课程学习和 SRPO 结合，直接生成物品标识。

![GREAM 方法架构图](assets/architectures/gream.png)

### HiD-VAE｜层次解耦语义标识可解释生成推荐
[论文](papers/hidvae.md) · 2025  ·  用层次监督和唯一性损失学习可解释、低碰撞 SID。

![HiD-VAE 方法架构图](assets/architectures/hidvae.png)

### IDGenRec｜文本 ID 学习的 LLM—推荐系统对齐
[论文](papers/idgenrec.md) · SIGIR 2024  ·  以文本 ID 作为 LLM 与推荐器之间的接口。

![IDGenRec 方法架构图](assets/architectures/idgenrec.png)

### OneRec-Think｜文本内推理生成式推荐
[论文](papers/onerecthink.md) · 2025  ·  在生成 itemic token 前加入偏好理由和强化学习。

![OneRec-Think 方法架构图](assets/architectures/onerecthink.png)

### GRLM｜基于结构化术语标识的原生 LLM 生成推荐
[论文](papers/grlm.md) · 2026  ·  用原生语言词表生成 Term ID，但最终落地仍依赖候选库结构化匹配。

![GRLM 方法架构图](assets/architectures/grlm.png)

### MACRec｜多方面跨模态量化生成式推荐
[论文](papers/macrec.md) · 2025  ·  在 SID 量化和生成训练中同时建模文本、图像及其交互。

![MACRec 方法架构图](assets/architectures/macrec.png)

### MQL4GRec｜生成式推荐的多模态量化语言
[论文](papers/mql4grec.md) · ICLR 2025  ·  将多域多模态内容翻译为统一的离散量化语言。

![MQL4GRec 方法架构图](assets/architectures/mql4grec.png)

### GenCDR｜带自适应语义分词的跨域生成推荐
[论文](papers/gencdr.md) · 2025  ·  用共享 SID、域特定适配器和动态路由实现跨域生成。

![GenCDR 方法架构图](assets/architectures/gencdr.png)

### GMC｜生成式多目标跨域推荐
[论文](papers/gmc.md) · 2025  ·  以共享 SID 连接多个领域，并用 LoRA 适配领域偏好。

![GMC 方法架构图](assets/architectures/gmc.png)

### VQ-Rec｜可迁移序列推荐的向量量化物品表示
[论文](papers/vqrec.md) · WWW 2023  ·  量化 code 只作为序列推荐器的物品表示，不直接生成完整 SID。

## 维护方式

- [论文详细卡片](papers/)
- [结构化方法总表](tables/all-methods.md)
- [边界与排除方法说明](tables/boundary-and-excluded-methods.md)
