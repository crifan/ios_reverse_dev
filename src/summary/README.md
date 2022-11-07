# iOS逆向心得

TODO：

* 【整理】iOS逆向心得：不同app的逆向破解出的难度不同
* 【整理】iOS逆向破解越狱开发：相关工具

---

## iOS安全对应的逆向破解对策

针对[iOS安全]((https://book.crifan.org/books/ios_security_protect/website/)的防护手段，目前能想到的，iOS逆向破解的办法：

* iOS的代码混淆
  * 被反编译后，也只能看到 乱码的函数
    * 部分防止被破解，被猜测到核心逻辑
* iOS的加壳？
  * 没法加壳
    * 但是也可以去研究看看，是否有机会
* iOS代码运行期间，动态下载要运行的核心代码（二进制格式？）
  * 增加核心逻辑的安全性
    * 好像涉及到虚拟机之类的
      * 注：对应的iOS逆向，则是：unicorn等 模拟器 虚拟机，模拟运行对应的指令
* iOS的抓包方面的：加https证书验证？ ssl pinning？
  * 甚至（参考抖音的做法）去本地ssl证书验证
    * 只有破解hook后，才能Charles抓包看到https明文
    * 后记：[[原创]绕过抖音SSL Pinning-iOS安全-看雪论坛-安全社区|安全招聘|bbs.pediy.com](https://bbs.pediy.com/thread-270700.htm)
      * > 1.加入自己的证书2.干掉所有的证书3.不让他验证证书。很显然，你用的是第二种

## 抓包方面

### 可以自己搭建服务器抓包

举例，别人的：

抓包的时候可以自己搭建服务器，用于嗅探记录，拦截请求数据包，或者叫转发数据号，记录当前传入和传出的参数，也就是请求和响应的各种参数记录下来，类似于这种效果：

```bash
--- 机器参数.
-- @table rfaker
-- @string name 设备名称 e.g. "“xxx”的 iPhone"
-- @string hw_machine_name e.g. "iPhone 11 Pro Max"
-- @string ssid e.g. "TP_LINK_E-BoJingEr-557-OFFICE"
-- @tparam integer create_time e.g.  创建时间 1654709286
-- @string locale_identifier e.g. "CN"
-- @string remark 备注 e.g. null
-- @number lon e.g. 123.98118244667
-- @string app_times e.g. null
-- @string network_state e.g. "WIFI"
-- @string localtion e.g. null
-- @string idfa e.g. "91566BBD-C5E6-48B0-85CA-6E0C68663F69"
-- @string hw_machine e.g. "iPhone12,5"
-- @string carrier_name e.g. "数码通"
-- @string build_version e.g. "18G82"
-- @string system_version e.g. "14.7.1"
-- @number lat e.g. 33.814002430383
-- @string current_radioaccess_technology e.g. "CTRadioAccessTechnologyLTE"
-- @string mobile_network_code e.g. "06"


--- 当前参数.
-- @function faker
-- @apiget http://127.0.0.1:1688/api/v1/machine/faker
-- @treturn rfaker 返回当前工作参数
-- @usage
-- -- 返回结果如:(json)
-- {
--     "name":"“xxx”的 iPhone",
--     "hw_machine_name":"iPhone 11 Pro Max",
--     "ssid":"TP_LINK_E-BoJingEr-557-OFFICE",
--     "create_time":1654709286,
--     "locale_identifier":"CN",
--     "remark":null,
--     "lon":123.98118244667,
--     "app_times":null,
--     "network_state":"WIFI",
--     "localtion":null,
--     "idfa":"91566BBD-C5E6-48B0-85CA-6E0C68663F69",
--     "hw_machine":"iPhone12,5",
--     "carrier_name":"数码通",
--     "build_version":"18G82",
--     "system_version":"14.7.1",
--     "lat":33.814002430383,
--     "current_radioaccess_technology":"CTRadioAccessTechnologyLTE",
--     "mobile_network_code":"06"
-- }
```
