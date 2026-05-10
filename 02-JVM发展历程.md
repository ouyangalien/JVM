## **JVM发展历程**

### Sun Classic VM

- 早在1996年Java1.0版本的时候，Sun公司发布了一款名为Sun Classic VM的Java虚拟机，它同时也是世界上第一款商用Java虚拟机，JDK1.4时完全被淘汰。

- 这款虚拟机内部只提供解释器

- 如果使用JIT编译器，就需要进行外挂。但是一旦使用了JIT编译器，JIT就会接管虚拟机的执行系统。解释器就不再工作。解释器和编译器不能配合工作。

- 现在hotspot内置了此虚拟机



### Exact VM

- 为了解决上一个虚拟机问题，jdk1.2时，sun提供了此虚拟机

- Exact Memory Management：准确式内存管理

  `也可以Non-Conservative/Accurate Memory Management`

  `虚拟机可以知道内存中某个位置的数据具体是什么类型。`

- 具备现代高性能虚拟机的维形

  `热点探测`

  `编译器与解释器混合工作模式`

- 只在Solaris平台短暂使用，其他平台上还是classic vm

  `英雄气短，终被Hotspot虚拟机替换`



### HotSpot VM

- HotSpot历史

  `最初由一家名为Longview Technologies的小公司设计`

  `1997年，此公司被Sun收购：2009年，Sun公司被甲骨文收购`

  ` JDK1.3时，HotSpot VM成为默认虚拟机`

- 日前Hotspot占有绝对的市场地位，称霸武林

  `不管是现在仍在广泛使用的JDK6，还是使用比例较多的JDK8中，默认的虚拟机都是Hotspot`

  `Sun/oracleJDK和OpenJDK的默认虚拟机`

- 从服务器、桌面到移动端、嵌入式都有应用。

- 名称中的HotSpot指的就是它的***热点代码探测技术***。

  通过计数器找到最具编译价值代码，触发即时编译或栈上替换

  通过编译器与解释器协同工作，在最优化的程序响应时间与最佳执行性能中取得平衡



### BEA的JRockit VM

专注于服务器端应用
   它可以不太关注程厅启动速度，因此JRockit内部不包含解析器实现，全部代码都靠即时编译器编译后执行。
大量的行业基准测试显示，JRockitjVM是世界上最快的JVM。
     使用JRockit产品，客户已经体验到了显著的性能提高（一些超过了70%）和硬件成本的减少（达50%）。
优势：全面的Java运行时解决方案组合
    JRockit面向延退敏感型应用的解决方案JRockitRealTime提供以毫秒或微秒级的JVM响应时间，适合财务、军事指挥、电信网络的需要
    Missioncontro1服务套件，它是一组以极低的开销来监控、管理和分析生产环境中的应用程序的工具。
2008年，BEA被oracle收购。
racle表达了整合两大优秀虚拟机的工作，大致在JDK8中完成。整合的方式是在HotSpot的基础上，移植JRockit的优秀特性。
高斯林：日前就职于谷歌，研究人工智能和水下机器人
