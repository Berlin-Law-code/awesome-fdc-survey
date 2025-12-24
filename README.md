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
| Condition monitoring and fault diagnosis of industrial robots: A review | Sci China Tech Sci 2025 | - |
| Can’t touch this: Real-time, safe motion planning and control for manipulators under uncertainty | IEEE T-RO 2025 | - |
| Object misdetection, pose estimation and failure propagation in robotic manipulation | IEEE T-RO | - |
| Reflect: Summarizing robot experiences for failure explanation and correction | CoRL 2023 | https://github.com/real-stanford/reflect |
| Robot error awareness through human reactions | arXiv 2025 | - |
| Distilling and retrieving generalizable knowledge for robot manipulation via language corrections | ICRA 2024 | - |
| Robotic manipulation via imitation learning: Taxonomy, evolution, benchmark, and challenges | arXiv 2025 | - |
| Reinforcement learning in robotics: A survey | IJRR 2013 | - |
| Reflexion: Language agents with verbal reinforcement learning | NeurIPS 2023 | https://github.com/noahshinn/reflexion |
| Vision-language-action models in robotic manipulation: A systematic review | arXiv 2025 | - |
| Do As I Can, Not As I Say: Grounding Language in Robotic Affordances | arXiv 2022 | https://github.com/google-research/google-research/tree/master/saycan |
| Talk-to-Resolve: Combining scene understanding and spatial dialogue to resolve granular task ambiguity | RAS 2022 | - |
| RAIDER: Tool-equipped LLM agent for robotic action issue detection, explanation and recovery | arXiv 2025 | - |
| RACER: Rich language-guided failure recovery policies for imitation learning | arXiv 2024 | https://github.com/UT-Austin-RPL/RACER |
| Recover: A neuro-symbolic framework for failure detection and recovery | IROS 2024 | - |



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

