# Awesome Self-supervised Speech Representation Learning
A comprehensive list of awesome self-supervised speech representation learning papers.

## Introduction

- Why Self-supervised Speech Representation Learning?
    - Unlabeled speech data are easier to collect.
    - Learning good representations might benefit various downstream tasks (speech recognition, speaker classification, diarization, etc.)
- What is the purpose of this repo?
    - Collects lastest works in this field for reference of future research.


## Contributing

Please help contribute this list by contacting [me](https://vectominist.github.io/) or add [pull request](https://github.com/vectominist/awesome-self-supervised-speech-representation-learning/pulls).

Markdown format:
```markdown
- Paper Name. 
  [[pdf]](link) 
  [[code]](link)
  - Author 1, Author 2, and Author 3. *Conference Year*
```

## Table of Contents

- [Paper List](#paper-list)
    - [Generative](#generative)
    - [Contrastive](#contrastive)
    - [Predictive](#predictive)
    - [Multitask Learning](#multitask-learning)
    - [Benchmark](#benchmark)
- [Toolkits](#toolkits)


## Paper List
### Generative
Generative approaches aim to reconstruct masked or future frames.

- Non-Autoregressive Predictive Coding for Learning Speech Representations from Local Dependencies (NPC)
    [[pdf]](https://arxiv.org/abs/2011.00406)
    [[code]](https://github.com/Alexander-H-Liu/NPC)
    - Alexander H. Liu, Yu-An Chung, James Glass. *Interspeech 2021*

- DeCoAR 2.0: Deep Contextualized Acoustic Representations with Vector Quantization
    [[pdf]](https://arxiv.org/abs/2012.06659)
    [[code]](https://github.com/awslabs/speech-representations)
    - Shaoshi Ling, Yuzong Liu. *ArXiv 2020*

- TERA: Self-Supervised Learning of Transformer Encoder Representation for Speech
    [[pdf]](https://arxiv.org/abs/2007.06028)
    [[code]](https://github.com/s3prl/s3prl)
    - Andy T. Liu, Shang-Wen Li, Hung-yi Lee. *IEEE/ACM TASLP 2021*

- Audio ALBERT: A Lite BERT for Self-supervised Learning of Audio Representation
    [[pdf]](https://arxiv.org/abs/2005.08575)
    [[code]](https://github.com/s3prl/s3prl)
    - Po-Han Chi, Pei-Hung Chung, Tsung-Han Wu, Chun-Cheng Hsieh, Yen-Hao Chen, Shang-Wen Li, Hung-yi Lee. *SLT 2021*

- Vector-Quantized Autoregressive Predictive Coding (VQ-APC)
    [[pdf]](https://arxiv.org/abs/2005.08392)
    [[code]](https://github.com/Alexander-H-Liu/NPC)
    - Yu-An Chung, Hao Tang, James Glass. *Interspeech 2020*

- Mockingjay: Unsupervised Speech Representation Learning with Deep Bidirectional Transformer Encoders
    [[pdf]](https://arxiv.org/abs/1910.12638)
    [[code]](https://github.com/s3prl/s3prl)
    - Andy T. Liu, Shu-wen Yang, Po-Han Chi, Po-chun Hsu, Hung-yi Lee. *ICASSP 2020*

- Deep Contextualized Acoustic Representations For Semi-Supervised Speech Recognition (DeCoAR)
    [[pdf]](https://arxiv.org/abs/1912.01679)
    [[code]](https://github.com/awslabs/speech-representations)
    - Shaoshi Ling, Yuzong Liu, Julian Salazar, Katrin Kirchhoff. *ICASSP 2020*

- An Unsupervised Autoregressive Model for Speech Representation Learning (APC)
    [[pdf]](https://arxiv.org/abs/1904.03240)
    [[code]](https://github.com/Alexander-H-Liu/NPC)
    - Yu-An Chung, Wei-Ning Hsu, Hao Tang, James Glass. *Interspeech 2019*

### Contrastive
Contrastive approaches use contrastive learning, i.e., predicting masked or future frames with negative examples.

- Robust wav2vec 2.0: Analyzing Domain Shift in Self-Supervised Pre-Training
    [[pdf]](https://arxiv.org/abs/2104.01027)
    [[code]](https://github.com/pytorch/fairseq)
    - Wei-Ning Hsu, Anuroop Sriram, Alexei Baevski, Tatiana Likhomanenko, Qiantong Xu, Vineel Pratap, Jacob Kahn, Ann Lee, Ronan Collobert, Gabriel Synnaeve, Michael Auli. *ArXiv 2021*

- wav2vec 2.0: A Framework for Self-Supervised Learning of Speech Representations
    [[pdf]](https://arxiv.org/abs/2006.11477)
    [[code]](https://github.com/pytorch/fairseq)
    - Alexei Baevski, Yuhao Zhou, Abdelrahman Mohamed, Michael Auli. *NeurIPS 2020*

- Learning Robust and Multilingual Speech Representations
    [[pdf]](https://arxiv.org/abs/2001.11128)
    - Kazuya Kawakami, Luyu Wang, Chris Dyer, Phil Blunsom, Aaron van den Oord. *Findings of EMNLP 2020*

- Unsupervised pretraining transfers well across languages (Modified CPC)
    [[pdf]](https://arxiv.org/abs/2002.02848)
    [[code]](https://github.com/facebookresearch/CPC_audio)
    - Morgane Rivière, Armand Joulin, Pierre-Emmanuel Mazaré, Emmanuel Dupoux. *ICASSP 2020*

- Effectiveness of self-supervised pre-training for speech recognition (Discrete BERT)
    [[pdf]](https://arxiv.org/abs/1911.03912)
    [[code]](https://github.com/pytorch/fairseq)
    - Alexei Baevski, Michael Auli, Abdelrahman Mohamed. *ArXiv 2019*

- vq-wav2vec: Self-Supervised Learning of Discrete Speech Representations
    [[pdf]](https://arxiv.org/abs/1910.05453)
    [[code]](https://github.com/pytorch/fairseq)
    - Alexei Baevski, Steffen Schneider, Michael Auli. *ICLR 2020*

- wav2vec: Unsupervised Pre-training for Speech Recognition
    [[pdf]](https://arxiv.org/abs/1904.05862)
    [[code]](https://github.com/pytorch/fairseq)
    - Steffen Schneider, Alexei Baevski, Ronan Collobert, Michael Auli. *Interspeech 2019*

- Representation Learning with Contrastive Predictive Coding (CPC)
    [[pdf]](https://arxiv.org/abs/1807.03748)
    [[code]](https://github.com/facebookresearch/CPC_audio)
    - Aaron van den Oord, Yazhe Li, Oriol Vinyals. *ArXiv 2018*

### Predictive
Predictive approaches aim to predict pseudo-labels of masked frames.
Pseudo-labels include K-means on MFCC or hidden features.

- HuBERT: Self-Supervised Speech Representation Learning by Masked Prediction of Hidden Units
    [[pdf]](https://arxiv.org/abs/2106.07447)
    [[code]](https://github.com/pytorch/fairseq)
    - Wei-Ning Hsu, Benjamin Bolte, Yao-Hung Hubert Tsai, Kushal Lakhotia, Ruslan Salakhutdinov, Abdelrahman Mohamed. *ICASSP 2021*

### Multitask Learning

- Multi-task self-supervised learning for Robust Speech Recognition (PASE+)
    [[pdf]](https://arxiv.org/abs/2001.09239)
    [[code]](https://github.com/santi-pdp/pase)
    - Mirco Ravanelli, Jianyuan Zhong, Santiago Pascual, Pawel Swietojanski, Joao Monteiro, Jan Trmal, Yoshua Bengio. *ICASSP 2020*

### Benchmark

- SUPERB: Speech processing Universal PERformance Benchmark
    [[pdf]](https://arxiv.org/abs/2105.01051)
    [[website]](https://superbbenchmark.org/)
    - Shu-wen Yang, Po-Han Chi, Yung-Sung Chuang, Cheng-I Jeff Lai, Kushal Lakhotia, Yist Y. Lin, Andy T. Liu, Jiatong Shi, Xuankai Chang, Guan-Ting Lin, Tzu-Hsien Huang, Wei-Cheng Tseng, Ko-tik Lee, Da-Rong Liu, Zili Huang, Shuyan Dong, Shang-Wen Li, Shinji Watanabe, Abdelrahman Mohamed, Hung-yi Lee. *Interspeech 2021*


## Toolkits

- [s3prl/s3prl](https://github.com/s3prl/s3prl)
- [pytorch/fairseq](https://github.com/pytorch/fairseq)

