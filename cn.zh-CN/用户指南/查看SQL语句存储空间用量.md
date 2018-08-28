# 查看SQL语句存储空间用量 {#concept_lxm_qz2_xdb .concept}

不同版本数据库审计服务提供的SQL语句存储空间不同，如果您发现您的SQL语句存储空间可用量不足，您需要升级数据库审计实例版本。

## 判断SQL语句存储空间是否够用 {#section_om4_t3l_xdb .section}

[登录云数据库审计控制台](cn.zh-CN/用户指南/登录数据库审计系统.md#)，在首页即可看到已审计的语句量 。

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12778/15354547693695_zh-CN.png)

**说明：** 如果要查看精确的磁盘容量，您可以使用系统管理员账号，登录云数据库审计系统进行查看。

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12778/15354547693696_zh-CN.png)

下表显示了不同版本产品可用的存储量，您可以参照比对当前存储空间是否够用：

|版本|可存储的SQL条数|
|专业版|30亿|
|高级版|30亿|
|企业版|350亿|

当您发现数据中心分区或数据备份分区的已使用量接近80%，则说明日志存储空间已满，需要升级数据库审计实例版本扩容存储空间。

