构建一个多平等节点的系统，针对每个node信息，生成一个goroutine，每个goroutine通过无限循环执行，定时的ping 和 pong，并通过回调或者channel实现将node down或者node up事件通知调用方

接口如下
1. AddNodes/AddNode 
2. RemoveNode
3. GetKnownNodes
4. GetLinkedNodes
5. 定时器时间设置


微服务有多个实例时，先通过 Etcd 选举一个 Master 实例，然后 Master 实例为所有实例较均匀的分配任务，并将任务分配结果 Set 到 Etcd，最后 Master 和 Node 实例 Watch 到任务列表，并过滤出自身需要处理的任务列表
