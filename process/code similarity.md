通过二进制代码相似度做漏洞检测

数据集来源：2022 USENIX How Machine Learning Is Solving the Binary Function Similarity Problem；
由七个流行的开源项目组成：ClamAV、Curl、Nmap、OpenSSL、Unrar、Z3和Zlib

2022 ISSTA jTrans Jump-Aware Transformer for Binary Code Similarity；
优势：
局限性：

2022 Cryptography and Security UniASM Binary Code Similarity Detection without Fine-tuning；
考虑了二进制代码中跳转指令（jump instructions）对控制流图（CFG）和语义信息的影响，并设计了一种跳转感知（jump-aware）的Transformer模型，它可以显式地捕捉CFG中的跳转信息，并增强Transformer对二进制代码结构和语义的理解。此外，jTrans还使用了一种自适应注意力机制，它可以动态地调整不同类型指令之间的注意力权重，并提高模型对重要指令的关注度。
优势：可以有效处理跳转信息；
局限性：依赖于输入的控制流图的完整性







