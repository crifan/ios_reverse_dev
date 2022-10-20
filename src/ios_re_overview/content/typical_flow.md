# iOS典型逆向开发流程

典型的iOS逆向开发的流程是：

* 先：iPhone越狱
  * 越狱工具
    * unc0ver
    * checkra1n
* 再：逆向破解某iOS的app
  * 对于要研究的某个iOS的app来说，从工作内容角度，主要分：
    * 从AppStore中搜索和安装正版app
    * 去砸壳得到ipa
      * frida-ios-dump
    * 再去研究
      * 静态分析
        * 字符串分析
          * strings
          * nm
          * otool
        * 查看详情
          * MachOView
          * jtool2
          * rabin2
        * 导出头文件
          * class-dump
        * 分析代码逻辑
          * IDA
            * 汇编代码
            * 伪代码
      * 动态调试
        * 命令行方式
          * debugserver + lldb
        * GUI图形界面方式
          * Xcode + MonkeyDev
            * lldb
    * 写hook插件
      * 再去调试和验证
        * 如此反复
  * 最后结果：得到一个插件tweak，实现了你要的目的
    * 比如反越狱检测、改机、hook某个app的某些特定功能（比如微信抢红包）等等
