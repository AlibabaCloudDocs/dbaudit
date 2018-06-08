# 扩容SQL语句存储空间 {#concept_lxm_qz2_xdb .concept}

不同版本数据库审计服务提供的SQL语句存储空间不同，如果您判断您的SQL语句存储空间不足，您可以进行扩容。

## 判断SQL语句存储空间是否够用 {#section_om4_t3l_xdb .section}

[登录云数据库审计控制台](cn.zh-CN/用户指南/登录数据库审计系统.md#)，在首页即可看到已审计的语句量 。

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12778/3695_zh-CN.png)

**Note:** 如果要查看精确的磁盘容量，您可以使用系统管理员账号，登录云数据库审计系统进行查看。

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/12778/3696_zh-CN.png)

下表显示了不同版本产品可用的存储量，您可以参照比对当前存储空间是否够用：

|版本|可存储的SQL条数|
|专业版|30亿|
|高级版|30亿|
|企业版|350亿|

如果发现数据中心分区或数据备份分区的已使用量接近80%，则说明日志存储空间已满，需要进行扩容。

## 存储空间的扩容 {#section_z2r_53l_xdb .section}

参照以下步骤对存储空间扩容：

1.  登录[ECS控制台](https://ecs.console.aliyun.com)，将云数据库审计的ECS停止。
2.  通过ECS实例进入本实例磁盘页面， 选择数据盘条目下**更多** \> **磁盘扩容**，填写想要扩容到的磁盘大小。
3.  重新启动云数据库审计ECS，等待审计系统识别扩容的磁盘，完成存储空间的扩容。

    **Note:** 数据盘只能扩大容量，不能缩小容量


