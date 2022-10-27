# iOS典型逆向开发流程

典型的iOS逆向开发的流程是：

* 先：iPhone越狱
  * 越狱工具
    * unc0ver
    * checkra1n
* 再：逆向破解某iOS的app
  * 对于要研究的某个iOS的app来说，从工作内容角度，主要分：
    * 从AppStore中搜索和安装正版app
    * ipa
      * 砸壳得到ipa
        * frida-ios-dump
      * 或者直接从网上搜索某版本的ipa
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
        * 恢复符号表
          * restore-symbol
        * 分析代码逻辑
          * IDA
            * 汇编代码
            * 伪代码
      * 动态调试
        * 调试代码逻辑
          * 命令行方式
            * debugserver + lldb
          * GUI图形界面方式
            * Xcode + MonkeyDev
              * lldb
                * 插件
                  * chisel
          * 其他调试工具
            * frida
        * 分析界面元素
          * Reveal
          * Cycript
    * 再去调试和验证
      * 写hook插件
      * 加断点调试，验证代码是否运行到
      * 如此反复静态分析和动态调试的过程
  * 最后结果：得到一个插件tweak，实现了你要的目的
    * 比如反越狱检测、改机、hook某个app的某些特定功能（比如微信抢红包）等等
