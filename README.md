<h1 align="center"><strong>Towards Robust Robotic Manipulation: A Survey on Failure Detection and Recovery in the Era of Foundation Model</strong></h1>
A curated collection of seminal papers, codebases, datasets and benchmarks in the field of failure detection and recovery, continuously updated.

## 📖 Content

1. [Introduction](#intro)
2. [Failure Classification](#classification)
3. [Methods](#method)
4. [Datasets and Benchmarks](#dataset)
5. [Updates](#updates)
6. [Call for Contribution](#call)
7. [Citation](#refer)
8. [Acknowledgement](#acknowledgement)

## 🏠 <a name="intro"></a> Introduction
![Image Alt Text](figures/1_1.png)
Recent advancements in foundation models have significantly enhanced the capabilities of robots in reasoning, decision-making, and task execution, enabling them to handle complex, unstructured tasks. However, these models also introduce new failure modes, particularly in robotic manipulation. As robots shift from deterministic systems to those driven by foundation models, issues like hallucinations, lack of physical commonsense, and semantic misinterpretations can lead to failures in perception, grounding, planning, and execution. These cognitive-level failures increase uncertainty in task outcomes, highlighting the need for better failure detection and recovery mechanisms.

Foundation models are key in detecting and correcting failures in robotic systems. They enhance robots' understanding and reasoning, helping identify discrepancies between expected and actual outcomes. LLMs and MLLMs enable semantic verification and task re-planning, while Vision-Language-Action Models (VLAs) can correct movements in real-time. World models can proactively prevent failures by simulating and evaluating recovery strategies.


## 📄 <a name="classification"></a>  Failure Classification
![Image Alt Text](figures/3_1.png)

As foundation models are increasingly integrated into robotic manipulation, failures are no longer limited to execution errors but also encompass cognitive and semantic failures arising from stages such as perception, grounding, planning, and reasoning. To address these challenges, this paper introduces a hierarchical failure classification framework that aligns with the perception-grounding-planning-execution pipeline.
> Tips: The table below may not be displayed completely, **scroll right** to see more~

| Paper | Published in | Code/Project |
| ------------- | :-----:| :-----:|
| [Reflect: Summarizing Robot Experiences for Failure Explanation and Correction](https://arxiv.org/pdf/2306.15724) | CoRL 2023 | https://robot-reflect.github.io/ |
| [Condition Monitoring and Fault Diagnosis of Industrial Robots: A Review](https://link.springer.com/article/10.1007/s11431-024-2810-2) | Science China Technological Sciences 2025 |  |
| [Dadu-E: Rethinking the Role of Large Language Model in Robotic Computing Pipeline](https://arxiv.org/pdf/2412.01663.pdf) | arXiv 2024 | https://rlc-lab.github.io/dadu-e/ |
| [Can’t Touch This: Real-Time, Safe Motion Planning and Control for Manipulators Under Uncertainty](https://ieeexplore.ieee.org/abstract/document/11059838/) | IEEE T-RO 2025 |  https://roahmlab.github.io/armour/|
| [ReMac: Self-Reflective and Self-Evolving Multi-Agent Collaboration for Long-Horizon Robot Manipulation](https://arxiv.org/pdf/2503.22122.pdf) | arXiv 2025 |  |
| [Robot Error Awareness Through Human Reactions: Implementation, Evaluation, and Recommendations](https://arxiv.org/pdf/2501.05723.pdf) | arXiv 2025 |  |
| [Distilling and Retrieving Generalizable Knowledge for Robot Manipulation via Language Corrections](https://ieeexplore.ieee.org/abstract/document/10610455) | ICRA 2024 | https://sites.google.com/stanford.edu/droc |
| [Robotic Manipulation via Imitation Learning: Taxonomy, Evolution, Benchmark, and Challenges](https://arxiv.org/pdf/2508.17449.pdf) | arXiv 2025 |  |
| [Reinforcement Learning in Robotics: A Survey](https://journals.sagepub.com/doi/pdf/10.1177/0278364913495721) | IJRR 2013 |  |
| [Reflexion: Language Agents with Verbal Reinforcement Learning](https://arxiv.org/pdf/2303.11366.pdf) | NeurIPS 2023 | https://github.com/noahshinn024/reflexion |
| [TidyBot: Personalized Robot Assistance with Large Language Models](https://arxiv.org/pdf/2305.05658.pdf) | Autonomous Robots 2023 | https://github.com/google-research/tidybot |
| [Talk-to-Resolve: Combining Scene Understanding and Spatial Dialogue to Resolve Granular Task Ambiguity for a Collocated Robot](https://www.sciencedirect.com/science/article/pii/S0921889022001077) | RAS 2022 |  |
| [Raider: Tool-Equipped Large Language Model Agent for Robotic Action Issue Detection, Explanation and Recovery](https://arxiv.org/pdf/2503.17703.pdf) | arXiv 2025 | https://eurecat.github.io/raider-llmagent/ |
| [RACER: Rich Language-Guided Failure Recovery Policies for Imitation Learning](https://arxiv.org/pdf/2409.14674.pdf) | arXiv 2024 | https://rich-language-failure-recovery.github.io/ |
| [Rethinking the Bias of Foundation Model Under Long-Tailed Distribution](https://arxiv.org/pdf/2501.15955) | ICML 2025 |  |
| [I-FailSense: Towards General Robotic Failure Detection with Vision-Language Models](https://arxiv.org/pdf/2509.16072.pdf) | arXiv 2025 | https://clemgris.github.io/I-FailSense/ |
| [A Survey of Robotic Language Grounding: Tradeoffs Between Symbols and Embeddings](https://arxiv.org/pdf/2405.13245) | IJCAI 2024 |  |
| [RePlan: Robotic Replanning with Perception and Language Models](https://arxiv.org/pdf/2401.04157.pdf) | arXiv 2024 | https://github.com/aspuru-guzik-group/replan |
| [Do As I Can, Not As I Say: Grounding Language in Robotic Affordances](https://arxiv.org/pdf/2204.01691.pdf) | arXiv 2022 | https://github.com/google-research/robotics_transformer |
| [Recover: A Neuro-Symbolic Framework for Failure Detection and Recovery](https://ieeexplore.ieee.org/abstract/document/10801853) | IROS 2024 | https://recover-ontothor.github.io |
| [Code-as-Monitor: Constraint-Aware Visual Programming for Reactive and Proactive Robotic Failure Detection](https://openaccess.thecvf.com/content/CVPR2025/papers/Zhou_Code-as-Monitor_Constraint-Aware_Visual_Programming_for_Reactive_and_Proactive_Robotic_Failure_Detection_CVPR_2025_paper.pdf) | CVPR 2025 | https://zhoues.github.io/Code-as-Monitor |


## 🤖 <a name="method"></a> Methods
We categorize existing failure detection and recovery methods into three core paradigms: Human-in-the-Loop (HITL), Model-in-theLoop (MITL), and Reinforcement Fine-Tuning (RFT). 

### Human in the Loop

![Image Alt Text](figures/4_1.png)
HITL mechanism involves human operators providing judgment and corrective actions during failure detection and recovery in autonomous systems. These methods are especially useful in dynamic, unstructured environments where the systems may lack adequate reasoning or commonsense knowledge.
> Tips: The table below may not be displayed completely, **scroll right** to see more~

| Paper | Published in | Code/Project |
| ------------- | :-----:| :-----:|
| [RACER: Rich Language-Guided Failure Recovery Policies for Imitation Learning](https://arxiv.org/pdf/2409.14674.pdf) | arXiv 2024 | https://rich-language-failure-recovery.github.io/ |
| [Rethinking the Bias of Foundation Model Under Long-Tailed Distribution](https://arxiv.org/pdf/2501.15955) | ICML 2025 |  |
| [I-FailSense: Towards General Robotic Failure Detection with Vision-Language Models](https://arxiv.org/pdf/2509.16072.pdf) | arXiv 2025 | https://clemgris.github.io/I-FailSense/ |
| [A Survey of Robotic Language Grounding: Tradeoffs Between Symbols and Embeddings](https://arxiv.org/pdf/2405.13245) | IJCAI 2024 |  |
| [A Review of Robot Learning for Manipulation: Challenges, Representations, and Algorithms](https://www.jmlr.org/papers/v22/19-804.html) | JMLR 2021 |  |
| [Real-Time Detection of Robot Failures Using Gaze Dynamics in Collaborative Tasks](https://ieeexplore.ieee.org/abstract/document/10973922) | HRI 2025 |  |
| [Human-in-the-loop Robot Learning for Smart Manufacturing: A Human-Centric Perspective](https://ieeexplore.ieee.org/abstract/document/10836893) | IEEE Trans. on Automation Science and Engineering 2025 |  |
| [Real-Time Out-of-Distribution Failure Prevention via Multi-Modal Reasoning](https://arxiv.org/pdf/2505.10547) | RSS Workshop 2025 | https://milanganai.github.io/fortress |
| [GRAPE: Generalizing Robot Policy Via Preference Alignment](https://arxiv.org/pdf/2411.19309) | ICRA 2025 Workshop |  |
| [Interactive Imitation Learning in Robotics: A Survey](https://www.nowpublishers.com/article/Details/ROB-072) | Foundations and Trends® in Robotics 2022 |  |
| [Don’t Yell at Your Robot: Physical Correction as the Collaborative Interface for Language Model Powered Robots](https://arxiv.org/pdf/2412.12602.pdf) | arXiv 2024 |  |
| [RoboCopilot: Human-in-the-loop Interactive Imitation Learning for Robot Manipulation](https://arxiv.org/pdf/2503.07771.pdf) | arXiv 2025 |  |
| [Yell at Your Robot: Improving On-the-Fly from Language Corrections](https://arxiv.org/pdf/2403.12910.pdf) | arXiv 2024 | https://yay-robot.github.io/ |
| [Interactive Robot Learning from Verbal Correction](https://arxiv.org/pdf/2310.17555) | LA@R Workshop 2023 | https://ut-austin-rpl.github.io/olaf/ |
| [Learning to Learn Faster from Human Feedback with Language Model Predictive Control](https://arxiv.org/pdf/2402.11450) | ICRA Workshop 2024 | https://robot-teaching.github.io/ |
| [Perception Alignment for Human-Robot Collaboration (SynergAI)](https://ieeexplore.ieee.org/document/10478765) | ICRA 2025 |  |
| [Online Imitation Learning for Manipulation via Decaying Relative Correction](https://arxiv.org/pdf/2503.15368.pdf) | arXiv 2025 |  |
| [Head and Shoulders: Automatic Error Detection in Human-Robot Interaction](https://dl.acm.org/doi/abs/10.1145/3136755.3136805) | ACM ICMI 2017 |  |
| [Correcting Robot Mistakes in Real Time Using EEG Signals](https://ieeexplore.ieee.org/document/7989407) | ICRA 2017 |  |
| [Learning to Share Autonomy Across Repeated Interaction](https://arxiv.org/pdf/2108.00123.pdf) | IROS 2021 |  |
| [Human-in-the-loop Task and Motion Planning for Imitation Learning](https://proceedings.mlr.press/v206/mandlekar23a.html) | CoRL 2023 |  |
| [Robots That Ask for Help: Uncertainty Alignment for LLM Planners](https://proceedings.mlr.press/v206/ren23a.html) | CoRL 2023 |  |
| [RT-H: Action Hierarchies Using Language](https://www.roboticsconference.org/rss2024/papers/??) | RSS 2024 |  |
| [Enhancement of Long Horizon Task Planning via Active and Passive Modification in Large Language Models](https://www.nature.com/articles/s41598-025-07113-z) | Scientific Reports 2025 |  |
| [Correcting Robot Plans with Natural Language Feedback](https://arxiv.org/pdf/2204.05186.pdf) | arXiv 2022 |  |
| [Robot Learning on the Job: Human-in-the-loop Autonomy and Learning During Deployment](https://www.roboticsconference.org/rss2023/papers/???.pdf) | RSS 2023 |  |
| [Learning from Interventions: Human-Robot Interaction as Feedback](https://arxiv.org/pdf/2003.12909.pdf) | RSS 2020 |  |
| [Human-in-the-loop Imitation Learning Using Remote Teleoperation](https://arxiv.org/pdf/2012.06733.pdf) | arXiv 2020 |  |
| [ThriftyDAGGER: Budget-Aware Novelty and Risk Gating for Interactive Imitation Learning](https://proceedings.mlr.press/v164/belkhale22a.html) | CoRL 2022 |  |
| [Learning Preferences for Manipulation Tasks from Online Coactive Feedback](https://journals.sagepub.com/doi/pdf/10.1177/0278364915589289) | IJRR 2015 |  |
| [Bridging the Human to Robot Dexterity Gap Through Object-Oriented Rewards](https://openaccess.thecvf.com/content/CoRL2024/papers/Guzey_Bridging_the_Human_to_Robot_Dexterity_Gap_Through_Object-Oriented_Rewards_CoRL_2024_paper.pdf) | CoRL Workshop 2024 |  |
| [Human-in-the-loop Error Detection in Object Organization Task with a Social Robot](https://www.frontiersin.org/articles/10.3389/frobt.2024.1356827/full) | Frontiers in Robotics and AI 2024 |  |
| [Asking Follow-Up Clarifications to Resolve Ambiguities in Human-Robot Conversation](https://ieeexplore.ieee.org/document/9759016) | HRI 2022 |  |
| [ConRFT: Reinforced Fine-Tuning Method for VL Models via Consistency Policy](https://arxiv.org/pdf/2502.05450.pdf) | arXiv 2025 |  |

### Model in the Loop
![Image Alt Text](figures/4_2.png)
MITL mechanism embeds failure detection and recovery capabilities directly within the robotic system, relying on internal models to monitor and respond to failures autonomously. This paradigm offers greater scalability and adaptability, as it reduces the need for constant human involvement. 
> Tips: The table below may not be displayed completely, **scroll right** to see more~

| Paper | Published in | Code/Project |
| ------------- | :-----:| :-----:|
| [Inner Monologue: Embodied Reasoning Through Planning with Language Models](https://proceedings.mlr.press/v205/huang23b/huang23b.pdf) | CoRL 2023 |  |
| [Embodied-Reasoner: Synergizing Visual Search, Reasoning, and Action for Embodied Interactive Tasks](https://arxiv.org/pdf/2503.21696.pdf) | arXiv 2025 |  |
| Overcoming Reward Model Noise in Instruction-Guided Reinforcement Learning | arXiv 2024 |  |
| [Safe: Multitask Failure Detection for Vision-Language-Action Models](https://arxiv.org/pdf/2506.09937.pdf) | arXiv 2025 |  |
| [A Self-Correcting Vision-Language-Action Model for Fast and Slow System Manipulation](https://arxiv.org/pdf/2405.17418.pdf) | arXiv 2024 |  |
| [Roboreflect: Robotic Reflective Reasoning for Grasping Ambiguous Condition Objects](https://arxiv.org/pdf/2501.09307.pdf) | arXiv 2025 |  |
| [Robofac: A Comprehensive Framework for Robotic Failure Analysis and Correction](https://arxiv.org/pdf/2505.12224.pdf) | arXiv 2025 |  |
| [DoReMi: Grounding Language Model by Detecting and Recovering from Plan-Execution Misalignment](https://ieeexplore.ieee.org/document/10465874) | IROS 2024 |  |
| [Errors are Useful Prompts: Instruction Guided Task Programming with Verifier-Assisted Iterative Prompting](https://arxiv.org/pdf/2303.14100.pdf) | arXiv 2023 |  |
| [RePlan: Robotic Replanning with Perception and Language Models](https://arxiv.org/pdf/2401.04157.pdf) | arXiv 2024 | https://github.com/aspuru-guzik-group/replan |
| [Self-Correcting Quadratic Programming-Based Robot Control](https://ieeexplore.ieee.org/document/10298130) | IEEE T-SMC: Systems 2023 |  |
| [Failure Identification and Recovery Framework for a Planar Reconfigurable Cable Driven Parallel Robot](https://www.sciencedirect.com/science/article/pii/S1474667022033252) | IFAC PapersOnLine 2022 |  |
| [Failure Handling of Robotic Pick and Place Tasks with Multimodal Cues under Partial Object Occlusion](https://www.frontiersin.org/articles/10.3389/fnbot.2021.570507/full) | Frontiers in Neurorobotics 2021 |  |
| [A Unified Framework for Real-Time Failure Handling in Robotics Using Vision-Language Models, Reactive Planner and Behavior Trees](https://arxiv.org/pdf/2503.15202.pdf) | arXiv 2025 |  |
| [Model-Based Runtime Monitoring with Interactive Imitation Learning](https://ieeexplore.ieee.org/document/10465009) | ICRA 2024 |  |
| [Asking for Help: Failure Prediction in Behavioral Cloning through Value Approximation](https://ieeexplore.ieee.org/document/10080003) | ICRA 2023 |  |
| [Steering Your Generalists: Improving Robotic Foundation Models via Value Guidance](https://proceedings.coralvox.org/v270/nakamoto25a/nakamoto25a.pdf) | CoRL 2025 |  |
| [Feature Expansive Reward Learning: Rethinking Human Input](https://dl.acm.org/doi/10.1145/3434075.3444535) | HRI 2021 |  |
| [CoPaL: Corrective Planning of Robot Actions with Large Language Models](https://ieeexplore.ieee.org/document/10390884) | ICRA 2024 |  |
| [GraspCorrect: Robotic Grasp Correction via Vision-Language Model-Guided Feedback](https://arxiv.org/pdf/2503.15035.pdf) | arXiv 2025 |  |
| [GeomaniP: Geometric Constraints as General Interfaces for Robot Manipulation](https://arxiv.org/pdf/2501.09783.pdf) | arXiv 2025 |  |
| [ReplanVLM: Replanning Robotic Tasks with Visual Language Models](https://ieeexplore.ieee.org/document/10446452) | IEEE RA-L 2024 |  |
| [Can We Detect Failures Without Failure Data? Uncertainty-Aware Runtime Failure Detection for Imitation Learning Policies](https://arxiv.org/pdf/2503.08558.pdf) | arXiv 2025 |  |
| [CAPE: Corrective Actions from Precondition Errors Using Large Language Models](https://ieeexplore.ieee.org/document/10465046) | ICRA 2024 |  |
| [ConditionNet: Learning Preconditions and Effects for Execution Monitoring](https://ieeexplore.ieee.org/document/10499348) | IEEE RA-L 2024 |  |
| [Learning Symbolic Failure Detection for Grasping and Mobile Manipulation Tasks](https://ieeexplore.ieee.org/document/9811972) | IROS 2022 |  |
| [Multimodal Execution Monitoring for Anomaly Detection During Robot Manipulation](https://ieeexplore.ieee.org/document/7487419) | ICRA 2016 |  |
| [VLM-in-the-Loop Policy Steering via Latent Alignment](https://openreview.net/forum?id=WG9B0hY7hCb) | ICLR 2025 Workshop |  |
| [Chat with the Environment: Interactive Multimodal Perception Using Large Language Models](https://ieeexplore.ieee.org/document/10180592) | IROS 2023 |  |
| [From Mystery to Mastery: Failure Diagnosis for Improving Manipulation Policies](https://arxiv.org/pdf/2503.03768.pdf) | RSS 2025 Workshop |  |
| [Adaptable Recovery Behaviors in Robotics…BTMG for Failure Management](https://ieeexplore.ieee.org/document/10355723) | IEEE CASE 2024 |  |
| [Expel: LLM Agents are Experiential Learners](https://ojs.aaaai.org/index.php/AAAI/article/view/26602) | AAAI 2024 |  |
| [AIC MLLM: Autonomous Interactive Correction MLLM for Robust Robotic Manipulation](https://arxiv.org/pdf/2406.11548.pdf) | arXiv 2024 |  |
| [Risk-Guided Diffusion: Toward Deploying Robot Foundation Models in Space](https://proceedings.rss.org/v2025/abstracts/abstract2075.html) | RSS 2025 Workshop |  |
| [HiCRISP: An LLM-based Hierarchical Closed-Loop Robotic Intelligent Self-Correction Planner](https://ieeexplore.ieee.org/document/10385672) | CAC 2024 |  |
| Pre-Emptive Action Revision by Environmental Feedback for Embodied Instruction Following Agents | CoRL 2024 |  |
| [Multimodal Detection and Classification of Robot Manipulation Failures](https://ieeexplore.ieee.org/document/10084679) | IEEE RA-L 2023 |  |
| [FinoNet: A Deep Multimodal Sensor Fusion Framework for Manipulation Failure Detection](https://ieeexplore.ieee.org/document/9635264) | IROS 2021 |  |
| [Multi-Task Interactive Robot Fleet Learning with Visual World Models](https://proceedings.coralvox.org/v270/liu25a/liu25a.pdf) | CoRL 2025 |  |
| [Voyager: An Open-Ended Embodied Agent with Large Language Models](https://openaccess.thecvf.com/content/CVPR2024/papers/Wang_Voyager_An_Open-Ended_Embodied_Agent_With_Large_Language_Models_CVPR_2024_paper.pdf) | TMLR 2024 |  |
| [Uniform Learning from Demonstrations, Corrections, and Preferences](https://arxiv.org/pdf/2207.03395.pdf) | arXiv 2024 |  |
| [Learning Human Objectives from Sequences of Physical Corrections](https://ieeexplore.ieee.org/document/9382428) | ICRA 2021 |  |
| [Toward Grounded Commonsense Reasoning](https://ieeexplore.ieee.org/document/10465082) | ICRA 2024 |  |
| [Bebop: Combining Reactive Planning and Bayesian Optimization for Robotic Manipulation](https://ieeexplore.ieee.org/document/10446462) | ICRA 2024 |  |
| [Unpacking Failure Modes of Generative Policies: Runtime Monitoring of Consistency & Progress](https://proceedings.coralvox.org/v270/agia25a/agia25a.pdf) | CoRL 2025 |  |



### Reinforcement Learning Fine-Tuning
![Image Alt Text](figures/4_3.png)
RFT enhances robotic manipulation by using feedback from the environment and past failures to continuously refine action policies, improving task performance and failure recovery over time.
> Tips: The table below may not be displayed completely, **scroll right** to see more~

| Paper | Published in | Code/Project |
| ------------- | :-----:| :-----:|
| Paper | Published in | Code/Project |
| ------------- | :-----:| :-----:|
| [RFTF: Reinforcement Fine-Tuning for Embodied Agents with Temporal Feedback](https://arxiv.org/pdf/2505.19767.pdf) | arXiv 2025 |  |
| [ReinboT: Amplifying Robot Visual-Language Manipulation with Reinforcement Learning](https://arxiv.org/pdf/2505.07395.pdf) | ICML 2025 |  |
| [GR-RL: Going Dexterous and Precise for Long-Horizon Robotic Manipulation](https://arxiv.org/pdf/2512.01801.pdf) | arXiv 2025 |  |
| [CO-RFT: Efficient Fine-Tuning of Vision-Language-Action Models through Chunked Offline Reinforcement Learning](https://arxiv.org/pdf/2508.02219.pdf) | arXiv 2025 |  |
| [Improving Vision-Language-Action Model with Online Reinforcement Learning](https://arxiv.org/pdf/2501.16664.pdf) | arXiv 2025 |  |
| [RLDG: Robotic Generalist Policy Distillation via Reinforcement Learning](https://arxiv.org/pdf/2412.09858.pdf) | arXiv 2024 |  |
| [Efficient Online Reinforcement Learning with Offline Data](https://arxiv.org/pdf/2302.02948.pdf) | ICML 2023 | [Code](https://github.com/ikostrikov/rlpd) |
| [DeepSeekMath: Pushing the Limits of Mathematical Reasoning in Open Language Models](https://arxiv.org/pdf/2402.03300.pdf) | arXiv 2024 | [Code](https://github.com/deepseek-ai/DeepSeek-Math) |
| [Visual-RFT: Visual Reinforcement Fine Tuning](https://arxiv.org/pdf/2503.01785.pdf) | arXiv 2025 |  |
| [Perception-R1: Pioneering Perception Policy with Reinforcement Learning](https://arxiv.org/pdf/2504.07954.pdf) | arXiv 2025 |  |
| [R1-VL: Learning to Reason with Multimodal Large Language Models via Step-wise Group Relative Policy Optimization](https://arxiv.org/pdf/2503.12937.pdf) | arXiv 2025 |  |
| [Multi-SpatialMLLM: Multi-frame Spatial Understanding with Multi-modal Large Language Models](https://arxiv.org/pdf/2505.17015.pdf) | arXiv 2025 |  |
| [Embodied-R: Collaborative Framework for Activating Embodied Spatial Reasoning in Foundation Models via Reinforcement Learning](https://arxiv.org/pdf/2504.12680.pdf) | ACM MM 2025 | [Code](https://github.com/EmbodiedCity/Embodied-R.code) |
| [ManipLVM-R1: Reinforcement Learning for Reasoning in Embodied Manipulation with Large Vision-Language Models](https://arxiv.org/pdf/2505.16517.pdf) | arXiv 2025 |  |
| [Residual Reinforcement Learning for Robot Control](https://arxiv.org/pdf/1812.03201.pdf) | ICRA 2019 | [Project](https://residualrl.github.io/) |
| [Track2Act: Predicting Point Tracks from Internet Videos enables Generalizable Robot Manipulation](https://arxiv.org/pdf/2405.01527.pdf) | ECCV 2024 |  |
| [Teach a Robot to FISH: Versatile Imitation from One Minute of Demonstrations](https://arxiv.org/pdf/2303.01497.pdf) | RSS 2023 | [Project](https://fast-imitation.github.io/) |
| [See to Touch: Learning Tactile Dexterity through Visual Incentives](https://arxiv.org/pdf/2309.12300.pdf) | ICRA 2024 | [Code](https://github.com/irmakguzey/see-to-touch) |
| [Self-improving Vision-Language-Action Models with Data Generation via Residual RL](https://arxiv.org/pdf/2511.00091.pdf) | arXiv 2025 |  |
| TransIC: Sim-to-real Policy Transfer by Learning from Online Correction | CoRL 2025 |  |
| [Compliant Residual DAgger: Improving Real-World Contact-Rich Manipulation with Human Corrections](https://arxiv.org/pdf/2506.16685.pdf) | arXiv 2025 | [Code](https://github.com/yifan-hou/cr-dagger) |

### Matching Failures to Recovery Strategies
![Image Alt Text](figures/4_4.png)

## 📦 <a name="dataset"></a> Datasets and Benchmarks
Effective failure detection and recovery strategies for robotic manipulation require high-quality datasets and standardized benchmarks. These resources help train models, evaluate failure handling approaches, and compare system robustness in various failure scenarios.

### Datasets
> Tips: The table below may not be displayed completely, **scroll right** to see more~

| Paper | Published in | Code/Project |
| ------------- | :-----:| :-----:|
| [A Multimodal Handover Failure Detection Dataset and Baselines](https://arxiv.org/pdf/2402.18319) | ICRA 2024 | [Code]( https://sthoduka.github.io/handover_failure_detection) |
| [Data-Agnostic Robotic Long-Horizon Manipulation with Vision-Language-Guided Closed-Loop Feedback](https://ghiara.github.io/DAHLIA/static/DAHLIA-v2.pdf) | arXiv 2025 | [Code](https://github.com/Ghiara/DAHLIA) |
| [Open X-Embodiment: Robotic Learning Datasets and RT-X Models](https://arxiv.org/pdf/2310.08864) | ICRA 2024 | [Project](https://github.com/google-deepmind/open_x_embodiment) |
| [All Robots in One: A New Standard and Unified Dataset for Versatile, General-Purpose Embodied Agents](https://arxiv.org/pdf/2408.10899) | arXiv 2024 | [Project](https://imaei.github.io/project_pages/ario/) |
| [A System-Level View on Out-of-Distribution Data in Robotics](https://arxiv.org/pdf/2212.14020.pdf) | arXiv 2022 |  |
| [RoboMIND: Benchmark on Multi-embodiment Intelligence Normative Data for Robot Manipulation](https://arxiv.org/pdf/2412.13877.pdf) | arXiv 2024 | [Project](https://x-humanoid-robomind.github.io/) |
| [REFLEX Dataset: A Multimodal Dataset of Human Reactions to Robot Failures and Explanations](https://arxiv.org/pdf/2502.14185.pdf) | HRI 2025 | [Project](https://github.com/andreasnaoum/reflex-viz) |
| [Scaling Up and Distilling Down: Language-Guided Robot Skill Acquisition](https://proceedings.mlr.press/v229/ha23a/ha23a.pdf) | CoRL 2023 | [Project](https://www.cs.columbia.edu/~huy/scalingup/) |
| [IntervenGen: Interventional Data Generation for Robust and Data-Efficient Robot Imitation Learning](https://arxiv.org/pdf/2405.01472.pdf) | IROS 2024 | [Project](https://sites.google.com/view/intervengen2024) |




### Benchmarks
> Tips: The table below may not be displayed completely, **scroll right** to see more~

| Paper | Published in | Code/Project |
| ------------- | :-----:| :-----:|
| [Embodied Question Answering](https://openaccess.thecvf.com/content_cvpr_2018/html/Das_Embodied_Question_Answering_CVPR_2018_paper.html) | CVPR 2018 | https://embodiedqa.org/ |
| [IQA: Visual Question Answering in Interactive Environments](https://openaccess.thecvf.com/content_cvpr_2018/html/Gordon_IQA_Visual_Question_CVPR_2018_paper.html) | CVPR 2018 | https://youtu.be/pXd3C-1jr98 |
| [Multi-Target Embodied Question Answering](https://openaccess.thecvf.com/content_CVPR_2019/html/Yu_Multi-Target_Embodied_Question_Answering_CVPR_2019_paper.html) | CVPR 2019 | https://embodiedqa.org/ |
| [Embodied Question Answering in Photorealistic Environments with Point Cloud Perception](https://openaccess.thecvf.com/content_CVPR_2019/papers/Wijmans_Embodied_Question_Answering_in_Photorealistic_Environments_With_Point_Cloud_Perception_CVPR_2019_paper.pdf) | CVPR 2019 |  |
| [EgoTaskQA: Understanding Human Tasks in Egocentric Videos](https://arxiv.org/pdf/2210.03929) | NeurIPS 2022 | https://sites.google.com/view/egotaskqa |
| [EQA MX: Embodied Question Answering using Multimodal Expression](https://openreview.net/pdf?id=7gUrYE50Rb) | ICLR 2024 | [Dataset](https://bit.ly/eqa-mx-dataset), [Code](https://bit.ly/eqa-repo) |
| [OpenEQA: Embodied Question Answering in the Era of Foundation Models](https://openaccess.thecvf.com/content/CVPR2024/html/Majumdar_OpenEQA_Embodied_Question_Answering_in_the_Era_of_Foundation_Models_CVPR_2024_paper.html) | CVPR 2024 | https://open-eqa.github.io/ |
| [Muble: Mujoco and Blender Simulation Environment and Benchmark for Task Planning in Robot Manipulation](https://arxiv.org/pdf/2503.02834.pdf) | arXiv 2025 | https://github.com/michaal94/MuBlE |
| [Beyond the Destination: A Novel Benchmark for Exploration-Aware Embodied Question Answering](https://arxiv.org/pdf/2503.11117) | arXiv 2025 | https://github.com/HCPLab-SYSU/EXPRESS-Bench |
| [IndustryEQA: Pushing the Frontiers of Embodied Question Answering in Industrial Scenarios](https://arxiv.org/pdf/2505.20640.pdf) | arXiv 2025 | [Dataset](https://huggingface.co/datasets/IndustryEQA/IndustryEQA),  [Code](https://github.com/JackYFL/IndustryEQA)|
| [Grounded, or a Good Guesser?: A Per-Question Balanced Dataset to Separate Blind from Grounded Models for Embodied QA](https://aclanthology.org/2025.acl-short.11.pdf) | ACL 2025 | https://milesshelton.github.io/pqb_eqa/ |
| [RoboCerebra: A Large-Scale Benchmark for Long Horizon Robotic Manipulation Evaluation](https://arxiv.org/pdf/2506.06677.pdf) | arXiv 2025 | https://robocerebra.github.io/ |
| [Explore Until Confident: Efficient Exploration for Embodied Question Answering](https://arxiv.org/pdf/2403.15941) | ICRA 2024 Workshop | https://explore-eqa.github.io/ |
| [Robo2VLM: Visual Question Answering from Large-Scale In-the-Wild Robot Manipulation Datasets](https://arxiv.org/pdf/2505.15517.pdf) | arXiv 2025 | https://berkeleyautomation.github.io/robo2vlm/ |
| [VLatest: Testing and Evaluating Vision-Language-Action Models for Robotic Manipulation](https://arxiv.org/pdf/2409.12894) | ACM SE 2025 | https://github.com/ma-labo/VLATest |
| [What Matters in Learning from Offline Human Demonstrations for Robot Manipulation](https://proceedings.mlr.press/v164/mandlekar22a/mandlekar22a.pdf) | CoRL 2022 | https://arise-initiative.github.io/robomimic-web/ |
| [The COLOSSEUM: A Benchmark for Evaluating Generalization for Robotic Manipulation](https://arxiv.org/pdf/2402.08191) | RSS 2024 Workshop | https://robot-colosseum.github.io/ |
| [RLBench: The Robot Learning Benchmark & Learning Environment](https://ieeexplore.ieee.org/document/9153261) | IEEE RA-L 2020 | https://sites.google.com/view/rlbench |
| [Sapien: A Simulated Part-Based Interactive Environment](https://arxiv.org/pdf/2003.08515) | CVPR 2020 | https://sapien.ucsd.edu/ |
| [AI2-THOR: An Interactive 3D Environment for Visual AI](https://arxiv.org/pdf/1712.05474.pdf) | arXiv 2017 | http://ai2thor.allenai.org/ |
| [AutoEval: Autonomous Evaluation of Generalist Robot Manipulation Policies in the Real World](https://arxiv.org/pdf/2503.24278) | 7th Robot Learning Workshop 2025 | https://auto-eval.github.io/ |


## 🔥 <a name="updates"></a> Updates
This section records big updates to ease refer (See `./release_detail.md` or click links below):
- [Updates 2025.10.1](https://github.com/Berlin-Law-code/awesome-fdc-survey/blob/main/release_detail.md.md#20251001): Release in public.

## 📚 <a name="call"></a> Call for Contribution
If you would like to contribute to this project, please refer to our [contribution guide](Contribution.md). Contributions are always welcome, and we encourage you to:
- Directly pull request;
- Send me new method and dataset info;
- Send me new experiment results from published paper or public code implements.

## 🔗 <a name="refer"></a> Citation
If you find our work helpful, please cite:

```bibtex
@inproceedings{FDC_Survey,
    title = {A_Survey_on_Failure_Detection_and_Correction_for_Robotic_Manipulation_in_the_Era_of_Foundation_Models},
    author={Wang, Tai and Mao, Xiaohan and Zhu, Chenming and Xu, Runsen and Lyu, Ruiyuan and Li, Peisen and Chen, Xiao and Zhang, Wenwei and Chen, Kai and Xue, Tianfan and Liu, Xihui and Lu, Cewu and Lin, Dahua and Pang, Jiangmiao},
    year={2025},
    publisher = {GitHub}
    journal = {GitHub repository},
    howpublished = {\url{https://https://github.com/Berlin-Law-code/awesome-fdc-survey/}},
    commit = {master}
}
```
## 👏 <a name="acknowledgment"></a>Acknowledgment

Thanks for supports from my adviser [Wanxiang Che](http://ir.hit.edu.cn/~car/english.htm).

Thanks for **public contributions** from:
[Shuai Lin](https://github.com/ha-lins).

