# proj65-build-kernel-with-profile-guided-gcc

### 项目名称 
基于gcc反馈编译优化的Linux kernel构建

### 项目描述

- 反馈编译优化（Profile-guided optimization，PGO）是一种编译优化技术，通过利用程序的运行时信息指导编译器进行更好的分支选择、函数内联、循环展开等优化，以获取更好的性能。
- Gcov是GCC的覆盖率测试工具，它使用与PGO相同格式的文件记录程序运行时信息。Linux kernel已经支持使用Gcov收集覆盖率信息，因此可以使用该信息反馈式编译优化内核。
- 本实验的目标是对Linux kernel构建进行PGO优化，实现在特定内核上运行Redis的性能提升。主要目标包括两点：

1. 基于Compass CI的构建和benchmark能力，打造gcc反馈式编译优化流程，构建出优化后的linux kernel RPM包。
2. 实现优化后的内核运行Redis的性能提升5%，挑战10%。

环境限定：
1. 操作系统版本：openEuler 20.09
2. 编译器版本：鲲鹏GCC 9.3.0
3. 测试平台：Compass CI

openEuler 是华为主导，社区开源的一个Linux的发行版，所有开发者、合作伙伴、开源爱好者共同参与，围绕客户的场景进行创新，有更多新的想法产生，创建多样性计算场景最佳操作系统。在通讯，金融、安全等多个领域有着广泛的应用。

Compass-CI 是一个可持续集成的测试平台。为开发者提供针对上游开源软件（来自 Github, Gitee, Gitlab 等托管平台）的测试服务、登录服务、故障辅助定界服务和基于历史数据的分析服务。(https://compass-ci.openeuler.org/)

### 所属赛道

2025全国大学生操作系统比赛的“OS功能设计”赛道


### 参赛要求

- 以小组为单位参赛，最多三人一个小组，且小组成员是来自同一所高校的本科生
- 如学生参加了多个项目，参赛学生选择一个自己参加的项目参与评奖
- 请遵循“2025全国大学生操作系统比赛”的章程和技术方案要求


### 项目导师

马明泽 吴峰光

* gitee [Fengguang](https://gitee.com/wu_fengguang)
* email mamingze2@huawei.com 
* email wufengguang@huawei.com 

### 难度

中等

### 特征

- 对Linux kernel和编译原理有一定了解
- 熟悉C, ruby语言

### 文档

[1] Yuan P, Guo Y, Chen X. Experiences in profile-guided operating system kernel optimization[C]//Proceedings of 5th Asia-Pacific Workshop on Systems. 2014: 1-6.

[2] https://github.com/facebookincubator/BOLT

[3] https://github.com/google/autofdo

### License

[木兰宽松许可证, 第2版](http://license.coscl.org.cn/MulanPSL2)  


## 预期目标

### 注意：下面的内容是建议内容，不要求必须全部完成。选择本项目的同学也可与导师联系，提出自己的新想法，如导师认可，可加入预期目标

### 第一题：在Compass CI上实现反馈式编译优化openEuler内核RPM

1. 预期目标是打通PGO kernel的流程，在openEuler内核上实现该优化。
2. 设计应该足够通用，方便推广到其它软件包的优化构建。

### 第二题：针对Redis应用，进行反馈编译优化内核，从而提升Redis的运行效率。

包括：
1. 使用第一步的方法，完成针对Redis应用优化的内核构建。
2. 分析Redis应用的程序热点，构建不同的workload，尽可能提升优化效果。
3. 设计应该足够通用，方便推广到包含更多benchmark的性能优化。
