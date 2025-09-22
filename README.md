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

### System-Level Perspective
| Name | Failure Classification | Paper / Source |
| ------------- | :-----:| :-----:|
| SOM-DST (BERT-large)* (Kim et al, 2020.09) | None | [Efficient Dialogue State Tracking by Selectively Overwriting Memory](https://arxiv.org/pdf/1911.03906.pdf) |

### Root Causes Perspective
| Name | Failure Classification | Paper / Source |
| ------------- | :-----:| :-----:|
| SOM-DST (BERT-large)* (Kim et al, 2020.09) | None | [Efficient Dialogue State Tracking by Selectively Overwriting Memory](https://arxiv.org/pdf/1911.03906.pdf) |

### Behavioral Manifestation Perspective
| Name | Failure Classification | Paper / Source |
| ------------- | :-----:| :-----:|
| SOM-DST (BERT-large)* (Kim et al, 2020.09) | None | [Efficient Dialogue State Tracking by Selectively Overwriting Memory](https://arxiv.org/pdf/1911.03906.pdf) |

### Human-Robot Interaction Perspective
| Name | Failure Classification | Paper / Source |
| ------------- | :-----:| :-----:|
| SOM-DST (BERT-large)* (Kim et al, 2020.09) | None | [Efficient Dialogue State Tracking by Selectively Overwriting Memory](https://arxiv.org/pdf/1911.03906.pdf) |


## <a name="method"></a> Methods Introduction
We categorize existing failure detection and correction methods into two core paradigms: Human-in-the-Loop (HITL) and Model-in-theLoop (MITL). 

### Human in the Loop
HITL mechanisms enhance system adaptability in complex tasks through supervision and interaction, effectively compensating for the shortcomings of autonomous models in common-sense reasoning and unconventional decision-making. Humans can provide intuitive feedback through multimodal interaction methods such as language, gestures, physiological signals, and interactive user interfaces, thereby accelerating the system’s ability to identify and respond to emergent failures.

> Notice: None

| Name | Detection | Correction | Tools | Paper / Source |
| ------------- | :-----:| :-----:| :-----:| :-----:|
| SOM-DST (BERT-large)* (Kim et al, 2020.09)  | None | None | [Efficient Dialogue State Tracking by Selectively Overwriting Memory](https://arxiv.org/pdf/1911.03906.pdf) | ICRA |

### Model in the Loop
MITL mechanism deeply integrates world models, multimodal perception, and adaptive algorithms, enabling the system to autonomously form a closed feedback loop of perception, planning, execution and verification. By continuously monitoring task states, predicting potential risks, and dynamically adjusting strategies, the MITL mechanism aims to significantly reduce reliance on external intervention, thereby enhancing autonomy and efficiency. 

> Notice: None.`

| Name | Detection | Correction | Principle | Paper / Source |
| ------------- | :-----:| :-----:| :-----:| :-----:|
| SOM-DST (BERT-large)* (Kim et al, 2020.09)  | [x] | [√] | None | [Efficient Dialogue State Tracking by Selectively Overwriting Memory](https://arxiv.org/pdf/1911.03906.pdf) | ICRA |

### RL Fine-tuning Correction
Researchers are shifting their focus toward reinforcement fine-tuning for VLA architectures to autonomously learn and optimize through trial-and-error and reward mechanisms, thereby spontaneously developing advanced reasoning abilities such as CoT, selfverification, and failure correction, and even exhibiting emergent capabilities to achieve autonomous policy optimization, significantly enhancing their robustness and adaptability. 

Clarification of dataset types:

| Name | VLM/VLA | Strategy | Paper / Source |
| ------------- | :-----:| :-----:| :-----:|
| GRAPE (Kim et al, 2020.09)  | OpenVLA | TPO | [Efficient Dialogue State Tracking by Selectively Overwriting Memory](https://arxiv.org/pdf/1911.03906.pdf) |

## <a name="dataset"></a> Datasets and Benchmarks
Constructing failure datasets and benchmarks for robotic manipulation tasks constitutes a critical prerequisite for enabling effective failure detection and correction. The following section provides a systematic overview of the datasets and benchmarking frameworks in this domain.

### Datasets Introduction

Following information is included for each dataset:
- Name
- Task Types
- Scale and Diversity
- Link (Paper / Source)

> Tips: The table below may not be displayed completely, **scroll right** to see more~

| Name | Task Types | Scale and Diversity | Paper / Source |
| ------------- | :-----:| :-----:| :-----:|
| FAC | None | None | None |

### Benchmarks Introduction

Following information is included for each dataset:
- Name
- Evaluation Task Types
- Scale and Diversity
- Link (Paper / Source)

> Tips: The table below may not be displayed completely, **scroll right** to see more~

| Name | Evaluation Task Types | Scale and Diversity | Paper / Source |
| ------------- | :-----:| :-----:| :-----:|
| Few-shot Slot Tagging Benchmark | None | None | None |


## <a name="acknowledgment"></a>Acknowledgment

Thanks for supports from my adviser [Wanxiang Che](http://ir.hit.edu.cn/~car/english.htm).

Thanks for **public contributions** from:
[Shuai Lin](https://github.com/ha-lins)
.

