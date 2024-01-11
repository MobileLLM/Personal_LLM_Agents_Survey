# Personal LLM Agents - Survey

This repo maintains a curated list of papers related to Personal LLM Agents. For more details, please refer to our paper or join our discussion group:

> [Personal LLM Agents: Insights and Survey about the Capability, Efficiency and Security](https://github.com/MobileLLM/Personal_LLM_Agents_Survey/)
>
> Yuanchun Li, Hao Wen, Weijun Wang, Xiangyu Li, Yizhen Yuan, Guohong Liu, Jiacheng Liu, Wenxing Xu, Xiang Wang, Yi Sun, Rui Kong, Yile Wang, Hanfei Geng, Jian Luan, Xuefeng Jin, Zilong Ye, Guanjing Xiong, Fan Zhang, Xiang Li, Mengwei Xu, Zhijun Li, Peng Li, Yang Liu, Ya-Qin Zhang, Yunxin Liu
>
> [[arxiv]](https://arxiv.org/)  [[pdf]](https://yuanchun-li.github.io/static/files/personal_llm_agents.pdf)  [[cite]](#citation)  [[discuss (zulip)]](https://mobilellm.zulipchat.com/join/md3qfwhmvko4yt4fu3cendve/)

**Personal LLM Agents** are defined as a special type of LLM-based agents that are deeply integrated with personal data, personal devices, and personal services.
They are perferably deployed to resource-constrained mobile/edge devices and/or powered by lightweight AI models.
The main purpose of personal LLM agents is to assist end-users and augment their abilities, helping them to focus more and do better on interesting and important affairs.

This paper list covers several main aspects of Personal LLM Agents, including the capabilities, efficiency and security. 
Table of content:

- [Personal LLM Agents - Survey](#personal-llm-agents---survey)
  - [Key Capabilities of Personal LLM Agents](#key-capabilities-of-personal-llm-agents)
    - [Task Automation](#task-automation)
      - [UI-grounded Agents for Task Automation](#ui-grounded-agents-for-task-automation)
      - [Benchmarks of UI Automation](#benchmarks-of-ui-automation)
    - [Sensing](#sensing)
      - [LLM-based Approaches](#llm-based-approaches)
      - [Traditional Approaches](#traditional-approaches)
    - [Memorization](#memorization)
      - [Memory Obtaining](#memory-obtaining)
      - [Memory Management](#memory-management)
      - [Agent Self-evolution](#agent-self-evolution)
  - [Efficiency of LLM Agents](#efficiency-of-llm-agents)
    - [Efficient LLM Inference \& Training](#efficient-llm-inference--training)
    - [Efficient Memory Retrieval \& Management](#efficient-memory-retrieval--management)
      - [Organizing the Memory](#organizing-the-memory)
      - [Optimizing the Efficiency of Memory](#optimizing-the-efficiency-of-memory)
  - [Security \& Privacy of Personal LLM Agents](#security--privacy-of-personal-llm-agents)
    - [Confidentiality (of User Data)](#confidentiality-of-user-data)
    - [Integrity (of Agent Behavior)](#integrity-of-agent-behavior)
    - [Reliability (of Agent Decisions)](#reliability-of-agent-decisions)

## Key Capabilities of Personal LLM Agents

### Task Automation

Task automation is a core capability of personal LLM agents, which determines how well the agent can respond to user commands and/or automatically execute tasks for the user.

We focus on UI-based task automation agents in this list due to their popularity and close relevance to personal devices.

#### UI-grounded Agents for Task Automation 

LLM-based Approaches

- WebGPT: Browser-assisted question-answering with human feedback. [[paper](https://arxiv.org/abs/2112.09332)]
- Enabling Conversational Interaction with Mobile UI Using Large Language Models. [CHI 2023] [[paper](https://doi.org/10.1145/3544548.3580895)]
- Language Models can Solve Computer Tasks. [NeurIPS 2023] [[paper](https://openreview.net/forum?id=M6OmjAZ4CX)]
- DroidBot-GPT: GPT-powered UI Automation for Android. [[arxiv](https://arxiv.org/abs/2304.07061)] [[code](https://github.com/MobileLLM/DroidBot-GPT)]
- Responsible Task Automation: Empowering Large Language Models as Responsible Task Automators.[[paper](https://arxiv.org/abs/2306.01242)]
- Mind2Web: Towards a Generalist Agent for the Web. arxiv 2023 [[paper](https://arxiv.org/abs/2306.06070)][[code](https://github.com/OSU-NLP-Group/Mind2Web)][[code](https://github.com/google-research-datasets/uibert)]
- (AutoDroid) Empowering LLM to use Smartphone for Intelligent Task Automation. [[paper](https://arxiv.org/abs/2308.15272)] [[code](https://github.com/MobileLLM/AutoDroid)]
- You Only Look at Screens: Multimodal Chain-of-Action Agents. ArXiv Preprint [[paper](https://arxiv.org/abs/2309.11436)] [[code](https://github.com/TouristShaun/Auto-UI/tree/main)]
- AXNav: Replaying Accessibility Tests from Natural Language. [[paper](https://arxiv.org/abs/2310.02424)]
- Automatic Macro Mining from Interaction Traces at Scale. [[paper](https://arxiv.org/abs/2310.07023)]
- A Zero-Shot Language Agent for Computer Control with Structured Reflection. [[paper](https://arxiv.org/abs/2310.08740)]
- Reinforced UI Instruction Grounding: Towards a Generic UI Task Automation API. [[paper](https://arxiv.org/abs/2310.04716)]
- GPT-4V in Wonderland: Large Multimodal Models for Zero-Shot Smartphone GUI Navigation. [[paper](https://arxiv.org/abs/2311.07562)][[code](https://github.com/zzxslp/MM-Navigator)]
- UGIF: UI Grounded Instruction Following. [[paper](https://arxiv.org/abs/2211.07615)]
- Explore, Select, Derive, and Recall: Augmenting LLM with Human-like Memory for Mobile Task Automation. [[paper](https://arxiv.org/abs/2312.03003)][[code]()]
- CogAgent: A Visual Language Model for GUI Agents. [[paper](https://arxiv.org/abs/2312.08914)][[code](https://github.com/THUDM/CogAgent/tree/main)]
- AppAgent: Multimodal Agents as Smartphone Users. [[paper](https://arxiv.org/abs/2312.13771)][[code](https://github.com/mnotgod96/AppAgent)]

Traditional Approaches

- uLink: Enabling User-Defined Deep Linking to App Content. [[Mobisys 2016](https://doi.org/10.1145/2906388.2906416)] 
- SUGILITE: Creating Multimodal Smartphone Automation by Demonstration. [CHI 2017] [[paper](https://doi.org/10.1145/3025453.3025483)][[code](https://github.com/tobyli/Sugilite_development)]
- Programming IoT devices by demonstration using mobile apps. [IS-EUD 2017]
- Kite: Building Conversational Bots from Mobile Apps. [MobiSys 2018]. [[paper](https://doi.org/10.1145/3210240.3210339)]
- Reinforcement Learning on Web Interfaces using Workflow-Guided Exploration. [ICLR 2018]. [[paper](https://arxiv.org/abs/1802.08802)][[code](https://github.com/stanfordnlp/wge)]
- Mapping Natural Language Instructions to Mobile UI Action Sequences. [ACL 2020] [[paper](https://arxiv.org/pdf/tbd.pdf)][[code](https://github.com/google-research-datasets/seq2act)] 
- Glider: A Reinforcement Learning Approach to Extract UI Scripts from Websites. [SIGIR 2021] [[paper](https://yuanchun-li.github.io/static/files/SIGIR2021_Glider.pdf)]
- UIBert: Learning Generic Multimodal Representations for UI Understanding. [IJCAI-21] [[paper](https://doi.org/10.24963/ijcai.2021/235)]
- META-GUI: Towards Multi-modal Conversational Agents on Mobile GUI. [EMNLP 2022][[paper](https://arxiv.org/abs/2205.11029)][[code](https://x-lance.github.io/META-GUI-Leaderboard/)]
- UINav: A maker of UI automation agents. [[paper](https://arxiv.org/abs/2312.10170)]


#### Benchmarks of UI Automation
- Mapping natural language commands to web elements. [EMNLP 2018] [[paper](https://doi.org/10.18653/v1/D18-1540)][[code](https://github.com/stanfordnlp/phrasenode)]
- UIBert: Learning Generic Multimodal Representations for UI Understanding. [IJCAI-21] [[paper](https://doi.org/10.24963/ijcai.2021/235)]
- Mapping Natural Language Instructions to Mobile UI Action Sequences. [ACL 2020] [[paper](https://arxiv.org/pdf/tbd.pdf)][[code](https://github.com/google-research-datasets/seq2act)] 
- A Dataset for Interactive Vision Language Navigation with Unknown Command Feasibility. [ECCV 2022][[paper](https://arxiv.org/abs/2202.02312)] [[code](https://github.com/aburns4/MoTIF)]
- META-GUI: Towards Multi-modal Conversational Agents on Mobile GUI. [EMNLP 2022][[paper](https://arxiv.org/abs/2205.11029)][[code](https://x-lance.github.io/META-GUI-Leaderboard/)]
- UGIF: UI Grounded Instruction Following. [[paper](https://arxiv.org/abs/2211.07615)]
- ASSISTGUI: Task-Oriented Desktop Graphical User Interface Automation. [[paper](https://arxiv.org/abs/2312.13108)][[code](https://github.com/showlab/assistgui)]
- Mind2Web: Towards a Generalist Agent for the Web. arxiv 2023 [[paper](https://arxiv.org/abs/2306.06070)][[code](https://github.com/OSU-NLP-Group/Mind2Web)][[code](https://github.com/google-research-datasets/uibert)]
- Android in the Wild: A Large-Scale Dataset for Android Device Control. [[paper](https://arxiv.org/abs/2307.10088)][[code](https://github.com/google-research/google-research/tree/master/android_in_the_wild)]
- Empowering LLM to use Smartphone for Intelligent Task Automation. [[paper](https://arxiv.org/abs/2308.15272)] [[code](https://github.com/MobileLLM/AutoDroid)]
- World of Bits: An Open-Domain Platform for Web-Based Agents. [ICML 2017] [[paper](https://dl.acm.org/doi/10.5555/3305890.3306005)][[code](https://github.com/Farama-Foundation/miniwob-plusplus)]
- Reinforcement Learning on Web Interfaces using Workflow-Guided Exploration. [ICLR 2018]. [[paper](https://arxiv.org/abs/1802.08802)][[code](https://github.com/stanfordnlp/wge)]
- WebShop: Towards Scalable Real-World Web Interaction with Grounded Language Agents. [NeurIPS 2022] [[paper](https://proceedings.neurips.cc/paper_files/paper/2022/file/82ad13ec01f9fe44c01cb91814fd7b8c-Paper-Conference.pdf)]
- AndroidEnv: A Reinforcement Learning Platform for Android [[paper](https://arxiv.org/abs/2105.13231)][[code](https://github.com/google-deepmind/android_env)]
- Mobile-Env: An Evaluation Platform and Benchmark for Interactive Agents in LLM Era. [[paper](https://arxiv.org/abs/2305.08144)][[code](https://github.com/X-LANCE/Mobile-Env)]
- WebArena: A Realistic Web Environment for Building Autonomous Agents. [[paper](https://arxiv.org/abs/2307.13854)][[code](https://github.com/web-arena-x/webarena)]


### Sensing

The ability to understand the current context is crucial for Personal LLM Agents to offer personalized, context-aware services.
This include the techniques to sense the user activity, mental status, environment dynamics, etc.

#### LLM-based Approaches

- “Automated Mobile Sensing Strategies Generation for Human Behaviour Understanding” (Gao et al., 2023, p. 521) [arxiv](https://arxiv.org/abs/2311.05457)
- “Cue-CoT: Chain-of-thought Prompting for Responding to In-depth Dialogue Questions with LLMs” (Wang et al., 2023, p. 1) [EMNLP 2023](https://aclanthology.org/2023.findings-emnlp.806/)
- “Exploring Large Language Models for Human Mobility Prediction under Public Events” (Liang et al., 2023, p. 1) [arxiv](https://arxiv.org/abs/2311.17351)
- “Penetrative AI: Making LLMs Comprehend the Physical World” (Xu et al., 2023, p. 1) [arxiv](https://arxiv.org/abs/2310.09605)
- “Evaluating Subjective Cognitive Appraisals of Emotions from Large Language Models” (Zhan et al., 2023, p. 1) [arxiv](https://arxiv.org/abs/2310.14389)
- “PALR: Personalization Aware LLMs for Recommendation” (Yang et al., 2023, p. 1) [arxiv](https://arxiv.org/abs/2305.07622)
- “Sentiment Analysis through LLM Negotiations” (Sun et al., 2023, p. 1) [arxiv](https://arxiv.org/abs/2311.01876)
- “Bridging the Information Gap Between Domain-Specific Model and General LLM for Personalized Recommendation” (Zhang et al., 2023, p. 1) [arxiv](https://arxiv.org/abs/2311.03778)
- “Conversational Health Agents: A Personalized LLM-Powered Agent Framework” (Abbasian et al., 2023, p. 1) [arxiv](https://arxiv.org/abs/2310.02374)
  
#### Traditional Approaches

- “Afective State Prediction from Smartphone Touch and Sensor Data in the Wild” (Wampfler et al., 2022, p. 1) [CHI'22](https://dl.acm.org/doi/abs/10.1145/3491102.3501835)
- “Mobile Localization Techniques for Wireless Sensor Networks: Survey and Recommendations” (Oliveira et al., 2023, p. 361) [ACM Transactions on Sensor Networks](https://dl.acm.org/doi/full/10.1145/3561512)
- “Are You Killing Time? Predicting Smartphone Users’ Time-killing Moments via Fusion of Smartphone Sensor Data and Screenshots” (Chen et al., 2023, p. 1) [CHI'23](https://dl.acm.org/doi/abs/10.1145/3544548.3580689)
- “Remote Breathing Rate Tracking in Stationary Position Using the Motion and Acoustic Sensors of Earables” (Ahmed et al., 2023, p. 1) [CHI'23](https://dl.acm.org/doi/abs/10.1145/3544548.3581265)
- “SAMoSA: Sensing Activities with Motion and Subsampled Audio” (Mollyn et al., 2022, p. 1321) [IMWUT](https://dl.acm.org/doi/abs/10.1145/3550284)
- “A Systematic Survey on Android API Usage for Data-Driven Analytics with Smartphones” (Lee et al., 2023, p. 1) [ACM Computing Surveys](https://dl.acm.org/doi/full/10.1145/3530814)

- “A Multi-Sensor Approach to Automatically Recognize Breaks and Work Activities of Knowledge Workers in Academia” (Di Lascio et al., 2020, p. 781) [IMWUT](https://dl.acm.org/doi/abs/10.1145/3411821)
- “Robust Inertial Motion Tracking through Deep Sensor Fusion across Smart Earbuds and Smartphone” (Gong et al., 2021, p. 621) [IMWUT](https://dl.acm.org/doi/abs/10.1145/3463517)
- “DancingAnt: Body-empowered Wireless Sensing Utilizing Pervasive Radiations from Powerline” (Cui et al., 2023, p. 873) [ACM MobiCom'23](https://dl.acm.org/doi/abs/10.1145/3570361.3613272)
- “DeXAR: Deep Explainable Sensor-Based Activity Recognition in Smart-Home Environments” (Arrotta et al., 2022, p. 11) [IMWUT](https://dl.acm.org/doi/abs/10.1145/3517224)
- “MUSE-Fi: Contactless MUti-person SEnsing Exploiting Near-field Wi-Fi Channel Variation” (Hu et al., 2023, p. 1135) [IMWUT](https://dl.acm.org/doi/abs/10.1145/3570361.3613290)
- “SenCom: Integrated Sensing and Communication with Practical WiFi” (He et al., 2023, p. 903) [ACM MobiCom'23](https://dl.acm.org/doi/abs/10.1145/3570361.3613274)
- “SleepMore: Inferring Sleep Duration at Scale via Multi-Device WiFi Sensing” (Zakaria et al., 2022, p. 1931) [IMWUT](https://dl.acm.org/doi/abs/10.1145/3569489)
  
- “COCOA: Cross Modality Contrastive Learning for Sensor Data” (Deldari et al., 2022, p. 1081) [ACM MobiCom'23](https://dl.acm.org/doi/abs/10.1145/3570361.3613290)
- “M3Sense: Affect-Agnostic Multitask Representation Learning Using Multimodal Wearable Sensors” (Samyoun et al., 2022, p. 731) [IMWUT](https://dl.acm.org/doi/abs/10.1145/3534600)
- “Predicting Subjective Measures of Social Anxiety from Sparsely Collected Mobile Sensor Data” (Rashid et al., 2020, p. 1091) [IMWUT](https://dl.acm.org/doi/abs/10.1145/3411823)
- “Attend and Discriminate: Beyond the State-of-the-Art for Human Activity Recognition Using Wearable Sensors” (Abedin et al., 2021, p. 11) [IMWUT](https://dl.acm.org/doi/abs/10.1145/3448083)
- “Fall Detection based on Interpretation of Important Features with Wrist-Wearable Sensors” (Kim et al., 2022, p. 1) [IMWUT](https://dl.acm.org/doi/abs/10.1145/3495243.3558250)

- “PowerPhone: Unleashing the Acoustic Sensing Capability of Smartphones” (Cao et al., 2023, p. 842) [ACM MobiCom'23](https://dl.acm.org/doi/abs/10.1145/3570361.3613270)
- “I Spy You: Eavesdropping Continuous Speech on Smartphones via Motion Sensors” (Zhang et al., 2022, p. 1971) [IMWUT](https://dl.acm.org/doi/abs/10.1145/3569486)
- “Watching Your Phone’s Back: Gesture Recognition by Sensing Acoustical Structure-borne Propagation” (Wang et al., 2021, p. 821) [IMWUT](https://dl.acm.org/doi/abs/10.1145/3463522)
- “Gesture Recognition Method Using Acoustic Sensing on Usual Garment” (Amesaka et al., 2022, p. 411) [IMWUT](https://dl.acm.org/doi/abs/10.1145/3534579)

<!-- #### By different sensing targets -->

- “Complex Daily Activities, Country-Level Diversity, and Smartphone Sensing: A Study in Denmark, Italy, Mongolia, Paraguay, and UK” (Assi et al., 2023, p. 1) [CHI'23](https://dl.acm.org/doi/abs/10.1145/3544548.3581190)
- “Generalization and Personalization of Mobile Sensing-Based Mood Inference Models: An Analysis of College Students in Eight Countries” (Meegahapola et al., 2022, p. 1761) [IMWUT](https://dl.acm.org/doi/abs/10.1145/3569483)
- “Detecting Social Contexts from Mobile Sensing Indicators in Virtual Interactions with Socially Anxious Individuals” (Wang et al., 2023, p. 1341) [IMWUT](https://dl.acm.org/doi/abs/10.1145/3610916)
- “Examining the Social Context of Alcohol Drinking in Young Adults with Smartphone Sensing” (Meegahapola et al., 2021, p. 1211) [IMWUT](https://dl.acm.org/doi/abs/10.1145/3478126)
- “Towards Open-Domain Twitter User Profile Inference” (Wen et al., 2023, p. 3172) [ACL 2023](https://aclanthology.org/2023.findings-acl.198/)
- “One More Bite? Inferring Food Consumption Level of College Students Using Smartphone Sensing and Self-Reports” (Meegahapola et al., 2021, p. 261) [IMWUT](https://dl.acm.org/doi/abs/10.1145/3448120)
- “FlowSense: Monitoring Airflow in Building Ventilation Systems Using Audio Sensing” (Chhaglani et al., 2022, p. 51) [IMWUT](https://dl.acm.org/doi/abs/10.1145/3517258)
- “MicroCam: Leveraging Smartphone Microscope Camera for Context-Aware Contact Surface Sensing” (Hu et al., 2023, p. 981) [IMWUT](https://dl.acm.org/doi/abs/10.1145/3610921)

<!-- #### Sensing the User
E.g. user activities, mental status, etc. -->

- “A Multi-Sensor Approach to Automatically Recognize Breaks and Work Activities of Knowledge Workers in Academia” (Di Lascio et al., 2020, p. 781) [IMWUT](https://dl.acm.org/doi/abs/10.1145/3411821)
- Mobile and Wearable Sensing Frameworks for mHealth Studies and Applications: A Systematic Review” (Kumar et al., 2021, p. 81) [ACM Transaction on Computing for Healthcare](https://dl.acm.org/doi/abs/10.1145/3422158)
- “Afective State Prediction from Smartphone Touch and Sensor Data in the Wild” (Wampfler et al., 2022, p. 1) [CHI'22](https://dl.acm.org/doi/abs/10.1145/3491102.3501835)
- “Are You Killing Time? Predicting Smartphone Users’ Time-killing Moments via Fusion of Smartphone Sensor Data and Screenshots” (Chen et al., 2023, p. 1) [CHI'23](https://dl.acm.org/doi/abs/10.1145/3544548.3580689)
- “FeverPhone: Accessible Core-Body Temperature Sensing for Fever Monitoring Using Commodity Smartphones” (Breda et al., 2022, p. 31) [IMWUT](https://dl.acm.org/doi/abs/10.1145/3580850)
- “Guard Your Heart Silently: Continuous Electrocardiogram Waveform Monitoring with Wrist-Worn Motion Sensor” (Cao et al., 2022, p. 1031) [IMWUT](https://dl.acm.org/doi/abs/10.1145/3550307)
- “Listen2Cough: Leveraging End-to-End Deep Learning Cough Detection Model to Enhance Lung Health Assessment Using Passively Sensed Audio” (Xu et al., 2021, p. 431) [IMWUT](https://dl.acm.org/doi/abs/10.1145/3448124)
- “HealthWalks: Sensing Fine-grained Individual Health Condition via Mobility Data” (Lin et al., 2020, p. 1381) [IMWUT](https://dl.acm.org/doi/abs/10.1145/3432229)
- “Identifying Mobile Sensing Indicators of Stress-Resilience” (Adler et al., 2021, p. 511) [IMWUT](https://dl.acm.org/doi/abs/10.1145/3463528)
- “MoodExplorer: Towards Compound Emotion Detection via Smartphone Sensing” (Zhang et al., 2018, p. 1761) [IMWUT](https://dl.acm.org/doi/abs/10.1145/3161414)
- “mTeeth: Identifying Brushing Teeth Surfaces Using Wrist-Worn Inertial Sensors” (Akther et al., 2021, p. 531) [IMWUT](https://dl.acm.org/doi/abs/10.1145/3463494)

- “Detecting Job Promotion in Information Workers Using Mobile Sensing” (Nepal et al., 2020, p. 1131) [IMWUT](https://dl.acm.org/doi/abs/10.1145/3414118)
- “First-Gen Lens: Assessing Mental Health of First-Generation Students across Their First Year at College Using Mobile Sensing” (Wang et al., 2022, p. 951) [IMWUT](https://dl.acm.org/doi/abs/10.1145/3543194)
- “Predicting Personality Traits from Physical Activity Intensity” (Gao et al., 2019, p. 1) [IEEE Computer](https://ieeexplore.ieee.org/abstract/document/8747565)
- “Predicting Symptom Trajectories of Schizophrenia using Mobile Sensing” (Wang et al., 2017, p. 1101) [IMWUT](https://dl.acm.org/doi/abs/10.1145/3130976)
- “Predictors of Life Satisfaction based on Daily Activities from Mobile Sensor Data” (Yürüten et al., 2014, p. 1) [CHI'14](https://dl.acm.org/doi/abs/10.1145/2556288.2557147)
- “SmartGPA: How Smartphones Can Assess and Predict Academic Performance of College Students” (Wang et al., 2015, p. 1) [UbiComp'15](https://dl.acm.org/doi/abs/10.1145/2750858.2804251)
- “Social Sensing: Assessing Social Functioning of Patients Living with Schizophrenia using Mobile Phone Sensing” (Wang et al., 2020, p. 1) [CHI'20](https://dl.acm.org/doi/abs/10.1145/3313831.3376855)
- “SmokingOpp: Detecting the Smoking ‘Opportunity’ Context Using Mobile Sensors” (Chatterjee et al., 2020, p. 41) [IMWUT](https://dl.acm.org/doi/abs/10.1145/3380987)


### Memorization

Memorization is about the ability of Personal LLM Agents to maintain information about the user, so that the agents can provide more customized services and evolve themselves according to user preferences.

#### Memory Obtaining

- “LifeLogging: Personal Big Data”  [Foundations and Trends in information retrieval](https://www.nowpublishers.com/article/Details/INR-033)
- “Vision-based human activity recognition: a survey”  [Multimedia Tools and Applications](https://link.springer.com/content/pdf/10.1007/s11042-020-09004-3.pdf)
- “Predicting personality from patterns of behavior collected with smartphones”  [Proceedings of the National Academy of Sciences](https://www.pnas.org/doi/epdf/10.1073/pnas.1920484117)
- “Facial Emotion Detection Using Deep Learning”  [2020 international conference for emerging technology (INCET)](https://www.researchgate.net/profile/Akriti-Jaiswal-5/publication/343414057_Facial_Emotion_Detection_Using_Deep_Learning/links/64e6fe3e0acf2e2b520d943b/Facial-Emotion-Detection-Using-Deep-Learning.pdf)
- “Emotion detection of textual data: An interdisciplinary survey”  [2021 IEEE World AI IoT Congress](https://www.researchgate.net/profile/Samira-Zad/publication/352580215_Emotion_Detection_of_Textual_Data_An_Interdisciplinary_Survey/links/60dbcb3e458515d6fbeab256/Emotion-Detection-of-Textual-Data-An-Interdisciplinary-Survey.pdf)

#### Memory Management
- “Privacystreams: Enabling transparency in personal data processing for mobile apps”  [IMWUT](https://dl.acm.org/doi/pdf/10.1145/3130941)
- “Tree of Thoughts: Deliberate Problem Solving with Large Language Models”  [arxiv](https://arxiv.org/pdf/2305.10601.pdf)
- “Chain-of-Thought Prompting Elicits Reasoning in Large Language Models”  [Advances in Neural Information Processing Systems](https://proceedings.neurips.cc/paper_files/paper/2022/file/9d5609613524ecf4f15af0f7b31abca4-Paper-Conference.pdf)
- “ReAct: Synergizing Reasoning and Acting in Language Models”  [arxiv](https://arxiv.org/pdf/2210.03629.pdf)
- “Generative Agents: Interactive Simulacra of Human Behavior”  [Proceedings of the 36th Annual ACM Symposium on User Interface Software and Technology](https://dl.acm.org/doi/pdf/10.1145/3586183.3606763)
- “Show Your Work: Scratchpads for Intermediate Computation with Language Models”  [arxiv](https://arxiv.org/pdf/2112.00114.pdf)
- “Cognitive Architectures for Language Agents”  [arxiv](https://arxiv.org/pdf/2309.02427.pdf)

#### Agent Self-evolution

- “DreamCoder: growing generalizable, interpretable knowledge with wake–sleep Bayesian program learning”  [Proceedings of the 42nd acm sigplan international conference on programming language design and implementation](https://dl.acm.org/doi/pdf/10.1145/3453483.3454080)
- “Voyager: An Open-Ended Embodied Agent with Large Language Models”  [arxiv](https://arxiv.org/pdf/2305.16291.pdf)
- “Language models as zero-shot planners: Extracting actionable knowledge for embodied agents”  [International Conference on Machine Learning](https://proceedings.mlr.press/v162/huang22a/huang22a.pdf)
- “Bootstrap Your Own Skills: Learning to Solve New Tasks with Large Language Model Guidance”  [arxiv](https://arxiv.org/pdf/2310.10021.pdf)
- “FireAct: Toward Language Agent Fine-tuning”  [arxiv](https://arxiv.org/pdf/2310.05915.pdf)
                           
## Efficiency of LLM Agents

The efficiency of LLM agents is closely related to the efficiency of LLM inference, LLM training/customization, and memory management.

### Efficient LLM Inference & Training

LLM inference/training efficiency has been comprehensively summarized in existing surveys (e.g. [this link](https://github.com/AIoT-MLSys-Lab/Efficient-LLMs-Survey)). Therefore, we omit this part in this list.

### Efficient Memory Retrieval & Management

Here we mainly list the papers related to the efficiency memory management, an important component of LLM-based agents.

#### Organizing the Memory 

(with vector library, vector DB, and others)

**Vector Library**

- RETRO: Improving language models by retrieving from trillions of tokens. [ICML, 2021] [[paper]()]
- RETA-LLM: A Retrieval-Augmented Large Language Model Toolkit. [arXiv, 2023] [[paper](https://arxiv.org/pdf/2306.05212.pdf)] [[code]( https://github.com/RUC-GSAI/YuLan-IR/tree/main/RETA-LLM)]
- TRIME: Training Language Models with Memory Augmentation. [EMNLP, 2022] [[paper]()] [[code](https://github.com/princeton-nlp/TRIME)]
- Enhancing LLM Intelligence with ARM-RAG: Auxiliary Rationale Memory for Retrieval Augmented Generation. [arXiv, 2023] [[paper](https://arxiv.org/abs/2311.04177)] [[code](https://github.com/ericmelz/arm-rag)]

**Vector Database**

- Survey of Vector Database Management Systems. [arXiv, 2023] [[paper](https://arxiv.org/pdf/2310.14021.pdf)]
- Vector database management systems: Fundamental concepts, use-cases, and current challenges. [arXiv, 2023] [[paper](https://arxiv.org/pdf/2309.11322.pdf)]
- A Comprehensive Survey on Vector Database: Storage and Retrieval Technique, Challenge. [arXiv, 2023] [[paper](https://arxiv.org/pdf/2310.11703.pdf)]

**Other Forms of Memory**

- Memorizing Transformers. [ICLR, 2022] [[paper](https://arxiv.org/pdf/2203.08913.pdf)] [[code](https://github.com/lucidrains/memorizing-transformers-pytorch)]
- RET-LLM: Towards a General Read-Write Memory for Large Language Models. [arXiv, 2023] [[paper](https://arxiv.org/pdf/2305.14322.pdf)]

#### Optimizing the Efficiency of Memory

**Searching Design**

- Milvus: A purpose-built vector data management system. [SIGMOD, 2021] [[paper]()(https://dl.acm.org/doi/10.1145/3448016.3457550)] [[code](https://github.com/milvus-io/milvus)]
- Analyticdb-v: A hybrid analytical engine towards query fusion for structured and unstructured data. [Proceedings of the VLDB Endowment, Volume 13, Issue 12, pp 3152–3165] [[paper](https://dl.acm.org/doi/10.14778/3415478.3415541)]
- Hqann: Efficient and robust similarity search for hybrid queries with structured and unstructured constraints. [CIKM, 2022] [[paper](https://dl.acm.org/doi/10.1145/3511808.3557610)]
- Qdrant [[github](https://github.com/qdrant/qdrant)]

**Searching Execution**

- Faiss:Facebook AI Similarity Search. [[wiki](https://github.com/facebookresearch/faiss/wiki)] [[code](https://github.com/facebookresearch/faiss)]
- Milvus: A purpose-built vector data management system. [SIGMOD, 2021] [[paper](https://dl.acm.org/doi/10.1145/3448016.3457550)] [[code](https://github.com/milvus-io/milvus)]
- Quicker ADC : Unlocking the Hidden Potential of Product Quantization With SIMD. [IEEE Transactions on Pattern Analysis and Machine Intelligence, 2019] [[paper](https://arxiv.org/pdf/1812.09162.pdf)] [[code](https://github.com/nlescoua/faiss-quickeradc)]

**Efficient Indexing**

- LSH: Locality-sensitive hashing scheme based on p-stable distributions. [SCG, 2004] [[paper](https://dl.acm.org/doi/10.1145/997817.997857)]
- Random projection trees and low dimensional manifolds. [STOC, 2008] [[paper](https://dl.acm.org/doi/10.1145/1374376.1374452)]
- SPANN: Highly-efficient Billion-scale Approximate Nearest Neighborhood Search. [NeurIPS, 2021] [[paper](https://openreview.net/pdf?id=-1rrzmJCp4)] [[code](https://github.com/microsoft/SPTAG)]
- Efficient and Robust Approximate Nearest Neighbor Search Using Hierarchical Navigable Small World Graphs. [IEEE Transactions on Pattern Analysis and Machine Intelligence, VOL. 42, NO. 4, 2020] [[paper](https://ieeexplore.ieee.org/document/8594636)]
- DiskANN: Fast Accurate Billion-point Nearest Neighbor Search on a Single Node. [NeurIPS, 2019] [[paper](https://proceedings.neurips.cc/paper_files/paper/2019/file/09853c7fb1d3f8ee67a61b6bf4a7f8e6-Paper.pdf)] [[code](https://github.com/microsoft/DiskANN)]
- DiskANN++: Efficient Page-based Search over Isomorphic Mapped Graph Index using Query-sensitivity Entry Vertex. [arXiv, 2023] [[paper](https://arxiv.org/pdf/2310.00402v5.pdf)]
- CXL-ANNS: Software-Hardware Collaborative Memory Disaggregation and Computation for Billion-Scale Approximate Nearest Neighbor Search. [USENIX ATC, 2023] [[paper](https://www.usenix.org/system/files/atc23-jang.pdf)] 
- Co-design Hardware and Algorithm for Vector Search. [SC, 2023] [[paper](https://dl.acm.org/doi/10.1145/3581784.3607045)] [[code](https://github.com/WenqiJiang/SC-ANN-FPGA)]

## Security & Privacy of Personal LLM Agents

Security & Privacy of AI/ML is a huge area with lots of related papers. Here we only focus on the ones related to LLM and LLM agents.

### Confidentiality (of User Data)

- THE-X: Privacy-Preserving Transformer Inference with Homomorphic Encryption. [ACL, 2022][[paper](https://arxiv.org/pdf/2206.00216.pdf)]
- TextFusion: Privacy-Preserving Pre-trained Model Inference via Token Fusion [EMNLP, 2022] [[paper](https://aclanthology.org/2022.emnlp-main.572.pdf)][[code](https://github.com/xzhou20/TextFusion)]
- TextObfuscator: Making Pre-trained Language Model a Privacy Protector via Obfuscating Word Representations. [ACL, 2023] [[paper](https://aclanthology.org/2023.findings-acl.337.pdf)][[code](https://github.com/xzhou20/TextObfuscator)]
- Adversarial Training for Large Neural Language Models. [arXiv, 2020] [[paper](https://arxiv.org/pdf/2004.08994.pdf)][[code](https://github.com/namisan/mt-dnn)]


### Integrity (of Agent Behavior)

**Adversarial Attacks**

- Certifying LLM Safety against Adversarial Prompting. [arXiv, 2023] [[paper](https://arxiv.org/pdf/2309.02705.pdf)][[code](https://github.com/aounon/certified-llm-safety)]
- On evaluating adversarial robustness of large vision-language models. [arXiv, 2023] [[paper](https://arxiv.org/pdf/2305.16934.pdf)][[code](https://github.com/yunqing-me/AttackVLM)]
- Jailbroken: How does llm safety training fail? [arXiv, 2023] [[paper](https://arxiv.org/pdf/2307.02483.pdf)]
- On the adversarial robustness of multi-modal foundation models. [arXiv, 2023] [[paper](https://arxiv.org/pdf/2308.10741.pdf)]
- Misusing Tools in Large Language Models With Visual Adversarial Examples. [arXiv, 2023] [[paper](https://arxiv.org/pdf/2310.03185.pdf)]
- Jailbreak in pieces: Compositional Adversarial Attacks on Multi-Modal Language Models. [arXiv, 2023] [[paper](https://arxiv.org/pdf/2307.14539.pdf)]

**Backdoor Attacks**

- Backdoor attacks for in-context learning with language models. [arXiv, 2023] [[paper](https://arxiv.org/pdf/2307.14692.pdf)]
- Prompt as Triggers for Backdoor Attack: Examining the Vulnerability in Language Models. [arXiv, 2023] [[paper](https://arxiv.org/pdf/2305.01219.pdf)]
- PoisonPrompt: Backdoor Attack on Prompt-based Large Language Models. [arXiv, 2023] [[paper](https://arxiv.org/pdf/2310.12439.pdf)][[code](https://github.com/grasses/PoisonPrompt)]
- Defending against backdoor attacks in natural language generation. [arXiv, 2021] [[paper](https://arxiv.org/pdf/2106.01810.pdf)][[code](https://github.com/ShannonAI/backdoor_nlg)]

**Prompt Injection Attacks**

- Not What You've Signed Up For: Compromising Real-World LLM-Integrated Applications with Indirect Prompt Injection. [arXiv, 2023] [[paper](https://arxiv.org/pdf/2302.12173.pdf)]
- Ignore Previous Prompt: Attack Techniques For Language Models. [arXiv, 2022] [[paper](https://arxiv.org/pdf/2211.09527.pdf)][[code](https://github.com/agencyenterprise/PromptInject)]
- Prompt Injection attack against LLM-integrated Applications. [arXiv, 2023] [[paper](https://arxiv.org/pdf/2306.05499.pdf)][[code](https://github.com/liu00222/Open-Prompt-Injection)]
- Jailbreaking Black Box Large Language Models in Twenty Queries. [arXiv, 2023] [[paper](https://arxiv.org/pdf/2310.08419.pdf)][[code](https://github.com/patrickrchao/JailbreakingLLMs)]
- Extracting Training Data from Large Language Models. [arXiv, 2020] [[paper](https://arxiv.org/pdf/2012.07805.pdf)]
- SmoothLLM: Defending Large Language Models Against Jailbreaking Attacks. [arXiv, 2023] [[paper](https://arxiv.org/pdf/2310.03684.pdf)][[code](https://github.com/arobey1/smooth-llm)]

### Reliability (of Agent Decisions)

**Problems**
- Survey of Hallucination in Natural Language Generation. [ACM Computing Surveys 2023] [[paper](https://dl.acm.org/doi/10.1145/3571730)]
- A Survey of Hallucination in Large Foundation Models. [arXiv, 2023] [[paper](https://arxiv.org/abs/2309.05922.pdf)]
- DERA: Enhancing Large Language Model Completions with Dialog-Enabled Resolving Agents. [arXiv, 2023] [[paper](https://arxiv.org/abs/2303.17071.pdf)]
- Cumulative Reasoning with Large Language Models. [arXiv, 2023] [[paper](https://arxiv.org/abs/2308.04371.pdf)]
- Learning From Mistakes Makes LLM Better Reasoner. [arXiv, 2023] [[paper](https://arxiv.org/abs/2310.20689v2)]
- Large Language Models can Learn Rules. [arXiv, 2023] [[paper](https://arxiv.org/abs/2310.07064)]

**Improvement**
- PromptSource: An Integrated Development Environment and Repository for Natural Language Prompts. [ACL 2022] [[paper](https://aclanthology.org/2022.acl-demo.9.pdf)]
- Super-NaturalInstructions: Generalization via Declarative Instructions on 1600+ NLP Tasks. [EMNLP 2022] [[paper](https://aclanthology.org/2022.emnlp-main.340.pdf)]
- Finetuned Language Models are Zero-Shot Learners. [ICLR 2022] [[paper](https://openreview.net/pdf?id=gEZrGCozdqR)]
- SELFCHECKGPT: Zero-Resource Black-Box Hallucination Detection for Generative Large Language Models. [EMNLP 2023] [[paper](https://aclanthology.org/2023.emnlp-main.557.pdf)]
- Large Language Models Can Self-Improve. [arXiv, 2022] [[paper](https://arxiv.org/pdf/2210.11610.pdf)]
- Self-Refine: Iterative Refinement with Self-Feedback. [arXiv, 2023] [[paper](https://arxiv.org/pdf/2303.17651.pdf)]
- Teaching Large Language Models to Self-Debug. [arXiv, 2023] [[paper](https://arxiv.org/abs/2304.05128.pdf)]
- Prompt-Guided Retrieval Augmentation for Non-Knowledge-Intensive Tasks. [ACL 2023] [[paper](https://aclanthology.org/2023.findings-acl.693.pdf)]
- Chain-of-Note: Enhancing Robustness in Retrieval-Augmented Language Models. [arXiv, 2023] [[paper](https://arxiv.org/abs/2311.09210.pdf)]
- Self-RAG: Learning to Retrieve, Generate, and Critique through Self-Reflection. [arXiv, 2023] [[paper](https://arxiv.org/abs/2310.11511.pdf)]
- Self-Knowledge Guided Retrieval Augmentation for Large Language Models. [Findings of EMNLP, 2023] [[paper](https://aclanthology.org/2023.findings-emnlp.691.pdf)]

**Inspection**
- CGMH: Constrained Sentence Generation by Metropolis-Hastings Sampling. [AAAI 2019] [[paper](https://arxiv.org/pdf/1811.10996.pdf)]
- Gradient-Based Constrained Sampling from Language Models. [EMNLP 2022] [[paper](https://aclanthology.org/2022.emnlp-main.144.pdf)]
- Large Language Models are Better Reasoners with Self-Verification. [Findings of EMNLP 2023] [[paper](https://aclanthology.org/2023.findings-emnlp.167.pdf)]
- Explainability for Large Language Models: A Survey. [arXiv, 2023] [[paper](https://arxiv.org/abs/2309.01029.pdf)]
- Self-Consistency Improves Chain of Thought Reasoning in Language Models. [ICLR, 2023] [[paper](https://openreview.net/pdf?id=1PL1NIMMrw)]
- Enhancing Chain-of-Thoughts Prompting with Iterative Bootstrapping in Large Language Models. [arXiv, 2023] [[paper](https://arxiv.org/pdf/2304.11657.pdf)]
- Mutual Information Alleviates Hallucinations in Abstractive
Summarization. [EMNLP, 2023] [[paper](https://aclanthology.org/2022.emnlp-main.399.pdf)]
- Overthinking the Truth: Understanding how Language Models Process False Demonstrations. [arXiv, 2023] [[paper](https://arxiv.org/abs/2307.09476.pdf)]
- Inference-Time Intervention: Eliciting Truthful Answers from a Language Model. [NeurIPS, 2023] [[paper](https://arxiv.org/abs/2306.03341.pdf)]

# Acknowledgment

We sincerely thank the valuable feedback from many domain experts including Xiaobo Peng (Autohome), Ligeng Chen (Honor Device), Miao Wei, Pengpeng He (Huawei), Hansheng Hong, Wenjun Chen, Zhiyao Yang (Oppo), Xuesheng Qi (vivo), Liang Tao, Lishun Sun, Shuang Dong (Xiaomi), and the anonymous others.

# Citation

TBD

