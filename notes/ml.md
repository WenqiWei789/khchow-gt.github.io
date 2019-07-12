# Machine Learning
This is a curated list of representative papers on machine learning maintained by [Ka-Ho Chow](https://khchow.com). [[Edit]](https://github.com/khchow-gt/khchow-gt.github.io/edit/master/notes/ml.md)

---

## Security on Deep Neural Networks

### Adversarial Attacks

* [Intriguing Properties of Neural Networks](https://arxiv.org/abs/1312.6199) - Christian Szegedy et al., 2014
* [Explaining and Harnessing Adversarial Examples](https://arxiv.org/abs/1412.6572) - Ian J. Goodfellow et al., ICLR 2015
* [The Limitations of Deep Learning in Adversarial Settings](https://ieeexplore.ieee.org/abstract/document/7467366/) - Nicolas Papernot  et al., Euro S&P 2016
* [DeepFool: A Simple and Accurate Method to Fool Deep Neural Networks](https://www.cv-foundation.org/openaccess/content_cvpr_2016/html/Moosavi-Dezfooli_DeepFool_A_Simple_CVPR_2016_paper.html) - Seyed-Mohsen Moosavi-Dezfooli et al., CVPR 2016
* [Transferability in Machine Learning: from Phenomena to Black-Box Attacks using Adversarial Samples](https://arxiv.org/abs/1605.07277) - Nicolas Papernot et al., 2016
* [Adversarial Examples in the Physical World](https://arxiv.org/abs/1607.02533) - Alexey Kurakin et al., ICLR 2017
* [Adversarial Machine Learning at Scale](https://arxiv.org/abs/1611.01236) - Alexey Kurakin et al., ICLR 2017
* [Delving into Transferable Adversarial Examples and Black-box Attacks](https://arxiv.org/abs/1611.02770) - Yanpei Liu et al., ICLR 2017
* [Towards Evaluating the Robustness of Neural Networks](https://nicholas.carlini.com/papers/2017_sp_nnrobustattacks.pdf) - Nicholas Carlini et al., S&P 2017
* [Practical Black-Box Attacks against Machine Learning](https://dl.acm.org/citation.cfm?id=3053009) - Nicolas Papernot et al., 2017
* [EAD: Elastic-Net Attacks to Deep Neural Networks via Adversarial Examples](https://arxiv.org/abs/1709.04114) - Pin-Yu Chen et al., AAAI 2018 ✔
* [Attacking the Madry Defense Model with L1-based Adversarial Examples](https://arxiv.org/abs/1710.10733) - Yash Sharma et al., ICLR 2018 (Workshop) ✔

### Adversarial Defenses
* [Distillation as a Defense to Adversarial Perturbations Against Deep Neural Networks](https://ieeexplore.ieee.org/abstract/document/7546524/) - Nicolas Papernot et al., 2016
* [MagNet: a Two-Pronged Defense against Adversarial Examples](https://arxiv.org/abs/1705.09064) - Dongyu Meng et al., CCS 2017
* [Feature Squeezing: Detecting Adversarial Examples in Deep Neural Networks](https://arxiv.org/abs/1704.01155) - Weilin Xu et al., NDSS 2018
* [Defense-GAN: Protecting Classifiers Against Adversarial Attacks Using Generative Models](https://arxiv.org/abs/1805.06605) - Pouya Samangouei et al., ICLR 2018
* [Ensemble Adversarial Training: Attacks and Defenses](https://arxiv.org/abs/1705.07204) - Florian Tramèr et al., ICLR 2018
* [Towards Deep Learning Models Resistant to Adversarial Attacks](https://arxiv.org/abs/1706.06083) - Aleksander Madry et al., ICLR 2018 ✔

### Robustness

* [Maximum Resilience of Artificial Neural Networks](https://arxiv.org/abs/1705.01040) - Chih-Hong Cheng et al., ATVA 2017 *
* [Output Range Analysis for Deep Neural Networks](https://arxiv.org/abs/1709.09130) - Souradeep Dutta et al., NFM 2018 *
* [Formal Security Analysis of Neural Networks using Symbolic Intervals](https://arxiv.org/abs/1804.10829) - Shiqi Wang et al., USENIX Security 2018 *
* [Efficient Formal Safety Analysis of Neural Networks](https://arxiv.org/abs/1809.08098) - Shiqi Wang et al., NIPS 2018 *
* [A Unified View of Piecewise Linear Neural Network Verification](https://arxiv.org/abs/1711.00455) - Rudy Bunel et al., NIPS 2018 *
* [Scaling Provable Adversarial Defenses](https://arxiv.org/abs/1805.12514) - Eric Wong et al., NIPS 2018 *
* [Evaluating the Robustness of Neural Networks: An Extreme Value Theory Approach](https://arxiv.org/abs/1801.10578) - Tsui-Wei Weng et al., ICLR 2018 *
* [Evaluating Robustness of Neural Networks with Mixed Integer Programming](https://arxiv.org/abs/1711.07356) - Vincent Tjeng et al., ICLR 2019 *

---

## Autoencoders

* [Extracting and Composing Robust Features with Denoising Autoencoders](http://www.cs.toronto.edu/~larocheh/publications/icml-2008-denoising-autoencoders.pdf) - Pascal Vincent et al., ICML 2008 ✔
* [Stacked Denoising Autoencoders: Learning Useful Representations in a Deep Network with a Local Denoising Criterion](http://www.jmlr.org/papers/volume11/vincent10a/vincent10a.pdf) - Pascal Vincent et al., JMLR 2010 ✔
* [Anomaly Detection with Robust Deep Autoencoders](https://www.eecs.yorku.ca/course_archive/2017-18/F/6412/reading/kdd17p665.pdf) - Chong Zhou et al., KDD 2018 ✔ [[Code]](https://github.com/zc8340311/RobustAutoencoder)

---

## Graphs

### Network Representation Learning
The complete list of must-read papers can be found [here](https://github.com/thunlp/NRLPapers) and the open source toolkit [OpenNE](https://github.com/thunlp/openne) supports most of the representative algorithms.

* [DeepWalk: Online Learning of Social Representations](https://arxiv.org/pdf/1403.6652) - Bryan Perozzi et al., KDD 2014 ✔
* [GraRep: Learning Graph Representations with Global Structural Information](https://dl.acm.org/citation.cfm?id=2806512) - Shaosheng Cao et al., CIKM 2015
* [LINE: Large-scale Information Network Embedding](https://arxiv.org/pdf/1503.03578.pdf) - Jian Tang et al., WWW 2015 ✔
* [node2vec: Scalable Feature Learning for Networks](http://www.kdd.org/kdd2016/papers/files/rfp0218-groverA.pdf) - Aditya Grover et al., KDD 2016 ✔
* [Structural Deep Network Embedding](https://www.kdd.org/kdd2016/papers/files/rfp0191-wangAemb.pdf) - Daixin Wang et al., KDD 2016
* [Network Embedding as Matrix Factorization: Unifying DeepWalk, LINE, PTE, and node2vec](http://keg.cs.tsinghua.edu.cn/jietang/publications/WSDM18-Qiu-et-al-NetMF-network-embedding.pdf) - Jiezhong Qiu et al., WSDM 2018
* [A Survey on Network Embedding](https://arxiv.org/pdf/1711.08752.pdf) - Peng Cui et al., AAAI 2018 ✔

#### Dynamic Networks
* [Dynamic Network Embedding: An Extended Approach for Skip-gram based Network Embedding](https://www.ijcai.org/proceedings/2018/0288.pdf) - Lun Du et al., IJCAI 2018 ✔
* [DepthLGP: Learning Embeddings of Out-of-Sample Nodes in Dynamic Networks](https://aaai.org/ocs/index.php/AAAI/AAAI18/paper/view/17096) - Jianxin Ma et al., AAAI 2018
* [High-Order Proximity Preserved Embedding for Dynamic Networks](https://ieeexplore.ieee.org/document/8329541) - Dingyuan Zhu et al., TKDE
* [TIMERS: Error-Bounded SVD Restart on Dynamic Networks](https://www.aaai.org/ocs/index.php/AAAI/AAAI18/paper/viewFile/16674/15691) - Ziwei Zhang et al., AAAI 2018
* [Scalable Optimization for Embedding Highly-Dynamic and Recency-Sensitive Data](https://www.kdd.org/kdd2018/accepted-papers/view/scalable-optimization-for-embedding-highly-dynamic-and-recency-sensitive-da) - Xumin Chen et al., KDD 2018

### Adversarial Attacks on Graphs

* [Adversarial Attacks on Neural Networks for Graph Data](https://dl.acm.org/authorize?N665889) - Daniel Zügner et al., KDD 2018 (Best Paper)
* [Adversarial Attacks on Graph Structured Data](https://arxiv.org/pdf/1806.02371.pdf) - Hanjun Dai et al., ICML 2018
* [Adversarial Attacks on Node Embeddings via Graph Poisoning](https://arxiv.org/pdf/1809.01093.pdf) - Aleksandar Bojchevski et al., ICML 2019
* [Adversarial Attacks on Graph Neural Networks via Meta Learning](https://openreview.net/pdf?id=Bylnx209YX) - Daniel Zugner et al., ICLR 2019
* [Towards Data Poisoning Attack against Knowledge Graph Embedding](https://arxiv.org/pdf/1904.12052.pdf) - Hengtong Zhang et al., IJCAI 2019

### Adversarial Learning for Network Representation Learning

* [Adversarial Network Embedding](https://www.aaai.org/ocs/index.php/AAAI/AAAI18/paper/view/16498/15927) - Quanyu Dai et al., AAAI 2018 ✔
* [Graph Representation Learning with Generative Adversarial Nets](https://www.aaai.org/ocs/index.php/AAAI/AAAI18/paper/download/16611/15969) - Hongwei Wang et al., AAAI 2018
* [Adversarially Regularized Graph Autoencoder for Graph Embedding](https://www.ijcai.org/proceedings/2018/0362.pdf) - Shirui Pan et al., IJCAI 2018 ✔
* [Learning Deep Network Representations with Adversarially Regularized Autoencoders](https://dl.acm.org/authorize.cfm?key=N665860) - Wenchao Yu et al., KDD 2018
* [Semi-supervised Learning on Graphs with Generative Adversarial Nets](https://dl.acm.org/citation.cfm?id=3271768) -	Ming Ding et al., CIKM 2018 ✔
* [NetGAN: Generating Graphs via Random Walks](http://proceedings.mlr.press/v80/bojchevski18a/bojchevski18a.pdf) - Aleksandar Bojchevski et al., ICML 2018
* [Adversarial Training Methods for Network Embedding](https://dl.acm.org/citation.cfm?id=3313445) - Quanyu Dai et al., WWW 2019 ✔

### Datasets

* [BlogCatalog](http://socialcomputing.asu.edu/datasets/BlogCatalog) is a social network for users to publish blogs. In this dataset, each node is a BlogCatalog user and each edge is a friendship connection. Each node has multiple labels, indicating the topics of the user’s blog topics.
* [Flickr](http://socialcomputing.asu.edu/datasets/Flickr) is social network for users to share images and videos. In this dataset, each node is a Flickr user and each edge is a friendship connection. Each node has a label, indicating the user’s interest group.
* [YouTube](http://socialcomputing.asu.edu/datasets/YouTube) is a video sharing site where various interactions occur between users including contacts, subscriptions and favorite videos. In this dataset, each node is a YouTube user and each edge is a friendship connection. Each node has a label, indicating the user’s interest group.
* [Wikipedia](http://snap.stanford.edu/node2vec/POS.mat) is a co-occurrence network of words appearing in the fist million bytes of the Wikipedia dump. In this dataset, each node is a word and each edge is a word co-occurrence relationship. Each node has a label, indicating the word’s part-of-speech tag.
* [DBLP](https://aminer.org/citation) is an academic paper citation network built upon the DBLP repository.  In this dataset, each node is a paper and each edge is a citation. Each node has a label, indicating one of the areas for its paper’s conference venue.

---

## Adversarial Learning

* [Adversarial Autoencoders](https://arxiv.org/pdf/1511.05644.pdf) - Alireza Makhzani et al., ICLR 2016
* [Adversarial Feature Learning](https://arxiv.org/abs/1605.09782) - Jeff Donahue et al., ICLR 2017

---

## AutoML

* [The Lottery Ticket Hypothesis: Finding Sparse, Trainable Neural Networks](https://arxiv.org/pdf/1803.03635.pdf) - Jonathan Frankle et al., ICLR 2019 (Best Paper)
