# modular
This is a repo to use modular paradigm (sparse) LLM



## Module

LoRA have been proved its effectiveness in parameter-efficient finetuning. However, LoRA can not explicitly disambiguate the task-relvant information within the learned low-rank subspace.  FVAE-LoRA propose a FVAE LoRA to factorize the latent space into the $z_1$ and $z_2$ and then use $z_1$ to control the task-relvant information and $z_2$ to control residual information.
| **Paper Title** | **Year** | **Conference/Journal** | **Code** |
| --------------- | :----: | :----: | :----: |
| [Latent Space Factorization in LoRA](https://arxiv.org/pdf/2510.19640#page=1.01) | 2025 | NeurIPS | [code](no run)|
| [DoRA: Weight-Decomposed Low-Rank Adaptation](https://openreview.net/pdf?id=3d5CIRG1n2) | 2024 | ICML | [code](no run)|

## Model Merging

Model merging have proved to be a powerful way to combine multiple models into a single model, offering benefits such as reduced storage and serving cost. However, the merging approach always introduce interference between the models, which is not desirable. To reduce the interference of model merging, there are a rich body of work have been proposed to guide the merging process. Some research work have explored model merging without additional data for retraining or test-time computation. Wudi merging have demonstrated that the task vector of the linear layer consititute an approximate linear subspace for its corresponding input and then proce a wudi-mergin ((Whoever started the interference shoUld enD It)), a simple yet effective approach that can eliminate interference without addition dataset. AWD merging

| **Paper Title** | **Year** | **Conference/Journal** | **Code** |
| --------------- | :----: | :----: | :----: |
| [Whoever Started the Interference Should End It: Guiding Data-Free Model Merging via Task Vectors](https://arxiv.org/pdf/2503.08099#page=17.22) | 2025 | ICML | [code](https://github.com/nathanielyvo/WUDI-Merging)|
| [Multi-Task Model Merging via Adaptive Weight Disentanglement](https://arxiv.org/pdf/2411.18729) | 2025 | Arxiv | [code](no run)|

## Mixture of Experts

### Mixture of LoRA adapters. 

Fundational model needs to integrate multiple capabilities to handle complex downstream tasks. One simple methods  is to conduct contuning training on the downstream tasks. However, retraining on multi-domain corpus is expensive, particularly when the specialized models are available. Model merging is can be a more efficient way to Combine LoRA adapters on different domains. But Model merging will introduce the task interference. 

| **Paper Title** | **Year** | **Conference/Journal** | **Code** |
| --------------- | :----: | :----: | :----: |
| [FlyLoRA: Boosting Task Decoupling and Parameter Efficiency via Implicit Rank-Wise Mixture-of-Experts](https://arxiv.org/pdf/2510.08396#page=3.03) | 2025 | NeurIPS | [code](https://github.com/gfyddha/FlyLoRA)|
| [ThanoRA: Task Heterogeneity-Aware Multi-Task Low-Rank Adaptation](https://arxiv.org/abs/2505.18640) | 2025 | Arxiv | [code](https://github.com/LiangJian24/ThanoRA)|
| [LoRA-Mixer: Coordinate Modular LoRA Experts Through Serial Attention Routing](https://arxiv.org/abs/2507.00029) | 2025 | Arxiv | [code](no run)|


## LLM Selection. 

| **Paper Title** | **Year** | **Conference/Journal** | **Code** |
| --------------- | :----: | :----: | :----: |
| [RouteLLM: Learning to Route LLMs with Preference Data](https://arxiv.org/abs/2406.18665) | 2025 | ICML | [code](https://github.com/lm-sys/RouteLLM)|
| [RouterBench: A Benchmark for Multi-LLM Routing System](https://openreview.net/forum?id=IVXmV8Uxwh) | 2024 |  | |
| [Hybrid LLM: Cost-Efficient and Quality-Aware Query Routing](https://arxiv.org/abs/2404.14618) | 2024 | ICLR | | 
| [BEST-Route: Adaptive LLM Routing with Test-Time Optimal Compute](https://arxiv.org/abs/2506.22716) | 2025 | ICML | |