# iOS逆向的重点和难点

对于iOS逆向开发涉及到众多方面的内容，其中属于重点和难点的是：

* 先搞懂你想要干啥
  * 比如 微信抢红包
* 重点和难点
  * 用静态分析工具和动态调试，共同配合，找出要hook的类
    * 如何用好各种静态分析工具（[MachOView](https://book.crifan.org/books/exec_file_format_macho/website/macho_tool/machoview/)、[rabin2](https://book.crifan.org/books/exec_file_format_macho/website/macho_tool/rabin2/)、[jtoo2](https://book.crifan.org/books/exec_file_format_macho/website/macho_tool/jtool2/)、[otool](https://book.crifan.org/books/exec_file_format_macho/website/macho_tool/otool/)、[IDA](https://book.crifan.org/books/reverse_tool_ida/website/)、[Hopper](https://book.crifan.org/books/ios_re_tool_hopper/website/)等），如何进行动态调试（[Xcode](https://book.crifan.org/books/xcode_dev_debug_summary/website/)+[MonkeyDev](https://book.crifan.org/books/ios_re_monkeydev_debug/website/)、[debugserver](https://book.crifan.org/books/ios_re_dynamic_debug/website/debug_code/lldb_debugserver.html)+[lldb](https://book.crifan.org/books/popular_debugger_lldb/website/)、[frida](https://book.crifan.org/books/reverse_debug_frida/website/)、[Cycript](https://book.crifan.org/books/ios_re_dynamic_debug/website/debug_ui/cycript/)、[Reveal](https://book.crifan.org/books/ios_re_dynamic_debug/website/debug_ui/reveal.html)等），以及利用好已有的[class-dump](https://book.crifan.org/books/ios_re_static_analysis/website/analysis_content/export_header/class_dump.html)导出的头文件，从而找到要分析的类和代码运行逻辑等等，才是重点和难点
  * 再去写hook代码，开发出插件，实现对应的功能
