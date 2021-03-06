---
title: "Accelerating Machine Learning I/O by Overlapping Data Staging and Mini-batch Generations"
date: 2019-12-04
pubtype: "International conference"
featured: true
description: "The academic paper that I submitted to \"the 6th IEEE/ACM International Conference on Big Data Computing, Applications and Technologies (BDCAT'19)\""
tags: ["Proceedings", "International Conference"]
link: "https://doi.org/10.1145/3365109.3368768"
sitemap:
  priority : 1.0
---

[The slide of this talk](https://speakerdeck.com/serihiro/o-by-overlapping-data-staging-and-mini-batch-generations)

The training dataset used in deep neural networks (DNNs) keeps on increasing. When a training dataset grows larger, the reading performance of such a large training dataset becomes a problem. A high-performance computing (HPC) cluster has high performance I/O storage devices, for example, NVMe SSD, as local storage on each compute node. This high-performance I/O storage can mitigate the I/O bottleneck. However, such storage devices provide only temporary storage, therefore the users have to copy the training dataset from shared storage (such as Lustre) into local storage. Large datasets (over a few hundred GiB) takes a long time to copy the datasets between local storage and shared storage. To solve this problem, we propose a method to conceal the time spent on copying dataset to local storage by overlapping the copying and reading of training data. We implemented the proposed method at the machine learning framework Chainer. The results of our experiments showed that the read I/O bandwidth of our method improved from 1.38 times to 6.19 times compared with reading the dataset from Lustre directly using Chainer standard class. Moreover, evaluation of data parallel training showed that our method improved the performance from 1.26 times to 1.74 times for the same comparison.

```bibtex
@inproceedings{10.1145/3365109.3368768,
  author = {Serizawa, Kazuhiro and Tatebe, Osamu},
  title = {Accelerating Machine Learning I/O by Overlapping Data Staging and Mini-Batch Generations},
  year = {2019},
  isbn = {9781450370165},
  publisher = {Association for Computing Machinery},
  address = {New York, NY, USA},
  url = {https://doi.org/10.1145/3365109.3368768},
  doi = {10.1145/3365109.3368768},
  abstract = {The training dataset used in deep neural networks (DNNs) keeps on increasing. When a training dataset grows larger, the reading performance of such a large training dataset becomes a problem. A high-performance computing (HPC) cluster has high performance I/O storage devices, for example, NVMe SSD, as local storage on each compute node. This high-performance I/O storage can mitigate the I/O bottleneck. However, such storage devices provide only temporary storage, therefore the users have to copy the training dataset from shared storage (such as Lustre) into local storage. Large datasets (over a few hundred GiB) takes a long time to copy the datasets between local storage and shared storage. To solve this problem, we propose a method to conceal the time spent on copying dataset to local storage by overlapping the copying and reading of training data. We implemented the proposed method at the machine learning framework Chainer. The results of our experiments showed that the read I/O bandwidth of our method improved from 1.38 times to 6.19 times compared with reading the dataset from Lustre directly using Chainer standard class. Moreover, evaluation of data parallel training showed that our method improved the performance from 1.26 times to 1.74 times for the same comparison.},
  booktitle = {Proceedings of the 6th IEEE/ACM International Conference on Big Data Computing, Applications and Technologies},
  pages = {31???34},
  numpages = {4},
  keywords = {data staging, hpc, deep learning},
  location = {Auckland, New Zealand},
  series = {BDCAT '19}
}
```
