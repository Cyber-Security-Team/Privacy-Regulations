通过二进制代码相似度做漏洞检测

数据集来源：

2022 USENIX How Machine Learning Is Solving the Binary Function Similarity Problem；一篇综述

由七个流行的开源项目组成：ClamAV、Curl、Nmap、OpenSSL、Unrar、Z3和Zlib；这篇论文复现了20年之前的工作，

漏洞库：OpenSSL1.0.2d中选择了十个易受攻击的函数，涵盖了八个CVE


目前在复现代码，tensorflow1.14版本，使用docker环境

要先对数据集进行处理：
1、编译：二进制文件
2、生成IDB：通过IDA工具生成汇编文件
3、生成代码图数据：通过IDA Pro的扩展插件，基于IDB生成Flow图、ACFG汇编代码和ACFG特征
4、数据筛选清洗：
5、生成函数对：根据实验组中的编译优化、指令集等异同，组合生成用于训练的函数对
6、数据集拆分：拆分得到训练、验证、测试集

每个模型的数据预处理都不一样（同一个数据集对不同模型的预处理也不同）

2022 ISSTA jTrans Jump-Aware Transformer for Binary Code Similarity；
以前的方法忽略了忽略了二进制代码中跳转指令的重要性。因此，该论文考虑了二进制代码中跳转指令（jump instructions）对控制流图（CFG）和语义信息的影响，并设计了一种跳转感知（jump-aware）的Transformer模型，它可以显式地捕捉CFG中的跳转信息，并增强Transformer对二进制代码结构和语义的理解。然后，利用bert对模型进行预训练和微调。


