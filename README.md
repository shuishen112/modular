# modular
This is a repo to use modular paradigm (sparse) LLM



## Module



## Model Merging

Model merging have proved to be a powerful way to combine multiple models into a single model, offering benefits such as reduced storage and serving cost. However, the merging approach always introduce interference between the models, which is not desirable. To reduce the interference of model merging, there are a rich body of work have been proposed to guide the merging process. Some research work have explored model merging without additional data for retraining or test-time computation. Wudi merging have demonstrated that the task vector of the linear layer consititute an approximate linear subspace for its corresponding input and then proce a wudi-mergin ((Whoever started the interference shoUld enD It)), a simple yet effective approach that can eliminate interference without addition dataset. AWD merging

| **Paper Title** | **Year** | **Conference/Journal** | **Code** |
| --------------- | :----: | :----: | :----: |
| [Whoever Started the Interference Should End It: Guiding Data-Free Model Merging via Task Vectors](https://arxiv.org/pdf/2503.08099#page=17.22) | 2025 | ICML | [code](https://github.com/nathanielyvo/WUDI-Merging)|
| [Multi-Task Model Merging via Adaptive Weight Disentanglement](https://arxiv.org/pdf/2411.18729) | 2025 | Arxiv | [code](no run)|

## Mixture of Experts

### Mixture of LoRA adapters. 
| **Paper Title** | **Year** | **Conference/Journal** | **Code** |
| --------------- | :----: | :----: | :----: |
| [FlyLoRA: Boosting Task Decoupling and Parameter Efficiency via Implicit Rank-Wise Mixture-of-Experts](https://arxiv.org/pdf/2510.08396#page=3.03) | 2025 | NeurIPS | [code](https://github.com/gfyddha/FlyLoRA)|


## LLM Selection. 

| **Paper Title** | **Year** | **Conference/Journal** | **Code** |
| --------------- | :----: | :----: | :----: |
| [RouteLLM: Learning to Route LLMs with Preference Data](https://arxiv.org/abs/2406.18665) | 2025 | ICML | [code](https://github.com/lm-sys/RouteLLM)|
| [RouterBench: A Benchmark for Multi-LLM Routing System](https://openreview.net/forum?id=IVXmV8Uxwh) | 2024 |  | |
| [Hybrid LLM: Cost-Efficient and Quality-Aware Query Routing](https://arxiv.org/abs/2404.14618) | 2024 | ICLR | | 
| [BEST-Route: Adaptive LLM Routing with Test-Time Optimal Compute](https://arxiv.org/abs/2506.22716) | 2025 | ICML | |