OneFlow 作为下一代分布式深度学习框架，在性能、分布式方面具有多项明显优势，同时也在努力补齐完备性与易用性。

OneFlow 的研发团队具有的浓厚的工程师文化：超扁平化管理、优秀智慧的伙伴、不断创新的氛围、支持远程办公/实习。适合所有疯狂热爱技术的同学加入。

在[开源软件供应链点亮计划- 暑期 2021 活动](https://summer.iscas.ac.cn/) 中，OneFlow 将提供以下项目任务，并搭配导师，让大家以实习生身份来深入感受 OneFlow 的工作内容和氛围。

有其它想要了解的，也欢迎入群，OneFlow 爱好者 QQ 交流群：331883

![扫描二维码入群](./qq_group.png)

## 项目一：将 OneFlow 中的 CommNet 模块抽取为独立工程

#### 项目描述

CommNet 模块是 OneFlow 的底层通信模块。用于分布式训练时节点与节点之间的通信。 CommNet 采用了多种设计模式及优化技巧保证其底层协议的可扩展性及传输的高效性。CommNet 是纯异步且对深度学习最友好的高效网络传输模块。目前底层支持 RDMA 或者 epoll 方式，并且可以很方便地扩展底层通信方式。 由于 CommNet 模块易扩展、性能高效、协议简单等特性，不少项目希望将 CommNet 嵌入进自己的系统中用于网络通信。 在这个项目中，我们将从 OneFlow 中把 CommNet 抽取出来，作为一个独立工程，贡献给开源社区。

项目难度：中

项目社区导师：李新奇

导师联系方式：lixinqi@oneflow.org

相关资源：https://github.com/Oneflow-Inc/oneflow/tree/master/oneflow/core/comm_network

#### 项目产出要求

- 将CommNet独立为工程，附带能正常构建的CMake文件
- CommNet 的接口文档

#### 项目技术要求

- 一定的 C++ 代码阅读能力
- 对 CMake、Makefile 有一定了解
- 能在导师的指导下学习和理解项目中涉及的常见的设计模式


## 项目二：实现 einsum 算子

#### 项目描述

einsum 是一个强大又有趣的算子。OneFlow 目前还没有这个算子。如果尝试在 OneFlow 中添加这个算子，你不仅可以熟悉 OneFlow 的 Python 前端如何与 C++ 后端交互、掌握 CUDA 编程、深入体会 OneFlow 发明的 SBP 等概念如何在分布式训练中大显神威，还可以了解词法、语法分析等与编译有关的知识并立即应用在这个项目中。

项目难度：中

项目社区导师：蔡晟航

导师联系方式：caishenghang@oneflow.org

相关资源：https://pytorch.org/docs/stable/generated/torch.einsum.html?highlight=einsum#torch.einsum

#### 项目产出要求

- einsum 算子的 Python 前端
- einsum 算子的 CUDA Kernel
- einsum 算子的 CPU Kernel
- einsum 的接口文档
- einsum 的 Op 代码
- einsum 所需要的简单语法解析器

#### 项目技术要求

- 熟练掌握 Python
- 熟练掌握 C++
- 能够在导师的指导下学习编译原理相关知识并实现相关的词法、语法分析等功能
- 能在导师的指导下学习CUDA编程并实现 CUDA Kernel
- 对计算优化和高性能计算库有一定了解或有兴趣了解

## 项目三：OneFlow 部署实现 C/C++ API

#### 项目描述

收集数据、标注数据、搭建模型、进行训练、调参……直到得到一个精度不错的模型。所有这些工作，可能还只完成了工业落地的一半工作不到。训练好的模型需要部署上线，才能为业务逻辑提供底层支撑。 设计和开发部署框架时，需要考虑模型压缩、多平台支持、指定平台优化、高吞吐和低延迟……涉及的技术广度和深度都非常有趣。 OneFlow 已经有自己的部署模块，可以较为方便地部署已经训练好的模型。但是，目前 OneFlow 的部署还依赖 Python 解释器，在部署性能上还有提升空间。 这个项目中，你将在导师的指导下，基本要求是去掉 OneFlow 部署模块对 Python 的依赖，实现部署的 C/C++ 接口；在此基础上还有不少易用性、性能提升的工作，也非常值得尝试。

项目难度：高

项目社区导师：张文骁

导师联系方式：zhangwenxiao@oneflow.org

相关资源：https://github.com/Oneflow-Inc/oneflow/tree/master/oneflow/

#### 项目产出要求

- 在导师指导下，去掉部署模块对 Python 解释器的依赖
- 相关 API 接口的技术文档

#### 项目技术要求

- 了解部署的流程，熟悉常见的部署框架的操作流程
- 具有 C/C++ 开发能力
- 了解常见的网络协议，接触过网络编程

## 项目四：为 OneFlow XRT 后端提供 TVM 支持

#### 项目描述

OneFlow XRT 是 OneFlow 的一个子模块，用于适配张量编译器。通过 OneFlow XRT，我们可以将其它张量编译器的优化能力无缝地浅入到 OneFlow 运行时中。目前，OneFlow XRT 后端已经支持 XLA 与 TensorRT。 TVM 作为颇有影响力的机器学习编译框架，将其纳入 OneFlow XRT 的后端当然也是 OneFlow 的计划之一。

项目难度：高

项目社区导师：陈后江

导师联系方式：chenhoujiang@oneflow.org

相关资源：https://github.com/Oneflow-Inc/oneflow/tree/master/oneflow/xrt

#### 项目产出要求

- 为 OneFlow XRT 提供 TVM 后端支持
- 相关的技术文档

#### 项目技术要求

- 熟悉深度学习编译技术及其相关的优化技术
- 熟练掌握 C/C++
- 熟悉常见的设计模式，能够在导师的指导下掌握 OneFlow XRT 的设计理念及代码及代码结构

## 项目五：为 OneFlow 添加新的前端语言

#### 项目描述

因为各种机缘巧合和历史的必然，Python 成为了现在事实意义上的“人工智能编程语言”，OneFlow 也把 Python 作为了用户接口语言。 然而事实上，Python 只是 OneFlow 的前端，复杂的计算和并行功能代码，还是通过 C/C++ 实现的，OneFlow 良好的解耦设计，使得我们可以较容易的支持 Python 作为用户接口，自然也可以支持更多的语言作为用户接口。 不管是 Javascript、Swift、Ruby…… 只要你感兴趣，都可以加入这个项目，尝试在 OneFlow 的用户侧支持它。

项目难度：中

项目社区导师：蔡晟航

导师联系方式：caishenghang@oneflow.org

相关资源：https://github.com/Oneflow-Inc/oneflow/tree/master/oneflow/

#### 项目产出要求

- 为 OneFlow 新增一种脚本语言支持
- 对应语言接口的 API 文档规范、准则

#### 项目技术要求

- 了解常见脚本语言与 Native 代码的交互机制
- 熟练掌握想移植的前端语言
- 掌握 C/C++
- 了解动态链接、多线程锁等技术或者有兴趣在导师指导下学习掌握





## 项目六：自动并行中的算力代价建模

#### 项目描述

数据并行、模型并行、流水并行、混合并行……随着分布式训练中并行方式越来越复杂，由框架自动寻找较好的并行策略（寻找全局最好的策略是 NP 难度的问题），即自动并行技术，成为了研究热点。 OneFlow 中的自动并行技术中所使用的代价模型主要有两类：基于传输代价的，和基于算力代价的。 在这个项目中，你需要在导师的指导下，为某些算子的算力代价建模，并实现相关的代价函数。相关问题在工业界和学界都是新兴的，适合勇于探索的同学。

项目难度：高

项目社区导师：李一鹏

导师联系方式：liyipeng@oneflow.org

相关资源：https://github.com/Oneflow-Inc/oneflow/tree/master/oneflow/

#### 项目产出要求

- 实现基于算力代价的评估函数
- 在导师的指导下，相关研究结果整理为文档（根据产出质量，可考虑发论文或申请专利）

#### 项目技术要求

- 扎实的数理基础
- 了解或熟悉 C/C++ 开发

## 项目七：OneFlow 多设备类型支持

#### 项目描述

目前最新 OneFlow 的 Release 版本，仅支持 CPU 及 英伟达 GPU 设备。为适配更多兴起的新型芯片、AI 加速器，OneFlow 在 master 分支已经重构了部分代码，降低为 OneFlow 新增设备支持的难度，目前已经有初步的多设备支持框架，包括：1. 对各种设备抽象出设备中间层，应对新增设备的变化 2. 将新增设备的信息改为注册制，便于新增设备类型的管理 3. 部分去除原有代码中假定设备类型只有 CPU 或者 GPU 的依赖。并且在重构的框架下跑通了新增设备的神经网络测试。 

未来 OneFlow 将可以依赖多设备支持框架，快速优雅地增加对新计算设备的支持。不过，在正式发布前，还有一些细节需要打磨，主要体现在：1. 将多设备支持框架与 OneFlow 的分布式模块和动态图模块完全融合 2. 完全去除 Python 层对设备类型假定只有 CPU 或 GPU 的依赖 3. 在多设备框架的基础上，及软硬件导师的指导下，为 OneFlow 增加新设备支持 以上各个任务都有多个难度层次的子任务，除熟悉 C++ 外，并不需要太多的额外前置知识。适合熟悉 C++ 并有意借此机会深入了解深度学习框架如何驱使底层计算设备工作的原理的同学。也适合想借此机会锤炼自己的编程能力，深入实践设计模式的同学。

项目难度：中

项目社区导师：张建浩

导师联系方式：zhangjianhao@oneflow.org

相关资源：https://github.com/Oneflow-Inc/oneflow/tree/master/oneflow/

#### 项目产出要求

- 完全去除 Python 层对设备类型限制的假定
- 完善新增设备类型的注册机制
- 将多设备支持模块与分布式模块融合
- 将多设备支持模块与动态图模块融合
- 相关设计文档及接口文档

#### 项目技术要求

- 熟悉 C++
- 了解 OneFlow 或某一种深度学习框架的基本使用

## 项目八：为 OneFlow 的图编译后端提供获取网络权重的支持

#### 项目描述

OneFlow 的 Python 接口用于搭建神经网络的结构，当程序运行时，用户搭建的神经网络结构，将转化为 OneFlow 后端可以读取和解析的图数据结构，由 OneFlow 后端进行解析和优化。优化的过程包括图变换（Pass）。 当前 OneFlow 中的图变换，只能获取图中的拓扑关系信息，还无法获取权重信息，使得一些常见的 Pass （如将 conv 和 batchnorm 融合）无法实现。 在这个项目中，你将在导师的指导下，了解 Pass 的基本概念及难点（如果已经掌握了更好），根本地解决 OneFlow 的 Pass 过程中无法获取权重信息这个问题。如果还有余力及兴趣，也可以在此基础上，继续为 OneFlow 创造新的 Pass 用于图优化，甚至实现自动生成而不是基于规则手写 Pass 的机制。

项目难度：中

项目社区导师：张建浩

导师联系方式：zhangjianhao@oneflow.org

相关资源：https://github.com/Oneflow-Inc/oneflow/tree/master/oneflow/

#### 项目产出要求

- 重构相关 Python 端
- 重构 C++ 后端 Pass 模块的相关功能
- 相关的设计文档及 API 文档
- 相关的测试代码
- 在获取权重的基础上的新 Pass

#### 项目技术要求

- 熟悉 C++
- 了解深度学习编译技术（或者可以在导师指导下学习）

## 项目九：为 OneFlow 添加自动判断重计算区域功能

#### 项目描述

重计算（rematerialization，也有 gradient checkpointing 的称法）是一种时间换空间的优化方法，它在神经网络训练中的应用最早由陈天奇团队提出（arXiv:1604.06174）。在以上工作中，需要手工指定重计算区域，目前 OneFlow 采用的也是这种方式。但是在基于陈团队的优化方法的一些后续工作中，有不少工作提出了自动判断性价比最高的重计算区域的方法（如 arXiv:2006.09616）。在这个项目中，你将在导师的指导下，阅读相关资料及代码，并在 OneFlow 中落地自动判断重计算区域的相关功能。

项目难度：中

项目社区导师：张建浩

导师联系方式：zhangjianhao@oneflow.org

相关资源：https://arxiv.org/abs/1604.06174 https://arxiv.org/abs/2006.09616

#### 项目产出要求

- 在导师指导下，对相关文献进行调研并形成文档
- 在 OneFlow 中实现自动判断重计算区域的相关功能
- 相关的设计文档及接口文档

#### 项目技术要求

- 熟悉 C++
- 了解亚线性优化技术或能在指导下学习

## 项目十：NVlabs imaginaire 仓库的模型复现

#### 项目描述

NVlabs imaginaire 是英伟达维护的一个使用 PyTorch 实现的模型仓库。包含了多个与图像、视频生成方法有关的模型。生成对抗类神经网络（GAN）对硬件资源的要求非常高，NVlabs imaginaire 中的模型也不例外，在该仓库中的各模型，往往需要昂贵的深度学习主机（如 NVIDIA DGX1）和一定数量的高端显卡（如8张 V100)，这使得复现这些模型的工作难以“平民化”展开。
OneFlow 充分发挥自身分布式的优势，使用 OneFlow 重写这些模型后，可以使用多张“不那么昂贵”的显卡（如 2080）和主机组成集群，完成同样的训练任务。将这类模型的研究技术平民化、大众化。

项目难度：中

项目社区导师：梁德澎

导师联系方式：liangdepeng@oneflow.org

相关资源：https://github.com/NVlabs/imaginaire

#### 项目产出要求

- 对选定的模型使用 OneFlow 进行重写
- 通过对比 loss 下降曲线等方法，完成模型的正确性验证
- 使用 OneFlow 完成相关模型的分布式训练，并形成可复用的脚本及文档
- 相关的预训练模型

#### 项目技术要求

- 熟悉深度学习常见算法及理论
- 熟悉 PyTorch，能独立阅读学习 NVlabs imaginaire 仓库源码
- 了解 OneFlow 的使用，可以在指导下完成分布式训练

## 项目十一：给 TVM 添加 OneFlow 前端

#### 项目描述

TVM 作为当代应用最广泛的深度学习编译器支持将各种主流深度学习框架（如 TensorFlow/Pytorch/MxNet 等）模型直接转换为 TVM 的中间表示，可以实现在 GPU，CPU，FPGA 等各种后端硬件上部署，并结合 Auto TVM，Ansor 等技术可以在各种后端上取得较好的通用推理效率。

OneFlow 作为一个深度学习训练框架，将其训练的深度学习模型高效的部署到各个平台上也是重要的一环。但 OneFlow 目前没有提供通用的模型部署方案，因此本项目旨在为 TVM 添加 OneFlow 前端。使得 TVM 可以直接加载 OneFlow 训练的模型并转换为 TVM 的 Graph IR，然后在各种后端硬件上进行部署。另外，OneFlow 目前不仅支持 FP32 和 FP16 的训练，还很好的支持了 INT8 量化训练。所以本项目还期望在为 TVM 支持 OneFlow 前端的过程中，也可以实现部署 OneFlow 的 INT8 量化训练模型。



项目难度：中

项目社区导师：张晓雨

导师联系方式：zhangxiaoyu@oneflow.org

相关资源：https://tvm.apache.org/

#### 项目产出要求

- 为 TVM 支持 OneFlow 前端，支持在 TVM 中直接加载 OneFlow 的模型并推理。
- 完善 TVM 支持 OneFlow 前端的文档和使用示例，提交 PR 给 TVM，合进 TVM 官方仓库，并负责输出一篇 TVM 如何添加 OneFlow 前端的文档。
- 基于 TVM 的 OneFlow 前端完成常见模型如 ResNet50、MobileNet、Transformer 等在 TVM 中的部署。测试精度速度并整理报告文档。

#### 项目技术要求

- 熟悉 Python，了解单元测试
- 了解 OneFlow 的使用，可以搭建常用模型进行推理
- 了解 TVM 的使用，有深度学习编译器相关经验更佳
- 了解深度学习模型量化训练
