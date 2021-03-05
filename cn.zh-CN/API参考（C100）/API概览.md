# API概览

数据库审计提供以下API。

## 开通数据库审计实例

|API|描述|
|---|--|
|[CreateInstance](/cn.zh-CN/API参考（C100）/开通数据库审计实例/CreateInstance.md)|调用CreateInstance创建一个实例，并自动支付。|
|[QueryAvailableInstances](/cn.zh-CN/API参考（C100）/开通数据库审计实例/QueryAvailableInstances.md)|调用QueryAvailableInstances查询用户的实例列表。|
|[ModifyInstance](/cn.zh-CN/API参考（C100）/开通数据库审计实例/ModifyInstance.md)|调用ModifyInstance对实例资源配置进行变更，并自动支付。|
|[RenewInstance](/cn.zh-CN/API参考（C100）/开通数据库审计实例/RenewInstance.md)|调用RenewInstance对实例进行续费。|
|[SetRenewal]()|调用SetRenewal为一个实例设置自动续费服务。|

## 标签

|API|描述|
|---|--|
|[ListTagKeys](/cn.zh-CN/API参考（C100）/标签/ListTagKeys.md)

|调用ListTagKeys查询某个资源下已经绑定的标签列表。|
|[UntagResources](/cn.zh-CN/API参考（C100）/标签/UntagResources.md)

|调用UntagResources为指定的实例资源统一解绑并删除标签。|
|[TagResources](/cn.zh-CN/API参考（C100）/标签/TagResources.md)

|调用TagResources为指定的实例资源列表统一创建并绑定标签。|
|[ListTagResources](/cn.zh-CN/API参考（C100）/标签/ListTagResources.md)

|调用ListTagResources查询一个或多个实例已经绑定的标签列表。|

## 实例

|API|描述|
|---|--|
|[ConfigInstanceWhiteList](/cn.zh-CN/API参考（C100）/实例/ConfigInstanceWhiteList.md)|调用ConfigInstanceWhiteList配置公网IP地址白名单。实例开启公网访问后，可以指定公网IP地址配置白名单，允许公网流量访问审计实例。|
|[StartInstance](/cn.zh-CN/API参考（C100）/实例/StartInstance.md)|调用StartInstance启动审计实例。|
|[DescribeInstanceAttribute](/cn.zh-CN/API参考（C100）/实例/DescribeInstanceAttribute.md)|调用DescribeInstanceAttribute查询实例所有的属性信息，例如：实例ID、实例的备注信息。|
|[DescribeInstances](/cn.zh-CN/API参考（C100）/实例/DescribeInstances.md)|调用DescribeInstances查询实例的列表信息。|
|[EnableInstancePublicAccess](/cn.zh-CN/API参考（C100）/实例/EnableInstancePublicAccess.md)|调用EnableInstancePublicAccess开启指定实例公网访问能力。|
|[DisableInstancePublicAccess](/cn.zh-CN/API参考（C100）/实例/DisableInstancePublicAccess.md)|调用DisableInstancePublicAccess关闭实例的公网访问能力。|
|[ModifyInstanceAttribute](/cn.zh-CN/API参考（C100）/实例/ModifyInstanceAttribute.md)|调用ModifyInstanceAttribute修改指定实例的备注信息。|
|[MoveResourceGroup](/cn.zh-CN/API参考（C100）/实例/MoveResourceGroup.md)|调用MoveResourceGroup移动资源组实例至其他组。|

## 地域

|API|描述|
|---|--|
|[DescribeRegions](/cn.zh-CN/API参考（C100）/地域/DescribeRegions.md)|调用DescribeRegions查询数据库审计实例支持的阿里云地域。|

## 存储

|API|描述|
|---|--|
|[DescribeInstanceStorage](/cn.zh-CN/API参考（C100）/存储/DescribeInstanceStorage.md)|调用DescribeInstanceStorage查询实例存储信息。|
|[ModifyInstanceStorage](/cn.zh-CN/API参考（C100）/存储/ModifyInstanceStorage.md)|调用ModifyInstanceStorage修改指定实例的存储信息。|
|[ClearInstanceStorage](/cn.zh-CN/API参考（C100）/存储/ClearInstanceStorage.md)|调用ClearInstanceStorage清空指定实例存储数据。|

