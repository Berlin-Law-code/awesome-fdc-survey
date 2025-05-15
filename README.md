# awesome-fdc-survey
Review of relevant papers on fault detection and correction
# Awesome Fault Detection and Correction [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> 精选故障检测与修复领域的重要论文、代码与资源，持续更新中  
> 欢迎贡献！请阅读 [CONTRIBUTING.md](CONTRIBUTING.md)
> 
---

<link rel="stylesheet" type="text/css" href="auto-number-title.css" />

## 📖 Content
- ##### [Introduction](#intro)
- ##### [Updates](#updates)
- ##### [Call for Contribution](#call)
- ##### [Method Introduction](#method)
- ##### [Datasets Introduction](#dataset)
- ##### [Benchmark Introduction](#benchmark)
- ##### [Acknowledgement](#acknowledgement)



## <a name="intro"></a>Introduction
This repo is a dataset and methods survey for Task-oriented Dialogue.

We investigated most existing dialogue datasets and summarized their basic information, such as brief, download link and size.

We also included leader boards of popular dataset to present research progress in the task oriented dialogue fields.

A Chinese intro & news for this project is available [here](https://mp.weixin.qq.com/s?__biz=MzIxMjAzNDY5Mg==&mid=2650793618&idx=1&sn=dc5e592c5d8b451531383350af76e254&chksm=8f477379b830fa6fb0b5909f6d6a3f85dae44e8a37aa0ab9763df354cabcc9224c211075f127&mpshare=1&scene=1&srcid=#rd)

#### Refer to this repo:
```
@misc{MAML_Pytorch,
  author = {Yutai Hou},
  title = {Task-Oriented Dialogue Research Progress Survey},
  year = {2018},
  publisher = {GitHub},
  journal = {GitHub repository},
  howpublished = {\url{https://github.com/AtmaHou/Task-Oriented-Dialogue-Research-Progress-Survey/}},
  commit = {master}
}
```

## <a name="updates"></a> Updates
This section records big updates to ease refer (See `./release_detail.md` or click links below):
- [Updates 2020.7.30](https://github.com/AtmaHou/Task-Oriented-Dialogue-Dataset-Survey/blob/master/release_detail.md#20200730): Add 3 new datasets, re-claim 6 abnormal NLU results, refine layout.


## <a name="call"></a> Call for Contribution
Contributions are welcomed, you are encouraged to:
- Directly pull request
- Send me new dataset info
- Send me new experiment results from published paper or public code implements.

## <a name="method"></a> Method Introduction
Dialogue state tacking task aims to predict or give representation of dialogue state,
which usually contains a goal constraint, a set of requested slots, and the user's dialogue act.

### [MultiWOZ 2.0](http://dialogue.mi.eng.cam.ac.uk/index.php/corpus/) - Dialogue State Tracking

Multi-Domain Wizard-of-Oz dataset (MultiWOZ), a fully-labeled collection of human-human written conversations spanning over multiple domains and topics. At a size of 10k dialogues, it is at least one order of magnitude larger than all previous annotated task-oriented corpora.

The new, corrected versions of the dataset are available at [MultiWOZ 2.1 (2019)](https://arxiv.org/abs/1907.01669), [MultiWOZ 2.2 (2020)](https://www.aclweb.org/anthology/2020.nlp4convai-1.13.pdf). 

> Notice: Models marked with * are open-vocabulary based models.`

| Model           | Key Content | Paper / Source | experiments | Remarks |
| ------------- | :-----:| :-----:| :-----:| :-----:|
| SOM-DST (BERT-large)* (Kim et al, 2020.09)  | None | None | [Efficient Dialogue State Tracking by Selectively Overwriting Memory](https://arxiv.org/pdf/1911.03906.pdf) | ICRA |


### RL Fine-tuning Correction
Clarification of dataset types:

The main results we list here are obtained from pure DSTC2 dataset (ASR n-best).

However, we don't list other kinds of DSTC2 data source results such as **DSTC2-text**
(It formulates the dialog state tracking as a machine reading problem
which read the dialog transcriptions multiple times and answer the questions
about each of the slot,
for more info please refer to [paper](https://aaai.org/ocs/index.php/WS/AAAIW18/paper/view/17447/15652))
and **DSTC-cleaned**
(It is used by the NBT paper and fixes ASR noise and typo during training and include ASR noise during testing,
The cleaned version is available at [here](https://github.com/Divye02/baby-jarvis/tree/master/data/dstc2)),

| Model           | Key Content | Paper / Source | experiments | Remarks |
| ------------- | :-----:| :-----:| :-----:| :-----:|
| SOM-DST (BERT-large)* (Kim et al, 2020.09)  | None | None | [Efficient Dialogue State Tracking by Selectively Overwriting Memory](https://arxiv.org/pdf/1911.03906.pdf) | ICRA |

## <a name="dataset"></a> Dataset Introduction
See the data details Here or in [Excel File](https://github.com/AtmaHou/Task-Oriented-Dialogue-Dataset-Survey/blob/master/Atma'sDatasetSurvey.xlsx?raw=true)

Following information is included for each dataset:
- Name
- Introduction
- Link (Download & Paper)
- Modalities
- Annotations
- Task Types
- Scale and Diversity
- Key Papers Using This Dataset

> Tips: The table below may not be displayed completely, **scroll right** to see more~

| Name                                        | Introduction                                                                                                                                                                                                                                                                                                                                                                                                                                                         | Links                                                                                                                                                                                 | Modalities | Annotations                                                                                                                                                               | Task Types | Scale & Diversity                                                                                                                                                                                                                          | Key Papers Using This Dataset                                                                                                                                                             |
| ------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Few-shot Slot Tagging Benchmark             | 1\. Dialogue slot tagging dataset for few-shot learning setting<br>2\. First few-shot sequence labeling benchmark (Meta-episode style data format)<br>3\. Also include 5  NER dataset for few-shot sequence labeling evaluation.                                                                                                                                                                                                                                     | Download:https://atmahou.github.io/attachments/ACL2020data.zip<br>Paper: https://arxiv.org/pdf/2006.05702.pdf                                                                         | S                 | 7 dialogue task:<br>Weather,play music, search, add to list, book, moive<br>5 NER task                                                                                    | Yes               | For each task, it contains 100 episodes.<br>Each episode contains a query set (20 samples) and a support set (1-shot & 5-shot)                                                                                                        | Slots                                                                                                                                                                             |

## <a name="benchmark"></a> Benchmark Introduction
See the data details Here or in [Excel File](https://github.com/AtmaHou/Task-Oriented-Dialogue-Dataset-Survey/blob/master/Atma'sDatasetSurvey.xlsx?raw=true)

Following information is included for each dataset:
- Name
- Introduction
- Link (Download & Paper)
- Modalities
- Evaluation Task Types
- Evaluation Protocol
- Scale and Diversity
- Baseline Results


> Tips: The table below may not be displayed completely, **scroll right** to see more~

| Name                                        | Introduction                                                                                                                                                                                                                                                                                                                                                                                                                                                         | Links                                                                                                                                                                                 | Modalities | Evaluation Task Types                                                                                                                                                               | Evaluation Protocol | Scale & Diversity                                                                                                                                                                                                                          | Baseline Results                                                                                                                                                             |
| ------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Few-shot Slot Tagging Benchmark             | 1\. Dialogue slot tagging dataset for few-shot learning setting<br>2\. First few-shot sequence labeling benchmark (Meta-episode style data format)<br>3\. Also include 5  NER dataset for few-shot sequence labeling evaluation.                                                                                                                                                                                                                                     | Download:https://atmahou.github.io/attachments/ACL2020data.zip<br>Paper: https://arxiv.org/pdf/2006.05702.pdf                                                                         | S                 | 7 dialogue task:<br>Weather,play music, search, add to list, book, moive<br>5 NER task                                                                                    | Yes               | For each task, it contains 100 episodes.<br>Each episode contains a query set (20 samples) and a support set (1-shot & 5-shot)                                                                                                        | Slots                                                                                                                                                                             |


## <a name="acknowledgment"></a>Acknowledgment

Thanks for supports from my adviser [Wanxiang Che](http://ir.hit.edu.cn/~car/english.htm).

Thanks for **public contributions** from:
[Shuai Lin](https://github.com/ha-lins),
[JiAnge](https://github.com/linjian93),
[Su Zhu](https://github.com/sz128),
[seeledu](https://github.com/seeledu),
[Tony Lin](https://github.com/tnlin),
[Jason Krone](https://github.com/jasonkrone),
[Libo Qin](https://github.com/yizhen20133868),
[HariiHe](https://github.com/HariiHe),
[Jelle Bosscher](https://github.com/jellebosscher),
.

