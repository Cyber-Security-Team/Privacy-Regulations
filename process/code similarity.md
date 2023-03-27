通过二进制代码相似度做漏洞检测

数据集来源：2022 USENIX How Machine Learning Is Solving the Binary Function Similarity Problem；
由七个流行的开源项目组成：ClamAV、Curl、Nmap、OpenSSL、Unrar、Z3和Zlib

漏洞库：OpenSSL1.0.2d中选择了十个易受攻击的函数，涵盖了八个CVE

2022 ISSTA jTrans Jump-Aware Transformer for Binary Code Similarity；
UniASM 是一种新的基于 Transformer 的二进制代码嵌入模型，旨在学习用于二进制代码相似性检测 (BCSD) 的二进制函数表示。它使用汇编语言生成（ALG）和相似函数预测（SFP）这两个训练任务来生成具有更均匀空间分布的向量，可以直接用于相似性比较而无需任何微调。UniASM 还提出了一种新的二元函数标记化方法，可以增加标记的语义信息并解决词汇外问题。该模型学习汇编代码的语义并生成可以使用余弦相似性比较相似性的函数嵌入。二进制函数的表示包括指令规范化、汇编标记化和函数序列化。

优势：UniLM是一种统一的语言模型，可以同时处理自然语言和汇编语言，从而提高了二进制代码的表示能力

2022 Cryptography and Security UniASM Binary Code Similarity Detection without Fine-tuning；
考虑了二进制代码中跳转指令（jump instructions）对控制流图（CFG）和语义信息的影响，并设计了一种跳转感知（jump-aware）的Transformer模型，它可以显式地捕捉CFG中的跳转信息，并增强Transformer对二进制代码结构和语义的理解。此外，jTrans还使用了一种自适应注意力机制，它可以动态地调整不同类型指令之间的注意力权重，并提高模型对重要指令的关注度。

优势：可以有效处理跳转信息；
局限性：依赖于输入的控制流图的完整性







