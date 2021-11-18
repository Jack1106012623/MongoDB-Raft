# Fuzzing
[Fuzzing: Mutation vs. generation](https://resources.infosecinstitute.com/topic/fuzzing-mutation-vs-generation/)

Fuzz Test:利用随机生成的数据作为应用程序的输入，来检测bug的技术
* Mutual：dumb fuzzer，完全随机地生成输入，或者从现有输入中进行随机操作如比特反转(zzuf)生成输入
* Generation：smart fuzzer，将应用的输入规范定义成各种模型，再由模型来随机生成输入
* vs. Mutual更简单，但只能寻找简单的bug，Generation更强但需要对应用进行规范比较耗时

