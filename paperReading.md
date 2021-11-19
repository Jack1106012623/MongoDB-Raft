# Fault-Tolerant Replication with Pull-Based Consensus in MongoDB
NSDI 2021


# MongoDB’s JavaScript Fuzzer
CACM 2017

> Hybrid Fuzzing

方法：从现有测试集中随机选取一组，转换为AST。再从一组seed中随机生成节点来替换AST中节点生成测试。

做法：每次从现有测试集(corpus)中选择150组，每组包括几十个已知的测试文件，每组最终生成一个fuzzed文件作为新的测试。（从每组中的测试文件随机选取一些测试命令生成AST，然后由seed生成突变的节点来替换。）

> Catch Bugs
* Tools for generic errors：语言运行时异常检测工具，内存嗅探等。用来检测代码bug
* Assertions：使用assertion来检测程序逻辑bug。使用时间戳，BFS等方法追踪catch到的异常所在的代码位置。


# Linearizability: A Correctness Condition for Concurrent Objects 

ACM Transactions on Programming Languages and Systems (TOPLAS) 1990

MAURICE P. HERLIHY, JEANNETTE M. WING

非形式化定义：
> 一组并发进程对一组共享对象的访问具有实时序，对象的调用操作像是瞬时发生在invocation和response之间的某刻

形式化定义：
> Sequential: 
* 一个history的第一个事件是invocation；
* 除了最后一个，每个invocation的下一个是匹配的response，每个response的下一个是(匹配的？)invocation。
一个进程的history是sequential。

> complete(H): H的最大子序列，只包含匹配的invocation和response

> $<_H$: $e_0<_H e_1$ if res($e_0$) 先于 inv($e_1$)

> H is Linearizability: 为H扩展一些responses成H'(考虑未response但已经完成的event)
* 如果complete(H')等价于某些sequential history S，且
* $<_H\subseteq <_S$