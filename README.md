# modular
This is a repo to use modular paradigm (sparse) LLM



## Module

LoRA have been proved its effectiveness in parameter-efficient finetuning. However, LoRA can not explicitly disambiguate the task-relvant information within the learned low-rank subspace.  FVAE-LoRA propose a FVAE LoRA to factorize the latent space into the $z_1$ and $z_2$ and then use $z_1$ to control the task-relvant information and $z_2$ to control residual information.
| **Paper Title** | **Year** | **Conference/Journal** | **Code** |
| --------------- | :----: | :----: | :----: |
| [Latent Space Factorization in LoRA](https://arxiv.org/pdf/2510.19640#page=1.01) | 2025 | NeurIPS | [code](no run)|
| [DoRA: Weight-Decomposed Low-Rank Adaptation](https://openreview.net/pdf?id=3d5CIRG1n2) | 2024 | ICML | [code](no run)|

## Model Merging

Model merging has emerged as a powerful technique that aims to integrate the weights of multiple task-specific models into a single multi-task model without extra training, offering benefits such as reduced storage and serving cost. However, the merging approach always introduce interference between the models, which is not desirable. To reduce the interference of model merging, there are a rich body of work have been proposed to guide the merging process. Some research work have explored model merging without additional data for retraining or test-time computation. Wudi merging have demonstrated that the task vector of the linear layer consititute an approximate linear subspace for its corresponding input and then proce a wudi-merging ((Whoever started the interference shoUld enD It)), a simple yet effective approach that can eliminate interference without addition dataset. Knots (knowledge orientation through SVD), builds upon SVD to transform the task-updates of different LoRA adapters into a shared space, where merging methods can be applied. Close-form merging study the model merging methods based on Regmerge for federated continual learning.  Merge to learn study three paradigm: contuning finetuning, retraining and parallel-then-merge. They demonstrate that parallel-then-merge is a more effficient way to add the new knowledge.  

| **Paper Title** | **Year** | **Conference/Journal** | **Code** |
| --------------- | :----: | :----: | :----: |
| [Whoever Started the Interference Should End It: Guiding Data-Free Model Merging via Task Vectors](https://arxiv.org/pdf/2503.08099#page=17.22) | 2025 | ICML | [code](https://github.com/nathanielyvo/WUDI-Merging)|
| [Multi-Task Model Merging via Adaptive Weight Disentanglement](https://arxiv.org/pdf/2411.18729) | 2025 | Arxiv | [code](no run)|
| [Model Unmerging: Making Your Models Unmergeable for Secure Model Sharing](https://arxiv.org/abs/2509.01548) | 2025 | NeurIPS | [code](no run)|
| [Twin-Merging: Dynamic Integration of Modular Expertise in Model Merging](https://arxiv.org/pdf/2406.15479) | 2024 | NeurIPS | [code](no run)|
| [OptMerge: UNIFYING MULTIMODAL LLM CAPABILI-TIES AND MODALITIES VIA MODEL MERGING](https://openreview.net/pdf?id=Me0n0iESJY) | 2025 | Arxiv | [code](no run)|
| [WHAT MATTERS FOR MODEL MERGING AT SCALE?](https://openreview.net/forum?id=9sbetmvNpW) | 2024 | TMLR | [code](no run)|
| [CLOSED-FORM MERGING OF PARAMETER-EFFICIENTMODULES FOR FEDERATED CONTINUAL LEARNIN](https://arxiv.org/pdf/2410.17961) | 2025 | ICLR | [code](no run)|
| [Merge to Learn: Efficiently Adding Skills to Language Models
with Model Merging](https://arxiv.org/pdf/2410.12937) | 2024 | arxiv | [code](no run)|

### survey

| **Paper Title** | **Year** | **Conference/Journal** | **Code** |
| --------------- | :----: | :----: | :----: |
| [A Survey on Model MoErging: Recycling and Routing Among Specialized Experts for Collaborative Learning](https://arxiv.org/pdf/2408.07057) | 2024 | TMLR | |


### sparse merging
| **Paper Title** | **Year** | **Conference/Journal** | **Code** |
| --------------- | :----: | :----: | :----: |
| [LoRS: Efficient Low-Rank Adaptation for Sparse Large Language Model](https://arxiv.org/pdf/2501.085821) | 2025 | Arxiv | [code](no run)|
| [Exploring Sparse Adapters for Scalable Merging of Parameter Efficient Experts](https://arxiv.org/pdf/2507.07140) | 2025 | COLM | [code](no run)|

## Mixture of Experts

### Mixture of LoRA adapters. 

Fundational model needs to integrate multiple capabilities to handle complex downstream tasks. One simple method is to conduct contuning training on the downstream tasks. However, retraining on multi-domain corpus is expensive, particularly when the specialized models are available. 

To reduce the computational cost and memory resource reqiured by the full-finetuing, parameter efficient finetuning (PEFT) has emerged. Among these approaches, LoRA adapters have been proved comparable to full-fintuning while demanding less compuatation. Despite these improvement, LoRA-based methods face challenges in multi-task scenarios due to the limited training parameters and the catastrophic forgetting problems, which degrade the performance in the cross-task generalization. For instance, adapterfusion and LoRAhub introduce task-specifc LoRA modules or experts, combining knowledge into domain experts through additional attention fusion and element-wise composition. However, these additional components often add complexity to the training process, limitig their applicability compared to the simpler PEFT methods. 

A promising solution is to design an architecture that combine LoRA's resource-saving features with the versatility of MoE models. 

| **Paper Title** | **Year** | **Conference/Journal** | **Code** |
| --------------- | :----: | :----: | :----: |
| [FlyLoRA: Boosting Task Decoupling and Parameter Efficiency via Implicit Rank-Wise Mixture-of-Experts](https://arxiv.org/pdf/2510.08396#page=3.03) | 2025 | NeurIPS | [code](https://github.com/gfyddha/FlyLoRA)|
| [ThanoRA: Task Heterogeneity-Aware Multi-Task Low-Rank Adaptation](https://arxiv.org/abs/2505.18640) | 2025 | Arxiv | [code](https://github.com/LiangJian24/ThanoRA)|
| [LoRA-Mixer: Coordinate Modular LoRA Experts Through Serial Attention Routing](https://arxiv.org/abs/2507.00029) | 2025 | Arxiv | [code](no run)|
| [MIXLORA: Enhancing Large Language Models Fine-Tuning with LoRA-based Mixture of Experts](https://arxiv.org/pdf/2404.15159) | 2024 | Arxiv | [code](no run)|


## LLM Selection. 

| **Paper Title** | **Year** | **Conference/Journal** | **Code** |
| --------------- | :----: | :----: | :----: |
| [RouteLLM: Learning to Route LLMs with Preference Data](https://arxiv.org/abs/2406.18665) | 2025 | ICML | [code](https://github.com/lm-sys/RouteLLM)|
| [RouterBench: A Benchmark for Multi-LLM Routing System](https://openreview.net/forum?id=IVXmV8Uxwh) | 2024 |  | |
| [Hybrid LLM: Cost-Efficient and Quality-Aware Query Routing](https://arxiv.org/abs/2404.14618) | 2024 | ICLR | | 
| [BEST-Route: Adaptive LLM Routing with Test-Time Optimal Compute](https://arxiv.org/abs/2506.22716) | 2025 | ICML | |

