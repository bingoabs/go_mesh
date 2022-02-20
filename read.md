构建一个多平等节点的系统，针对每个node信息，生成一个goroutine，每个goroutine通过无限循环执行，定时的ping 和 pong，并通过回调或者channel实现将node down或者node up事件通知调用方

接口如下
1. AddNodes/AddNode 
2. RemoveNode
3. GetKnownNodes
4. GetLinkedNodes
5. 定时器时间设置
