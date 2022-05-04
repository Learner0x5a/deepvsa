# DEEPVSA

## Code of DEEPVSA
  
- Instruction Embedding based Deep Learning Model for Memory Access Region Predict.
- Deep Learning faciliateddiag VSA and Root Cause Diagnose.


## Data and models of DEEVPSA

See details in <https://psu.box.com/s/9nkz2uf9xv7acces7o5th81wb4uplxq3>

## Paper

Please see our paper and video presentation at [DEEPVSA: Facilitating Value-set Analysis with Deep Learning for Postmortem Program Analysis](https://www.usenix.org/conference/usenixsecurity19/presentation/guo)

## Note by zhuwy

DeepVSA利用Intel PIN记录二进制程序trace，包括指令的地址，访存的地址，/proc/self/maps，指令的字节码等，详见`pintool`目录；

之后写了脚本解析pintool生成的log，详见`pin_parser`目录，解析完丢给神经网络预测；

神经网络的输入是指令字节码，输出是访存区域（栈/堆/全局）
