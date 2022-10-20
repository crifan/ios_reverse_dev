# iOS逆向的重点和难点

对于iOS逆向开发涉及到众多方面的内容，其中属于重点和难点的是：

* 先搞懂你想要干啥
  * 比如 微信抢红包
* 重点和难点
  * 用静态分析工具和动态调试，共同配合，找出要hook的类
    * 如何用好各种静态分析工具（`otool`、`MachOView`、`IDA Pro`、`Hopper`等），如何进行动态调试（`Xcode`+`MonkeyDev`、`debugserver`+`lldb`、`frida`、`Cycript`、`Reveal`等），从而找到要分析的类和代码运行逻辑等等，才是重点和难点
  * 再去写hook代码，开发出插件，实现对应的功能
