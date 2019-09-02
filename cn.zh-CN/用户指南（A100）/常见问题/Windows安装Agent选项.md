# Windows安装Agent选项 {#concept_fx2_ktl_xdb .concept}

Windows上安装Agent时，需要根据应用与数据库的环境选择不同的安装选项进行安装。

应用与数据库不在同一服务器的情况下，请按照下图，勾选WinPcap选项，选择安装WinPcap，不安装npcap。

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12783/3712_zh-CN.png)

应用与数据库在统一服务器通过本机回环（loopback）进行访问的情况下，选择安装npcap，而不安装WinPcap。请按照下图指示进行安装。

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12783/3713_zh-CN.png)

之后在安装npcap的时候，请按照下图选择**Install Npcap in WinPcap API-compatible Mode**。

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12783/3714_zh-CN.png)

安装完成后，修改C:\\Users\\<用户名\>\\AppData\\Roaming\\rmagent\\rmagent.ini，将其中`#loopback=1`一行中的`#`删除以解除注释，保存文件。最后重启Windows。

