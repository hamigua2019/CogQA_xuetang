homework8

一. CogQA

CogQA是一个解决互联网大规模问答多跳问题的新框架。与此前相关框架相比，不仅引入了外部知识，运用Bert进行知识抽取，还运用GAN进行问答决策推理，给出了可解释的路径，从而在问题回答的准确性和可解释性都做出了开创性的工作。

什么叫多跳问题呢？就是根据现有文本无法一步得出答案，而需要引入外部知识，并进行知识推理决策的问题。论文

二. 运行结果与论文结果比较

作为作业跑出的结果。

不如论文中给出的结果。原因可能是因为未将参数调整到合适状态。

{'em': 0.20229574611748818, 'f1': 0.28453167784528083, 'prec': 0.2980000643066138, 'recall': 0.29234633104424973, 

'sp_em':0.087643484132343, 'sp_f1': 0.4436039958235459, 'sp_prec': 0.5225427380958236, 'sp_recall': 0.43626571492878335, 

'joint_em': 0.041188386225523295, 'joint_f1': 0.16846707791924628, 'joint_prec': 0.20438624900745073, 'joint_recall': 0.1717743266275058}

论文结果

三. 论文实施过程与细节

本次论文代码复现调试花了很长时间。预计如果在设备和工具知识等所有条件具备的情况下，运用AWS EC2 T80 GPU资源，整个运行时间可能在12小时左右。

但实际运行中，受EC2每次所用的最大12个小时时间限制，调试可能掉线；受Memory of out影响，特别是到调试步骤的中后段，调试可能频繁停止，时间可能加长，调试失败概率大增。解决办法是齐斌助教老师建议运用tmux工具，在实际调试中大大提高保证了调试的稳定性。

除了GPU资源等资源因素，对软件调试工具的熟练运用也是避免调试频繁失败的主要因素。依次是Redis、Rivdia-smi、gpustat、tmux等等。

四. 模型性能的提升与改进

本次因为时间因素，还有水平因素，未来得及对模型进行改进，推测对数据预处理进行改进能带来performance一定程度的提高；在模型结构方面，可能也有改进的空间，但目前暂时未有进一步深入的idea，有待于在继续的学习研究中再改进。

感谢老师的批阅，请多多批评指正，再次感谢：）
