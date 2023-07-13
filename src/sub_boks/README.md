# 子教程

上述所有和iOS逆向开发相关的内容，分别整理到多个独立的子教程以及相关内容：

* 系列
  * iOS逆向基本流程
    * iOS逆向之前，先要给iOS设备越狱
      * [iOS逆向开发：iPhone越狱](https://book.crifan.org/books/ios_re_iphone_jailbreak/website/)
      * 如果是`iOS 15+`，则需要最新的越狱工具
        * [iOS逆向：iOS15越狱](https://book.crifan.org/books/ios_re_ios15_jailbreak/website/)
      * 越狱后，常会涉及到
        * [iOS逆向开发：越狱包管理器](https://book.crifan.org/books/ios_re_package_manager/website/)
    * 然后再去砸壳出ipa文件
      * [iOS逆向开发：砸壳ipa](https://book.crifan.org/books/ios_re_crack_shell_ipa/website/)
    * 然后再去静态分析
      * [iOS逆向开发：静态分析](https://book.crifan.org/books/ios_re_static_analysis/website/)
      * 常用静态分析工具
        * [逆向利器：IDA](https://book.crifan.org/books/reverse_tool_ida/website/)
    * 以及动态调试
      * [iOS逆向开发：动态调试](https://book.crifan.org/books/ios_re_dynamic_debug/website/)
        * 工具
          * [iOS逆向开发：MonkeyDev调试](https://book.crifan.org/books/ios_re_monkeydev_debug/website/)
          * [逆向调试利器：Frida](https://book.crifan.org/books/reverse_debug_frida/website/)
          * [主流调试器：LLDB](https://book.crifan.org/books/popular_debugger_lldb/website/)
          * Xcode
            * [XCode开发心得](https://book.crifan.org/books/xcode_dev_summary/website/)         
              * [Xcode开发：调试心得](http://book.crifan.org/books/xcode_dev_debug_summary/website/)
  * iOS逆向常涉及领域/子项目
    * 如何用`Theos`/`iOSOpenDev`/`MonkeyDev`开发越狱插件，实现特定功能
      * [iOS逆向开发：越狱插件开发](https://book.crifan.org/books/ios_re_jailbreak_tweak/website/)
        * [iOS逆向开发：iOSOpenDev开发插件](https://book.crifan.org/books/ios_re_iosopendev_tweak/website/)
    * 正向的越狱检测和逆向的反越狱检测
      * [iOS逆向开发：越狱检测和反越狱检测](https://book.crifan.org/books/ios_re_jb_detection/website/)
    * iOS底层机制和原理
      * [iOS逆向开发：iOS底层机制](https://book.crifan.org/books/ios_re_ios_internal/website/)
        * [iOS逆向开发：ObjC运行时](https://book.crifan.org/books/ios_re_objc_runtime/website/)
        * [iOS逆向开发：Block匿名函数](https://book.crifan.org/books/ios_re_objc_block/website/)
    * 通用的
      * [iOS逆向之动态调试：断点](https://book.crifan.org/books/ios_re_debug_breakpoint/website/)
    * 高级逆向
      * 代码模拟
        * [CPU模拟利器：Unicorn](https://book.crifan.org/books/cpu_emulator_unicorn/website/)
  * iOS逆向具体实例
    * [iOS逆向开发：YouTube逆向](https://book.crifan.org/books/ios_re_youtube_reverse/website/)
      * [iOS逆向YouTube：protobuf逆向](https://book.crifan.org/books/ios_re_protobuf_reverse/website/)
    * 【整理Book】iOS逆向开发：抖音逆向
* 相关
  * 语言
    * 汇编
      * 通用
        * 【整理Book】底层编程语言：汇编语言asm
      * ARM
        * [最流行汇编语言：ARM crifan.org](https://book.crifan.org/books/popular_assembly_arm/website/)
    * C
      * [C语言开发心得](https://book.crifan.org/books/c_lang_dev_summary/website/)
    * iOS
      * [iOS开发心得](https://book.crifan.org/books/ios_dev_summary/website/)
  * 代码
    * iOS正向
      * 越狱检测
        * [crifan/iOSJailbreakDetection: iOS的ObjC的app，实现iOS越狱检测](https://github.com/crifan/iOSJailbreakDetection)
      * 配合测试(iOS逆向改机)的app
        * [crifan/ShowSystemInfo: iOS的app，检测并显示iOS的iPhone的系统信息](https://github.com/crifan/ShowSystemInfo)
    * iOS逆向
      * 反越狱检测
        * [crifan/iOSBypassJailbreak: 越狱iOS的hook插件，实现反越狱检测](https://github.com/crifan/iOSBypassJailbreak)
      * 逆向YouTube
        * [crifan/iOSYouTubeAdsFilter: MonkeyDev+Xcode项目，iOS逆向YouTube，尝试实现广告过滤功能](https://github.com/crifan/iOSYouTubeAdsFilter)
