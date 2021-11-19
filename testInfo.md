# MongoDB-Raft Test
1. model checking using TLA+
> [Two attempts to compare a TLA+ spec with a C++ implementation; 2020](https://emptysqua.re/blog/extreme-modelling-in-practice/)
   * 为了验证协议规约与实现的一致性，使用“model-based trace-checking"来检验MongoDB-Raft，失败，并分析了3个原因。
   * 使用“model-based test-case generation”验证 MongoDB Realm Sync，成功，算法覆盖率达到100%
> [visualzhou / mongo-repl-tla](https://github.com/visualzhou/mongo-repl-tla)
   * a simplified part of the MongoDB-Raft in TLA+
> [will62794 / mongo-repl-tla](https://github.com/will62794/mongo-repl-tla)
   * 对 [visualzhou / mongo-repl-tla]进行了扩展，为同步源选举建立了模型
> 成果
   * 发现了一个bug，并能复现出之前发现的几个bug。
2. unit testing
   * C++ old, new 
3. integration testing
   * evergreen 
4. fuzz testing. (CACM2017)
   * 集成在开发系统中，是目前为止发现最多bug的工具。
5. fault-injection testing.
   * Jepsen 