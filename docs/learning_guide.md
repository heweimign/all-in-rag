# all-in-rag 学习指南

欢迎来到 **all-in-rag** 项目学习指南！本指南将帮助你系统地学习 RAG（Retrieval-Augmented Generation）技术。

---

## 📚 项目概览

本项目包含：
- **11 个章节**的理论文档（`docs/`）
- **9 个实践模块**的代码示例（`code/C1-C9`）
- **完整的数据集**和配置文件
- **生产级系统实现**

---

## 🎯 不同学习路径

### 1️⃣ 快速入门路径（1 周）
**适合**：快速了解 RAG 概念和基本实现

- **Day 1-2**: Chapter 1 + C1 代码
  - 理解 RAG 基本概念
  - 跑通 LangChain 和 LlamaIndex 示例

- **Day 3-4**: Chapter 2 + C2 代码
  - 学习数据加载和文本分块
  - 实践不同的分块策略

- **Day 5-7**: Chapter 3 + C3 代码（基础部分）
  - 理解向量嵌入和检索
  - 使用 FAISS 和 Milvus

**学习目标**：能够实现一个基础的 RAG 系统

---

### 2️⃣ 系统学习路径（4-6 周）
**适合**：深入掌握 RAG 技术栈

#### 第一阶段：基础篇（2 周）
- Week 1: Chapter 1-2 + C1-C2
- Week 2: Chapter 3 + C3

#### 第二阶段：进阶篇（2 周）
- Week 3: Chapter 4 + C4
- Week 4: Chapter 5-6 + C5-C6

#### 第三阶段：高级篇（2 周）
- Week 5: Chapter 8 + C8
- Week 6: Chapter 9 + Chapter 11 + C9

**学习目标**：全面掌握 RAG 技术，能设计生产级系统

---

### 3️⃣ 实战导向路径（3-4 周）
**适合**：快速上手实际项目

- **Week 1**: C1 → C2 → C3（基础流程）
- **Week 2**: C4（高级检索技术）
- **Week 3**: C8（完整系统实现）
- **Week 4**: 实战项目开发

**学习目标**：能够独立开发 RAG 应用

---

### 4️⃣ 面向面试路径（2-3 周）
**适合**：准备面试的学习者

详见：[面向面试的学习计划](../learning_plan.md)

**重点**：
- 核心概念理解
- 高级技术掌握（混合搜索、Reranking、GraphRAG）
- 系统设计能力
- 面试常见问题准备

---

### 5️⃣ GraphRAG 专精路径（2-3 周）
**适合**：专注知识图谱 + RAG

- **Week 1**: C1 → C3（基础）
- **Week 2**: Chapter 11 + Neo4j 实践
- **Week 3**: Chapter 9 + C9（GraphRAG）

**学习目标**：掌握知识图谱与 RAG 的结合

---

## 📖 章节详解

### Chapter 1: RAG 入门
**文档位置**：`docs/chapter1/`

**核心内容**：
- RAG 技术介绍和发展历程
- 环境准备和工具安装
- 第一个 RAG 应用

**代码示例**：`code/C1/`
- `01_langchain_example.py` - LangChain 基础
- `02_llamaIndex_example.py` - LlamaIndex 基础

**学习重点**：
- 理解 RAG 的核心思想
- 掌握基本的开发环境设置
- 熟悉两大主流框架

**预计时间**：2-3 天

---

### Chapter 2: 数据处理
**文档位置**：`docs/chapter2/`

**核心内容**：
- 数据加载：PDF、Word、网页等
- 文本分块策略：固定长度、递归、语义

**代码示例**：`code/C2/`
- `01_unstructured_example.py` - Unstructured 框架
- `02_character_splitter.py` - 字符分割器
- `03_recursive_character_splitter.py` - 递归分割 ⭐
- `04_semantic_chunker.py` - 语义分块 ⭐

**学习重点**：
- 不同数据源的加载方法
- 分块策略的选择和影响
- Chunk 大小的权衡

**预计时间**：2-3 天

**面试重点**：
- 为什么需要分块？
- 如何选择分块策略？
- Chunk 重叠的作用？

---

### Chapter 3: 向量与索引
**文档位置**：`docs/chapter3/`

**核心内容**：
- 向量嵌入原理
- 多模态嵌入（文本、图像）
- 向量数据库对比
- Milvus 实践
- 索引优化

**代码示例**：`code/C3/`
- `01_bge_visualized.py` - BGE 模型可视化
- `02_langchain_faiss.py` - FAISS 向量库
- `03_llamaindex_vector.py` - LlamaIndex 向量索引
- `04_multi_milvus.py` - Milvus 实践 ⭐
- `05_sentence_window_retrieval.py` - 句子窗口检索 ⭐⭐
- `06_recursive_retrieval.py` - 递归检索 ⭐⭐
- `07_recursive_retrieval_v2.py` - 递归检索优化

**学习重点**：
- 向量嵌入的原理和选择
- 不同向量数据库的对比
- 高级检索技术（窗口、递归）

**预计时间**：5-7 天

**面试重点**：
- Embedding 模型如何选择？
- 向量相似度计算方法？
- 句子窗口检索的优势？
- 递归检索的应用场景？

---

### Chapter 4: 高级检索技术 ⭐⭐⭐
**文档位置**：`docs/chapter4/`

**核心内容**：
- 混合搜索（Hybrid Search）
- 查询构建和重写
- Text2SQL
- 高级检索技术（Reranking、Routing）

**代码示例**：`code/C4/`
- `01_hybrid_search.py` - 混合搜索 ⭐⭐⭐
- `02_text_to_metadata_filter.py` - 元数据过滤
- `03_text2sql_demo.py` - Text2SQL ⭐⭐
- `05_llm_based_routing.py` - LLM 路由 ⭐⭐
- `06_embedding_based_routing.py` - Embedding 路由
- `07_rerank_and_refine.py` - 重排序 ⭐⭐⭐

**学习重点**：
- 混合搜索的实现和优势
- Reranking 的作用和模型
- 查询路由的设计
- Text2SQL 的实现

**预计时间**：5-7 天

**面试重点**：
- 为什么需要混合搜索？
- BM25 算法原理？
- Reranking 使用什么模型？
- 如何设计多数据源路由？

---

### Chapter 5: 格式化生成
**文档位置**：`docs/chapter5/`

**核心内容**：
- 结构化输出
- Function Calling
- Pydantic 应用

**代码示例**：`code/C5/`
- `01_pydantic.py` - Pydantic 验证
- `02_function_calling_example.py` - 函数调用

**学习重点**：
- 如何确保输出格式
- Function Calling 的应用

**预计时间**：2-3 天

---

### Chapter 6: 系统评估
**文档位置**：`docs/chapter6/`

**核心内容**：
- RAG 评估指标
- 评估方法论
- 常用工具

**代码示例**：`code/C6/`
- `01_llamaindex_evaluation_example.py` - 评估示例

**学习重点**：
- RAG 系统的评估维度
- 常见评估指标
- 如何改进系统

**预计时间**：2-3 天

**面试重点**：
- 如何评估 RAG 系统质量？
- 常见问题和解决方案？

---

### Chapter 8: 完整 RAG 系统 ⭐⭐
**文档位置**：`docs/chapter8/`

**核心内容**：
- 系统架构设计
- 模块化实现
- 数据准备流程
- 索引和检索优化
- 生成系统集成

**代码示例**：`code/C8/`
- `main.py` - 主程序
- `config.py` - 配置管理
- `rag_modules/` - 模块化实现
  - `data_preparation.py`
  - `index_construction.py`
  - `retrieval_optimization.py`
  - `generation_integration.py`

**学习重点**：
- 生产级系统架构
- 模块化设计
- 性能优化

**预计时间**：5-7 天

**面试重点**：
- 如何设计 RAG 系统架构？
- 各模块的职责和接口？
- 性能优化策略？

---

### Chapter 9 + 11: GraphRAG ⭐⭐⭐
**文档位置**：
- `docs/chapter9/` - Graph RAG
- `docs/chapter11/` - 知识图谱和 Neo4j

**核心内容**：
- 知识图谱基础
- Neo4j 数据库
- GraphRAG 架构
- 图数据建模
- 智能查询路由

**代码示例**：`code/C9/`
- `main.py` - GraphRAG 主程序
- `rag_modules/` - GraphRAG 模块
  - `graph_data_preparation.py`
  - `graph_indexing.py`
  - `graph_rag_retrieval.py`
  - `hybrid_retrieval.py`
  - `intelligent_query_router.py`

**学习重点**：
- 知识图谱 + RAG 的结合
- Neo4j 基本操作
- GraphRAG 优势

**预计时间**：5-7 天

**面试重点**：
- GraphRAG 和传统 RAG 的区别？
- 知识图谱的应用场景？
- 如何设计图谱 Schema？

---

## 💡 学习建议

### 理论与实践结合
```
1. 先看文档（30分钟）- 理解原理
2. 运行代码（30分钟）- 观察效果
3. 修改代码（30分钟）- 实验验证
4. 总结思考（30分钟）- 深度理解
```

### 循序渐进
- 不要跳过基础章节
- 确保理解了再往下走
- 遇到问题及时记录和思考

### 动手实践
- 运行每一个代码示例
- 尝试修改参数观察变化
- 实现自己的小项目

### 建立知识体系
- 绘制思维导图
- 建立概念关联
- 定期复习总结

### 面试准备
- 用自己的话解释概念
- 准备项目经验描述
- 练习常见面试问题

---

## 📊 学习里程碑

### 🎯 里程碑 1：基础 RAG 流程
**完成标志**：
- ✅ 理解 RAG 核心概念
- ✅ 能实现数据加载和分块
- ✅ 能实现向量化和检索
- ✅ 能实现完整的 RAG 流程

**涉及章节**：Chapter 1-3, C1-C3

---

### 🎯 里程碑 2：高级检索技术
**完成标志**：
- ✅ 掌握混合搜索
- ✅ 理解 Reranking
- ✅ 了解查询路由
- ✅ 掌握 Text2SQL

**涉及章节**：Chapter 4, C4

---

### 🎯 里程碑 3：完整系统实现
**完成标志**：
- ✅ 理解系统架构设计
- ✅ 掌握模块化开发
- ✅ 能设计生产级系统
- ✅ 了解性能优化

**涉及章节**：Chapter 8, C8

---

### 🎯 里程碑 4：GraphRAG 掌握
**完成标志**：
- ✅ 理解知识图谱基础
- ✅ 掌握 Neo4j 操作
- ✅ 理解 GraphRAG 架构
- ✅ 能实现图谱 + RAG

**涉及章节**：Chapter 9, Chapter 11, C9

---

## 🛠️ 学习工具推荐

### 开发环境
- Python 3.8+
- Jupyter Notebook / VS Code
- Git

### 必备库
- LangChain
- LlamaIndex
- FAISS
- Milvus
- Neo4j

### 学习辅助
- 思维导图工具（XMind、MindNode）
- 笔记工具（Notion、Obsidian）
- 代码管理（GitHub）

---

## 📞 获取帮助

### Learning Coach
项目内置 Learning Coach 角色，可以：
- 引导你深入思考
- 记录学习进度
- 分析学习模式
- 提供学习建议

**激活方式**：使用 PromptX 激活 `learning-coach` 角色

### 社区资源
- 项目 Issues：提问和讨论
- 文档：完整的理论说明
- 代码注释：详细的实现说明

---

## 📈 进度追踪

建议使用 `learning_plan.md` 来追踪学习进度和记录笔记。

---

*最后更新：2025-10-23*

