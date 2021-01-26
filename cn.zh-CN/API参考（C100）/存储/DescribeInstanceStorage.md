# DescribeInstanceStorage

调用DescribeInstanceStorage查询数据库审计实例的审计日志存储信息，包括存储时长和存储空间大小。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Yundun-dbaudit&api=DescribeInstanceStorage&type=RPC&version=2019-12-09)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeInstanceStorage|要执行的操作。

 取值：DescribeInstanceStorage。 |
|InstanceId|String|是|dbaudit-cn-78v1gc\*\*\*\*|审计的实例ID。

 可以通过调用[DescribeInstances](~~162343~~)接口获取的审计实例列表获取实例ID。 |
|RegionId|String|否|cn-hangzhou|数据库审计的地域ID。

 可以通过调用[DescribeRegions](~~162344~~)接口获取地域ID。 |

调用API时，除了本文中该API的请求参数，还需加入阿里云API公共请求参数。公共请求参数的详细介绍，请参见[公共参数](~~148151~~)。

调用API的请求格式，请参见本文示例中的请求示例。

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|InstanceStorages|Array of InstanceStorage| |实例存储信息。 |
|StorageCapacity|Long|6047313952768|实例的存储容量（单位B）。 |
|StorageCategory|String|dbaudit-audit-dbaudit-cn-78v1gc\*\*\*\*|实例的存储类别（原始日志）。 |
|StorageSpace|String|dbaudit-cn-78v1gc\*\*\*\*|实例的存储空间。 |
|StorageTime|Long|185|需要指定的存储时长（单位：天）。

 修改的存储时间不能超过产品支持的存储时长范围，支持范围为30天~180天。 |
|StorageUsed|Long|0|实例的使用容量（单位B）。 |
|RequestId|String|4226E2BB-EED8-4067-B31B-7F02966765B2|本次请求的ID。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeInstanceStorage
&InstanceId=dbaudit-cn-78v1gcxxxxx
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<DescribeInstanceStorage>
  <InstanceStorages>
        <StorageCapacity>6047313952768</StorageCapacity>
        <StorageSpace>dbaudit-cn-78v1gc****</StorageSpace>
        <StorageCategory>dbaudit-audit-dbaudit-cn-78v1gc****</StorageCategory>
        <StorageTime>185</StorageTime>
        <StorageUsed>0</StorageUsed>
  </InstanceStorages>
  <InstanceStorages>
        <StorageCapacity>6047313952768</StorageCapacity>
        <StorageSpace>dbaudit-cn-78v1gc****</StorageSpace>
        <StorageCategory>dbaudit-rds-dbaudit-cn-78v1gc****</StorageCategory>
        <StorageTime>185</StorageTime>
        <StorageUsed>0</StorageUsed>
  </InstanceStorages>
  <InstanceStorages>
        <StorageCapacity>6047313952768</StorageCapacity>
        <StorageSpace>dbaudit-cn-78v1gc****</StorageSpace>
        <StorageCategory>dbaudit-session-dbaudit-cn-78v1gc****</StorageCategory>
        <StorageTime>185</StorageTime>
        <StorageUsed>0</StorageUsed>
  </InstanceStorages>
  <RequestId>4226E2BB-EED8-4067-B31B-7F02966765B2</RequestId>
</DescribeInstanceStorage>
```

`JSON`格式

```
{
	"InstanceStorages":[
		{
			"StorageCapacity":6047313952768,
			"StorageSpace":"dbaudit-cn-78v1gc****",
			"StorageCategory":"dbaudit-audit-dbaudit-cn-78v1gc****",
			"StorageTime":185,
			"StorageUsed":0
		},
		{
			"StorageCapacity":6047313952768,
			"StorageSpace":"dbaudit-cn-78v1gc****",
			"StorageCategory":"dbaudit-rds-dbaudit-cn-78v1gc****",
			"StorageTime":185,
			"StorageUsed":0
		},
		{
			"StorageCapacity":6047313952768,
			"StorageSpace":"dbaudit-cn-78v1gc****",
			"StorageCategory":"dbaudit-session-dbaudit-cn-78v1gc****",
			"StorageTime":185,
			"StorageUsed":0
		}
	],
	"RequestId":"4226E2BB-EED8-4067-B31B-7F02966765B2"
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Yundun-dbaudit)查看更多错误码。

