# FOFA ICO 资产关联搜索工具

## 简介
FOFA ICO 搜索工具 (支持语法搜索、ICON_Hash 搜索 和 一键导出) 本工具分别有windows 和 mac os 两个版本

**注意事项:本工具仅使用于高级会员，普通会员只能查询100条，高级会员能查询1W条(如果有什么更好的想法欢迎来向我们提出，我们将会一直更新做下去 ^ ~ ^)**

***温馨提示: Windows 版本GUI tk写的虽丑但麻雀虽小五脏俱全 Q A Q！！***

### 语法搜索(摘自FOFA官网:https://fofa.so/ --> 查询语法 处)


| 例句                                      | 用途说明                                           | 注                                                    |
| ----------------------------------------- | -------------------------------------------------- | ----------------------------------------------------- |
| title="beijing"                           | 从标题中搜索“北京”                                 | \-                                                    |
| header="elastic"                          | 从http头中搜索“elastic”                            | -                                                     |
| body="网络空间测绘"                       | 从html正文中搜索“网络空间测绘”                     | -                                                     |
| domain="qq.com"                           | 搜索根域名带有qq.com的网站。                       | -                                                     |
| icp="京ICP证030173号"                     | 查找备案号为“京ICP证030173号”的网站                | 搜索网站类型资产                                      |
| js_name="js/jquery.js"                    | 查找网站正文中包含js/jquery.js的资产               | 搜索网站类型资产                                      |
| js_md5="82ac3f14327a8b7ba49baa208d4eaa15" | 查找js源码与之匹配的资产                           | -                                                     |
| icon_hash="-247388890"                    | 搜索使用此icon的资产。                             | 仅限FOFA高级会员使用                                  |
| host=".gov.cn"                            | 从url中搜索”.gov.cn”                               | 搜索要用host作为名称                                  |
| port="6379"                               | 查找对应“6379”端口的资产                           | -                                                     |
| ip="1.1.1.1"                              | 从ip中搜索包含“1.1.1.1”的网站                      | 搜索要用ip作为名称                                    |
| ip="220.181.111.1/24"                     | 查询IP为“220.181.111.1”的C网段资产                 | -                                                     |
| status_code="402"                         | 查询服务器状态为“402”的资产                        | -                                                     |
| protocol="quic"                           | 查询quic协议资产                                   | 搜索指定协议类型(在开启端口扫描的情况下有效)          |
| country="CN"                              | 搜索指定国家(编码)的资产。                         | -                                                     |
| region="Xinjiang"                         | 搜索指定行政区的资产。                             | -                                                     |
| city="Ürümqi"                             | 搜索指定城市的资产。                               | -                                                     |
| cert="baidu"                              | 搜索证书(https或者imaps等)中带有baidu的资产。      | -                                                     |
| cert.subject="Oracle Corporation"         | 搜索证书持有者是Oracle Corporation的资产           | -                                                     |
| cert.issuer="DigiCert"                    | 搜索证书颁发者为DigiCert Inc的资产                 | -                                                     |
| cert.is_valid=true                        | 验证证书是否有效，true有效，false无效              | 仅限FOFA高级会员使用                                  |
| banner=users && protocol=ftp              | 搜索FTP协议中带有users文本的资产。                 | -                                                     |
| type=service                              | 搜索所有协议资产，支持subdomain和service两种       | 搜索所有协议资产                                      |
| os="centos"                               | 搜索CentOS资产。                                   | -                                                     |
| server=="Microsoft-IIS/10"                | 搜索IIS 10服务器。                                 | -                                                     |
| app="Microsoft-Exchange"                  | 搜索Microsoft-Exchange设备                         | -                                                     |
| after="2017" && before="2017-10-01"       | 时间范围段搜索                                     | -                                                     |
| asn="19551"                               | 搜索指定asn的资产。                                | -                                                     |
| org="Amazon.com, Inc."                    | 搜索指定org(组织)的资产。                          | -                                                     |
| base_protocol="udp"                       | 搜索指定udp协议的资产。                            | -                                                     |
| is_fraud=false                            | 排除仿冒/欺诈数据                                  | -                                                     |
| is_honeypot=false                         | 排除蜜罐数据                                       | 仅限FOFA高级会员使用                                  |
| is_ipv6=true                              | 搜索ipv6的资产                                     | 搜索ipv6的资产,只接受true和false。                    |
| is_domain=true                            | 搜索域名的资产                                     | 搜索域名的资产,只接受true和false。                    |
| port_size="6"                             | 查询开放端口数量等于"6"的资产                      | 仅限FOFA会员使用                                      |
| port_size_gt="6"                          | 查询开放端口数量大于"6"的资产                      | 仅限FOFA会员使用                                      |
| port_size_lt="12"                         | 查询开放端口数量小于"12"的资产                     | 仅限FOFA会员使用                                      |
| ip_ports="80,161"                         | 搜索同时开放80和161端口的ip                        | 搜索同时开放80和161端口的ip资产(以ip为单位的资产数据) |
| ip_country="CN"                           | 搜索中国的ip资产(以ip为单位的资产数据)。           | 搜索中国的ip资产                                      |
| ip_region="Zhejiang"                      | 搜索指定行政区的ip资产(以ip为单位的资产数据)。     | 搜索指定行政区的资产                                  |
| ip_city="Hangzhou"                        | 搜索指定城市的ip资产(以ip为单位的资产数据)。       | 搜索指定城市的资产                                    |
| ip_after="2021-03-18"                     | 搜索2021-03-18以后的ip资产(以ip为单位的资产数据)。 | 搜索2021-03-18以后的ip资产                            |
| ip_before="2019-09-09"                    | 搜索2019-09-09以前的ip资产(以ip为单位的资产数据)。 | 搜索2019-09-09以前的ip资产                            |



## Mac OS 安装 与 使用
* 下载完成之后在下载目录里会有一个FOFA ICO 搜索工具.dmg这样的文件


![图片 0](https://user-images.githubusercontent.com/49038429/121126208-60b4b700-c85a-11eb-975b-68f34d94c105.png)


* 双击打开，把工具拖动到Applications 图标上


![图片 1](https://user-images.githubusercontent.com/49038429/121126433-b9844f80-c85a-11eb-8ccb-3530242ef1fe.png)


* 然后我们在启动台就能看到我们的工具已经安装好了


![图片 2](https://user-images.githubusercontent.com/49038429/121126519-d882e180-c85a-11eb-9941-6f8eaaf5bbf8.png)


* 单击点开工具，打开后我们可以看到工具的页面是这样的


![图片 3](https://user-images.githubusercontent.com/49038429/121126845-6c54ad80-c85b-11eb-9a72-b48ccbece015.png)


![图片 4](https://user-images.githubusercontent.com/49038429/121126967-9f973c80-c85b-11eb-87c0-bf547f314ac3.png)


##使用：
打开网页版FOFA:https://fofa.so/

![图片 5](https://user-images.githubusercontent.com/49038429/121127317-2815dd00-c85c-11eb-8a62-0ae7f3bea7f6.png)

点击登录，并输入自己的账号和密码
![图片 6](https://user-images.githubusercontent.com/49038429/121127338-319f4500-c85c-11eb-9c5c-cf43d23470ac.png)

登录完成后跳转到该页面
![图片 7](https://user-images.githubusercontent.com/49038429/121127358-39f78000-c85c-11eb-9f36-1210348154f9.png)

打开F12找到NETWORK点击进入并且刷新一下
![图片 8](https://user-images.githubusercontent.com/49038429/121127470-68755b00-c85c-11eb-9e37-40c0fae62c32.png)

我们需要的就是紫色方括号内的那一段值 把他复制下来粘贴到工具中的fofa_token中
![图片 9](https://user-images.githubusercontent.com/49038429/121127594-96f33600-c85c-11eb-9702-8b141f888435.png)

然后呢加上我们想要搜索的搜索语句,例如找gov的站
![图片 10](https://user-images.githubusercontent.com/49038429/121127619-a07c9e00-c85c-11eb-81bf-64a3d4c641fa.png)

点击开始程序就会自动运行，当然如果你想结束了 直接点击停止就可以，工具会保留当前的输出内容，然后再导出就可以了，当再次按开始按钮的时候 这个时候会自动清空列表中的数据，并且爬去新的数据
![图片 11](https://user-images.githubusercontent.com/49038429/121127857-010bdb00-c85d-11eb-8efc-033bbfa53144.png)

当停止后点击导出
![图片 12](https://user-images.githubusercontent.com/49038429/121127908-18e35f00-c85d-11eb-89d2-c4d3aeb6496f.png)

数据就会自动生成到下载目录里
![图片 13](https://user-images.githubusercontent.com/49038429/121127953-28fb3e80-c85d-11eb-80b7-6684b059d4e6.png)

打开xls就可以自己筛选想要的数据
![image](https://user-images.githubusercontent.com/49038429/121128022-4a5c2a80-c85d-11eb-9176-6254fe402689.png)

## ！！！最后再次强调 windows 中的导出是导出到当前目录下 || MAC OS 导出到下载目录下！！！

## ICON 资产关联查询功能使用教程










By:08sec&zero-0sec 阳光宅男 && zero-0sec 凯文大叔
