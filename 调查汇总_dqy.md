### 大模型的安全性不足


---
* <strong> 针对r1的安全评估 </strong>
  主要参考:[The Hidden Risks of Large Reasoning Models: A Safety Assessment of R1](https://arxiv.org/abs/2502.12659)

  结论总结：
  > 1. r1与同为推理大模型的o3-mini安全性有明显差距；
  > 2. 蒸馏后的大模型在安全性的表现上会变差；
  > 3. 大模型的推理能力的显著增加也意味着潜在风险的显著增加；
  > 4. 大模型的思考过程(</think/>间)中也可能包含有危害的信息，尽管最终输出可能不会包含相关信息;
  > 除此以外，有数据显示所有推理大模型在[Air-Bench](https://arxiv.org/abs/2407.17436)上的‘Operational
 Misuses’ 和 ‘Sexual Content’都做得很差

  这一系列意味着类似r1这样的模型在恶意的提问与各类安全防护上做得并不完善，有着较大可能被利用的漏洞，更不用说面对特殊特定场景中的安全问题。
  
---
* <strong> 一些大模型面临的安全威胁总结 </strong>
  > 1. Adversarial Attack
  > 2. Jailbreak Attacks:[推荐文章](https://blog.csdn.net/qq_27590277/article/details/140598669),[论文地址](https://arxiv.org/abs/2407.04295)
  > 3. Prompt Injection Attacks:[推荐文章](https://zhuanlan.zhihu.com/p/647162002)
  > 4. Backdoor Attacks
  > 5. Model Extraction Attacks
  > 6. Data Extraction Attacks
  主要关注1到3的部分

---

* <strong> 一些相关工作 </strong>
  注：主要聚焦于llm的越狱攻击防护
  主要参考：[Safety at Scale: A Comprehensive Survey of Large Model Safety](https://arxiv.org/abs/2502.05206)
  > 1. Input Defences 主要是处理输入的prompt来避免产生有害回答；
  > 2. Input Filtering 检测可能是恶意的信息，直接拒绝回答;
  > 3. Ouput Defences 检测输出及时终止，目前看deepseek可能应用了该技术(仅是使用体验，具体需要研究或查阅官方资料)
  > 4. Ensemble Defenses 

相关具体实现与内容有待进一步研究