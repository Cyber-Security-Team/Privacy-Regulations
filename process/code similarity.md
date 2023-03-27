通过二进制代码相似度做漏洞检测

数据集来源：2022 USENIX How Machine Learning Is Solving the Binary Function Similarity Problem；
由七个流行的开源项目组成：ClamAV、Curl、Nmap、OpenSSL、Unrar、Z3和Zlib

漏洞库：OpenSSL1.0.2d中选择了十个易受攻击的函数，涵盖了八个CVE

2022 ISSTA jTrans Jump-Aware Transformer for Binary Code Similarity；
以前的方法忽略了忽略了二进制代码中跳转指令的重要性。因此，该论文考虑了二进制代码中跳转指令（jump instructions）对控制流图（CFG）和语义信息的影响，并设计了一种跳转感知（jump-aware）的Transformer模型，它可以显式地捕捉CFG中的跳转信息，并增强Transformer对二进制代码结构和语义的理解。然后，利用bert对模型进行预训练和微调。


