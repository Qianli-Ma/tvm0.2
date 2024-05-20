TVM: Tensor IR Stack for Deep Learning Systems
==============================================

[![GitHub license](http://dmlc.github.io/img/apache2.svg)](./LICENSE)
[![Build Status](http://mode-gpu.cs.washington.edu:8080/buildStatus/icon?job=dmlc/tvm/master)](http://mode-gpu.cs.washington.edu:8080/job/dmlc/job/tvm/job/master/)

[Installation](docs/how_to/install.md) |
[Documentation](http://docs.tvmlang.org) |
[Tutorials](http://tutorials.tvmlang.org) |
[Operator Inventory](topi) |
[FAQ](docs/faq.md) |
[Contributors](CONTRIBUTORS.md) |
[Release Notes](NEWS.md)

TVM is a Tensor intermediate representation(IR) stack for deep learning systems. It is designed to close the gap between the
productivity-focused deep learning frameworks, and the performance- and efficiency-focused hardware backends.
TVM works with deep learning frameworks to provide end to end compilation to different backends.
Checkout our [announcement](http://tvmlang.org/2017/08/17/tvm-release-announcement.html) for more details.

License
-------
© Contributors, 2017. Licensed under an [Apache-2.0](https://github.com/dmlc/tvm/blob/master/LICENSE) license.

Contribute to TVM
-----------------
TVM adopts apache committer model, we aim to create an open source project that is maintained and owned by the community.

- [Contributor Guide](docs/how_to/contribute.md)
- Please add your name to [CONTRIBUTORS.md](CONTRIBUTORS.md)
- Please also update [NEWS.md](NEWS.md) on changes and improvements in API and codes.

Acknowledgement
---------------
We learnt a lot from the following projects when building TVM.
- [Halide](https://github.com/halide/Halide): TVM uses [HalideIR](https://github.com/dmlc/HalideIR) as data structure for
  arithematic simplification and low level lowering. We also learnt and adapted some part of lowering pipeline from Halide.
- [Loopy](https://github.com/inducer/loopy): use of integer set analysis and its loop transformation primitives.
- [Theano](https://github.com/Theano/Theano): the design inspiration of symbolic scan operator for recurrence.

For [assignement-2018](https://github.com/Qianli-Ma/assignment2-2018)
---------------
The following instructions are tested for Ubuntu16.04

Clone using
```bash
git clone --recursive https://github.com/Qianli-Ma/tvm0.2.git
```
Compile TVM
```bash
mkdir build
cd build
cmake
make -j$(nproc)
```

Install to python (preferbably in virtual enviroment)
```bash
cd python
python setup.py install
cd ..
cd topi
python setup.py install
```
