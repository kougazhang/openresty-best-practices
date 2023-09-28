# 火焰图

让我们回想一下，曾经作为编程新手的我们是如何调优程序的？通常是在没有数据的情况下依靠主观臆断来瞎蒙，稍微有些经验的同学则会对差异代码进行二分或者逐段调试。这种定位问题的方式不仅耗时耗力，而且还不具有通用性，当遇到其他类似的性能问题时，需要重复踩坑、填坑，那么如何避免这种情况呢？

俗语有云：“工欲善其事，必先利其器。”个人认为，程序员定位性能问题也需要一件“利器”。 如同医生给病人看病，需要依靠专业的医学工具（比如 X 光片、听诊器等）进行诊断，最后依据医学工具的检验结果快速精准地定位出病因所在。性能调优工具（比如 perf / gprof 等）之于性能调优就像 X 光之于病人一样，它可以一针见血地指出程序的性能瓶颈。

但是常用的性能调优工具 perf 等，在呈现内容上只能单一地列出调用栈或者非层次化的时间分布，不够直观。这里我推荐大家配合使用火焰图，它将 perf 等工具采集的数据呈现得更为直观。火焰图是定位疑难杂症的神器，比如 CPU 占用高、内存泄漏等问题。特别是 Lua 级别的火焰图，可以定位到函数和代码级别。

下图来自 OpenResty 的 [官网](http://openresty.org/download/user-flamegraph.svg)，显示的是一个正常运行的 OpenResty 应用的火焰图，先不用了解细节，有一个直观的了解。

![Alt text](http://openresty.org/download/user-flamegraph.svg)

里面的颜色是随机选取的，并没有特殊含义。火焰图的数据来源，是通过 [systemtap](https://sourceware.org/systemtap/) 定期收集。