# awesome-fdc-survey
Review of relevant papers on fault detection and correction
# Awesome Fault Detection and Correction [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated collection of seminal papers, codebases, and resources in the field of failure detection and correction, continuously updated.  
> Contributions are welcome—please refer to [CONTRIBUTING.md](CONTRIBUTING.md)
> 
---

<link rel="stylesheet" type="text/css" href="auto-number-title.css" />

## 📖 Content
- ##### [Introduction](#intro)
- ##### [Updates](#updates)
- ##### [Call for Contribution](#call)
- ##### [Failure Classification](#classification)
- ##### [Methods Introduction](#method)
- ##### [Datasets and Benchmarks](#dataset)
- ##### [Acknowledgement](#acknowledgement)



## <a name="intro"></a>Introduction
This repo is a dataset and methods survey for Task-oriented Dialogue.

We investigated most existing dialogue datasets and summarized their basic information, such as brief, download link and size.

We also included leader boards of popular dataset to present research progress in the task oriented dialogue fields.
#### Refer to this repo:
```
@misc{FDC_Survey,
  author = {Yuanbin Liu},
  title = {A_Survey_on_Failure_Detection_and_Correction_for_Robotic_Manipulation_in_the_Era_of_Foundation_Models},
  year = {2025},
  publisher = {GitHub},
  journal = {GitHub repository},
  howpublished = {\url{https://https://github.com/Berlin-Law-code/awesome-fdc-survey/}},
  commit = {master}
}
```

## <a name="updates"></a> Updates
This section records big updates to ease refer (See `./release_detail.md` or click links below):
- [Updates 2025.10.1](https://github.com/Berlin-Law-code/awesome-fdc-survey/blob/main/release_detail.md.md#20251001): Release in public.


## <a name="call"></a> Call for Contribution
Contributions are welcomed, you are encouraged to:
- Directly pull request
- Send me new method and dataset info
- Send me new experiment results from published paper or public code implements.

## <a name="classification"></a>  Failure Classification
Through a comprehensive review of the literature on failure classification, we distill four principal paradigms for categorizing robotic failures, derived from multiple analytical perspectives.

| Paper | Published in | Code/Project |
| ------------- | :-----:| :-----:|
| [Efficient Dialogue State Tracking by Selectively Overwriting Memory](https://arxiv.org/pdf/1911.03906.pdf) | CVPR2025 | [Code](https://github.com/clovaai/som-dst) |
| [Reflect: Summarizing Robot Experiences for Failure Explanation and Correction](https://proceedings.mlr.press/v205/liu23d.html) | CoRL 2023 |  |
| [Condition Monitoring and Fault Diagnosis of Industrial Robots: A Review](https://link.springer.com/article/10.1007/s11431-024-2647-6) | Science China Technological Sciences 2025 |  |
| [Dadu-E: Rethinking the Role of Large Language Model in Robotic Computing Pipeline](https://arxiv.org/pdf/2412.01663.pdf) | arXiv 2024 |  |
| [Can’t Touch This: Real-Time, Safe Motion Planning and Control for Manipulators Under Uncertainty](https://ieeexplore.ieee.org/document/10457953) | IEEE T-RO 2025 |  |
| [ReMac: Self-Reflective and Self-Evolving Multi-Agent Collaboration for Long-Horizon Robot Manipulation](https://arxiv.org/pdf/2503.22122.pdf) | arXiv 2025 |  |
| [Robot Error Awareness Through Human Reactions: Implementation, Evaluation, and Recommendations](https://arxiv.org/pdf/2501.05723.pdf) | arXiv 2025 |  |
| [Distilling and Retrieving Generalizable Knowledge for Robot Manipulation via Language Corrections](https://ieeexplore.ieee.org/document/10500606) | ICRA 2024 |  |
| [Robotic Manipulation via Imitation Learning: Taxonomy, Evolution, Benchmark, and Challenges](https://arxiv.org/pdf/2508.17449.pdf) | arXiv 2025 |  |
| [Reinforcement Learning in Robotics: A Survey](https://journals.sagepub.com/doi/pdf/10.1177/0278364913495721) | IJRR 2013 |  |
| [Reflexion: Language Agents with Verbal Reinforcement Learning](https://arxiv.org/pdf/2303.11366.pdf) | NeurIPS 2023 | https://github.com/noahshinn024/reflexion |
| [TidyBot: Personalized Robot Assistance with Large Language Models](https://arxiv.org/pdf/2305.05658.pdf) | Autonomous Robots 2023 | https://github.com/google-research/tidybot |
| [Talk-to-Resolve: Combining Scene Understanding and Spatial Dialogue to Resolve Granular Task Ambiguity for a Collocated Robot](https://www.sciencedirect.com/science/article/pii/S0921889022001077) | RAS 2022 |  |
| [Raider: Tool-Equipped Large Language Model Agent for Robotic Action Issue Detection, Explanation and Recovery](https://arxiv.org/pdf/2503.17703.pdf) | arXiv 2025 |  |
| [RACER: Rich Language-Guided Failure Recovery Policies for Imitation Learning](https://arxiv.org/pdf/2409.14674.pdf) | arXiv 2024 |  |
| [Rethinking the Bias of Foundation Model Under Long-Tailed Distribution](https://arxiv.org/pdf/2502.02077.pdf) | ICML 2025 |  |
| [I-FailSense: Towards General Robotic Failure Detection with Vision-Language Models](https://arxiv.org/pdf/2509.16072.pdf) | arXiv 2025 |  |
| [A Survey of Robotic Language Grounding: Tradeoffs Between Symbols and Embeddings](https://arxiv.org/pdf/2403.09857.pdf) | IJCAI 2024 |  |
| [RePlan: Robotic Replanning with Perception and Language Models](https://arxiv.org/pdf/2401.04157.pdf) | arXiv 2024 | https://github.com/aspuru-guzik-group/replan |
| [Do As I Can, Not As I Say: Grounding Language in Robotic Affordances](https://arxiv.org/pdf/2204.01691.pdf) | arXiv 2022 | https://github.com/google-research/robotics_transformer |
| [Recover: A Neuro-Symbolic Framework for Failure Detection and Recovery](https://arxiv.org/pdf/2407.02883.pdf) | IROS 2024 |  |
| [Code-as-Monitor: Constraint-Aware Visual Programming for Reactive and Proactive Robotic Failure Detection](https://openaccess.thecvf.com/content/CVPR2025/papers/Zhou_Code-as-Monitor_Constraint-Aware_Visual_Programming_for_Reactive_and_Proactive_Robotic_Failure_Detection_CVPR_2025_paper.pdf) | CVPR 2025 |  |





## <a name="method"></a> Methods Introduction
We categorize existing failure detection and correction methods into two core paradigms: Human-in-the-Loop (HITL) and Model-in-theLoop (MITL). 

### Human in the Loop
HITL mechanisms enhance system adaptability in complex tasks through supervision and interaction, effectively compensating for the shortcomings of autonomous models in common-sense reasoning and unconventional decision-making. Humans can provide intuitive feedback through multimodal interaction methods such as language, gestures, physiological signals, and interactive user interfaces, thereby accelerating the system’s ability to identify and respond to emergent failures.

> Notice: None

| Paper | Published in | Code/Project |
| ------------- | :-----:| :-----:|
| [Efficient Dialogue State Tracking by Selectively Overwriting Memory](https://arxiv.org/pdf/1911.03906.pdf) | CVPR2025 | [Code](https://github.com/clovaai/som-dst) |

### Model in the Loop
MITL mechanism deeply integrates world models, multimodal perception, and adaptive algorithms, enabling the system to autonomously form a closed feedback loop of perception, planning, execution and verification. By continuously monitoring task states, predicting potential risks, and dynamically adjusting strategies, the MITL mechanism aims to significantly reduce reliance on external intervention, thereby enhancing autonomy and efficiency. 

> Notice: None.`

| Paper | Published in | Code/Project |
| ------------- | :-----:| :-----:|
| [Efficient Dialogue State Tracking by Selectively Overwriting Memory](https://arxiv.org/pdf/1911.03906.pdf) | CVPR2025 | [Code](https://github.com/clovaai/som-dst) |


### RL Fine-tuning Correction
Researchers are shifting their focus toward reinforcement fine-tuning for VLA architectures to autonomously learn and optimize through trial-and-error and reward mechanisms, thereby spontaneously developing advanced reasoning abilities such as CoT, selfverification, and failure correction, and even exhibiting emergent capabilities to achieve autonomous policy optimization, significantly enhancing their robustness and adaptability. 

Clarification of dataset types:

| Paper | Published in | Code/Project |
| ------------- | :-----:| :-----:|
| [Efficient Dialogue State Tracking by Selectively Overwriting Memory](https://arxiv.org/pdf/1911.03906.pdf) | CVPR2025 | [Code](https://github.com/clovaai/som-dst) |



## <a name="dataset"></a> Datasets and Benchmarks
Constructing failure datasets and benchmarks for robotic manipulation tasks constitutes a critical prerequisite for enabling effective failure detection and correction. The following section provides a systematic overview of the datasets and benchmarking frameworks in this domain.

### Datasets Introduction

Following information is included for each dataset:
- Name
- Task Types
- Scale and Diversity
- Link (Paper / Source)

> Tips: The table below may not be displayed completely, **scroll right** to see more~

| Paper | Published in | Code/Project |
| ------------- | :-----:| :-----:|
| [Efficient Dialogue State Tracking by Selectively Overwriting Memory](https://arxiv.org/pdf/1911.03906.pdf) | CVPR2025 | [Code](https://github.com/clovaai/som-dst) |


### Benchmarks Introduction

Following information is included for each dataset:
- Name
- Evaluation Task Types
- Scale and Diversity
- Link (Paper / Source)

> Tips: The table below may not be displayed completely, **scroll right** to see more~

| Paper | Published in | Code/Project |
| ------------- | :-----:| :-----:|
| [Efficient Dialogue State Tracking by Selectively Overwriting Memory](https://arxiv.org/pdf/1911.03906.pdf) | CVPR2025 | [Code](https://github.com/clovaai/som-dst) |



## <a name="acknowledgment"></a>Acknowledgment

Thanks for supports from my adviser [Wanxiang Che](http://ir.hit.edu.cn/~car/english.htm).

Thanks for **public contributions** from:
[Shuai Lin](https://github.com/ha-lins)
.

