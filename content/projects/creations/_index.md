---
title: "Projects"
sitemap:
  priority : 0.9
---


### [chainer_prefetch_multiprocess_iterator](https://github.com/serihiro/chainer_prefetch_multiprocess_iterator) (Python)

- This is the reference implementation of my study ["Accelerating Machine Learning I/O by Overlapping Data Staging and Mini-batch Generations"](https://doi.org/10.1145/3365109.3368768).
- This is a Chainer Iterator class that executes prefetching training data from slow storages (such like parallel file systems) into fast storage (such as SSD) and generating mini-batches in the same time.
- The aim of this study is to conceal the time for staging-in training dataset into node-local storages in computation nodes at HPC clusters (such as ABCI, TSUBAME, Cygnus, and so on).

### [chainer_minibatch_size_optimizer](https://github.com/serihiro/chainer_minibatch_size_optimizer) (Python)
- This is the reference implementation of my paper, [深層ニューラルネットワークにおける訓練高速化のための自動最適化](http://id.nii.ac.jp/1001/00194707/).
- This is a Chainer Trainer extension class that optimizes mini-batch size adaptically for training a model with one GPU.


### [inference_engine](https://github.com/serihiro/inference_engine) (C++)
- This is an ONNX runtime implementation, such like [onnxruntime](https://github.com/microsoft/onnxruntime) or [menoh](https://github.com/pfnet-research/menoh).
- For now, Gemm, Conv, MaxPool, Relu, Softmax, Dropout, Reshape are supported.
- All backend implementation is my own implementation for CPU (This means that current backend implementation does not use optimized matrix libraries, such like Blas, Intel MKL-DDN, and so on.).

### [simple_map_reduce](https://github.com/serihiro/simple_map_reduce) - Distributed MapReduce framework (Ruby)
- This is an experimental project to study MapReduce.
- [The blog post to illustrate this product (Japanese)](https://serihiro.hatenablog.com/entry/2018/02/12/191157).

### [optimization_experiments](https://github.com/serihiro/optimization_experiments) (C)
- This is an experimental project to study optimization for GEMM and GEMV.
- This projects includes dgemm and dgemv implementations which are optimized by `loop exchange`, `loop unloop`, `blcoknize`, `padding` repeatedly.

### [convolution_experiments](https://github.com/serihiro/convolution_experiments) (Python)
- This is an experimental project to study implementation for Convolution with `direct` and `im2col` style repeatedly.


### [config2args](https://github.com/serihiro/config2args) (Rust)
- This is a CLI tool to convert json config file into GNU CLI option style (such like `--key1 value1 --key2 value2`)
