# 开通实例API概览

开通数据库审计实例的OpenAPI是基于阿里云交易和账单管理OpenAPI（BSS OpenAPI）中实例域相关的API实现的。

本章节介绍开通数据库审计实例的相关API。如需查看BSS OpenAPI的详细介绍，请参见[阿里云交易和账单管理API参考]()。

调用开通数据库审计实例的OpenAPI，需要使用如下相关参数：

-   Endpoint：阿里云BSS OpenAPI的服务接入地址为business.aliyuncs.com。
-   **对应Region**：阿里云BSS OpenAPI的服务对应的唯一Region为**cn-hangzhou**。

目前数据库审计调用的BSS OpenAPI涉及如下实例域相关接口：

|API|描述|
|---|--|
|[CreateInstance](/cn.zh-CN/API参考（C100）/开通数据库审计实例/CreateInstance.md)|调用**CreateInstance**创建一个实例，并自动支付。|
|[QueryAvailableInstances](/cn.zh-CN/API参考（C100）/开通数据库审计实例/QueryAvailableInstances.md)|调用**QueryAvailableInstances**查询用户的实例列表。|
|[ModifyInstance](/cn.zh-CN/API参考（C100）/开通数据库审计实例/ModifyInstance.md)|调用**ModifyInstance**对实例资源配置进行变更，并自动支付。|
|[RenewInstance](/cn.zh-CN/API参考（C100）/开通数据库审计实例/RenewInstance.md)|调用**RenewInstance**对实例进行续费。|
|[SetRenewal](/cn.zh-CN/API参考（C100）/开通数据库审计实例/SetRenewal.md)|调用**SetRenewal**为一个实例设置自动续费服务。|

