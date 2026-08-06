# Micrograd 课程笔记

[Andrej Karpathy - Neural Networks: Zero to Hero 系列 · 第 1 课](https://www.youtube.com/watch?v=VMj-3S1tku0)

> 用约 150 行代码实现一个极简的自动求导引擎（Autograd Engine），
> 在此基础上训练一个二元分类的 MLP（多层感知机）。

## 课程内容

1. **Value 类** — 构建表达式图，每个节点保存值 + 梯度
2. **反向传播** — 链式法则，`backward()` 递归求梯度
3. **MLP 实现** — Neuron → Layer → MLP
4. **训练** — 用随机梯度下降（SGD）做二元分类
5. **可视化** — 用 graphviz 画出计算图

## 官方参考

- 官方仓库：https://github.com/karpathy/micrograd
- 讲义：`lecture1-3.pdf`（微积分/反向传播基础）
- **`reference/`** — 官方完整代码（已拉取本地作为对照）：
  - `micrograd/engine.py` — 官方 Value 类实现（94 行）
  - `micrograd/nn.py` — Neuron / Layer / MLP
  - `demo.ipynb` — 训练演示（notebook）
  - `trace_graph.ipynb` — graphviz 计算图可视化
  - `test/test_engine.py` — 官方测试

## 本目录文件

| 文件 | 说明 |
|------|------|
| `reference/` | 官方源码（对照参考，勿修改） |
| `engine.py` | 我自己的实现（Value 类，自动求导引擎） |
| `nn.py` | Neuron / Layer / MLP |
| `train.py` | 训练一个二元分类器 |
| `notes.md` | 学习笔记 |

## 运行环境

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install graphviz
python train.py
```
