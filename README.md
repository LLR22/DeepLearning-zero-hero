# 🚀 DeepLearning Zero to Hero

> From Linear Layers to LLMs and Agents, implemented from scratch with PyTorch.

当前的深度学习领域发展得非常快，各类教程、论文解读、开源项目和大模型工具层出不穷。与此同时，PyTorch、Transformers、Diffusers、LangChain 等基础库和工程框架也越来越完善。很多时候，我们只需要在现有代码上改一改参数、换一换模块、拼一拼 pipeline，就可以搭出一个看起来很完整的深度学习项目

这当然是一件好事。效率被大幅提高，更多人可以进入 AI，更多想法可以更快落地。

但它也带来了一个很现实的问题：我们可能跑过很多模型，却没有真正写过一个线性层；我们可能调过很多 transformer 参数，却不清楚 attention 里的 Q、K、V 是怎样流动的；我们可能完成了许多项目，却仍然对 normalization、loss、optimizer、training pipeline 这些基础模块只有模糊印象。

所以我想，在这样一个效率爆炸的时代，也许更需要慢慢去做一些看起来“不那么高效”的事情：把深度学习里那些重要的模块拆开，从原理走到代码，从最小实现走到完整系统，一点一点弄明白 ✨

这个项目就是基于这样的想法建立的：希望对当前网络上深度学习资源“不够系统”“停留在原理介绍”“缺少代码实现细节”的问题做一点小小的补充。对于刚入门的同学，可以从最简单的线性层、激活函数、损失函数开始，逐步建立完整的知识体系；对于已经做过一些深度学习项目的同学，也可以回过头来看看这些常用模块到底是怎么实现的。

简单来说，这个仓库想做的事情是：

> 不只是会用深度学习，而是尽量把它写明白、讲清楚、串起来。

## 🌱 项目目标

- 从基础组件开始，理解神经网络是怎么一层层搭起来的。
- 从经典模型出发，学习 CNN、RNN、ResNet、Transformer、SSM 等架构的实现思路。
- 从训练流程入手，理解一个模型从数据到收敛中间经历了什么。
- 从 Transformer 继续往前，进入现代 LLM 的核心机制。
- 在 LLM 之上，继续探索 Agent、RAG、Tool Calling 等前沿应用。

## 🧭 项目结构

```text
DeepLearning-zero-hero
|
├── 01-foundations        # 神经网络基础组件
├── 02-architectures      # 常见模型架构
├── 03-training           # 模型训练方法与实验流程
├── 04-llm                # 从 Transformer 到现代 LLM
└── 05-agents             # LLM 之上的 Agent 系统
```

## 🧩 01-foundations

这一部分会介绍深度学习中最基础、最常见、也最值得亲手实现的模块。它们就像积木一样，后面几乎所有复杂模型都会反复用到。

- Linear / MLP
- Activation
- Normalization
- Loss Function
- Attention
- Backpropagation 与 Autograd 直觉

## 🏗️ 02-architectures

这一部分会从完整模型架构出发，介绍常见算法的原理和代码实现。重点不是只知道模型名字，而是理解它们为什么这样组织计算。

- CNN
- ResNet
- RNN / LSTM / GRU
- Transformer
- SSM

## 🔥 03-training

模型写出来只是第一步，真正让模型学起来，还需要训练流程、优化策略、实验组织和评估方法。这一部分会关注“怎么把模型训好”。

- Training Pipeline
- Optimizer 与 Scheduler
- Evaluation
- Contrastive Learning / CLIP
- GAN
- 实验记录与复现

## 🤖 04-llm

这一部分会从 Transformer 出发，逐步走向现代大语言模型。我们会尽量把 LLM 中看起来复杂的部分拆成可以理解、可以实现的小模块。

- Tokenization
- Transformer Block
- Pretraining / SFT / Alignment
- Inference 与 KV Cache
- Prompting 与模型使用模式

## 🛠️ 05-agents

当 LLM 不再只是一个文本生成器，而是开始调用工具、检索知识、规划步骤、执行任务时，就进入了 Agent 的范围。这一部分会关注 LLM 之上的系统设计。

- Tool Calling
- Memory
- Planning
- RAG
- Multi-Agent
- Agent Workflow

## 💡 为什么要从头实现

因为“会用”和“懂得”之间，常常隔着一段亲手写过的距离。

从头实现并不是为了重复造轮子，也不是为了拒绝成熟框架。恰恰相反，只有真正理解了底层模块是如何工作的，之后再使用 PyTorch、Transformers 或各种 AI 工程框架时，才会更清楚自己在调用什么、修改什么、调试什么。

很多框架接口看起来像魔法，但魔法的背后，依然是 tensor、矩阵乘法、梯度、优化和一层层模块组合起来的系统。

## 📌 当前状态

项目正在持续建设中。后续会逐步补充每个部分的内容，包括：

- 原理说明
- 最小可运行代码
- 关键张量形状
- 训练与实验示例
- 常见问题和延伸阅读

## 🙌 一起学习

如果你也相信基础值得慢慢打磨，欢迎关注、阅读、提出 issue 或贡献实现。

这个仓库不追求一夜之间搭完所有东西，而是希望把深度学习中真正重要的部分，一步一步写清楚。希望它能陪你从 linear layer 出发，一路走到 LLM 和 Agent，也希望在这个过程中，我们都能对 AI 多一点真正的理解 🌟
