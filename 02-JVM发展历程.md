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

​	`英雄气短，终被Hotspot虚拟机替换`
