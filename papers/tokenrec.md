---
论文标题: "TokenRec: Learning to Tokenize ID for LLM-based Generative Recommendation"
方法简称: "TokenRec"
中文名称: "面向 LLM 生成推荐的 ID 分词"
年份: 2024
发表场所: "TKDE 投稿稿"
范围判断: "核心方法"
论文链接: "未报告"
代码链接: "未发现公开代码"
架构图: "../assets/architectures/tokenrec.png"
标签: ["多码本量化", "ID分词", "LLM推荐", "生成式检索"]
---

# TokenRec：面向 LLM 生成推荐的 ID 分词

> TokenRec 用掩码向量量化 tokenizer 将用户和物品 ID 转为多 token 表示，增强 LLM 对协同结构的建模能力。

## 方法架构

![方法架构图](../assets/architectures/tokenrec.png)

*图源：原论文，图2。图片使用许可待核实。*

## 研究动机与问题定义

原子 ID 缺乏语义且词表规模随物品数增长，多 token 表示又需要合理分配协同信息。TokenRec 学习 LLM 兼容的 ID tokenization，并直接用于生成式推荐。

## TL;DR（核心摘要）

`交互图与ID → 多码本量化 → 用户/物品 token → LLM生成 → 推荐物品`

方法用 K-way encoder 和掩码向量量化器学习物品 token，并用 K-to-1 decoder 重构原始表示；用户也可通过 MQ-tokenizer 表示。LLM 根据用户历史生成物品 token 序列，完成匹配并得到 Top-K 物品。

## 方法设计速览

| 组成部分 | 具体设计 |
|---|---|
| 使用信息 | 用户—物品交互与高阶协同结构 |
| 信息融入位置 | 向量数据库、tokenizer 和生成输入 |
| 语义标识构建 | 掩码向量量化与多码本编码 |
| 语义标识结构 | K 个离散 token 的序列 |
| 生成模型 | LLM 生成推荐器 |
| 训练方式 | tokenizer 重构与生成式推荐训练 |
| 解码方式 | 自回归 token 生成 |
| 适用场景 | LLM 生成式推荐与新物品泛化 |

## 方法设计

### 2-A 记号与整体框架
TokenRec 将用户和物品表示为可组合的多 token code，并用 LLM 进行生成式推荐。物品 token 既用于表示物品，也作为生成目标；用户 tokenizer 可将用户协同表示转成兼容 token。

### 2-B 掩码向量量化 tokenizer
K-way encoder 为一个物品生成多个潜向量，掩码向量量化器从多个 codebook 中选择离散 token。K-to-1 decoder 重构原始表示，使不同 code 的组合仍保留协同信息，并通过高阶交互增强区分度。

### 2-C 生成式检索
用户历史先替换为物品 token 序列，LLM 自回归生成下一物品 token。生成结果与 item code 匹配后得到 Top-K 物品；训练同时考虑 tokenizer 重构和推荐生成目标。

### 2-D 效率与泛化
论文分析新用户/物品、codebook 规模、效率和消融，重点说明多 token 表示相对原子 ID 的词表与泛化优势。

## 实验结论

- TokenRec 在多个数据集上改善了生成推荐效果。
- 多码本 tokenizer 带来更好的效率与泛化能力。

## 局限性与研究定位


### 局限性
- 向量数据库与多码本维护增加工程依赖。
- 动态用户/物品更新和大规模在线延迟仍需更多验证。


### 研究定位
TokenRec 的贡献是把协同 ID 学习为可组合 token，适合放在“LLM 物品分词与协同表示”章节。

## 相关资源

- 论文原文链接未报告。
- 暂未发现公开代码。

## 标签

`多码本量化` · `ID分词` · `LLM推荐` · `生成式检索`
