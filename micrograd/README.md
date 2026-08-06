# Micrograd Course Notes

[Andrej Karpathy - Neural Networks: Zero to Hero Series · Lecture 1](https://www.youtube.com/watch?v=VMj-3S1tku0)

> Build a tiny autograd engine (~150 lines) from scratch, then train a binary
> classification MLP on top of it.

## Course Topics

1. **Value class** — build an expression graph; each node holds value + gradient
2. **Backpropagation** — chain rule, recursive `backward()` to compute gradients
3. **MLP implementation** — Neuron → Layer → MLP
4. **Training** — binary classification with stochastic gradient descent (SGD)
5. **Visualization** — draw the computation graph with graphviz

## Official Reference

- Official repo: https://github.com/karpathy/micrograd
- Lecture notes: `lecture1-3.pdf` (calculus / backprop fundamentals)
- **`reference/`** — full official source (pulled locally for comparison):
  - `micrograd/engine.py` — official Value class implementation (94 lines)
  - `micrograd/nn.py` — Neuron / Layer / MLP
  - `demo.ipynb` — training demo (notebook)
  - `trace_graph.ipynb` — graphviz computation graph visualization
  - `test/test_engine.py` — official tests

## Files in This Directory

| File | Description |
|------|-------------|
| `reference/` | Official source (for comparison — do not modify) |
| `engine.py` | My own implementation (Value class, autograd engine) |
| `nn.py` | Neuron / Layer / MLP |
| `train.py` | Train a binary classifier |
| `notes.md` | Study notes |

## Environment

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install graphviz
python train.py
```
