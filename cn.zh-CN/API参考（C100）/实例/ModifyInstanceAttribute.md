# ModifyInstanceAttribute

调用ModifyInstanceAttribute修改指定实例的备注信息，设置后用户可以快速识别实例的用途。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Yundun-dbaudit&api=ModifyInstanceAttribute&type=RPC&version=2019-12-09)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|ModifyInstanceAttribute|要执行的操作。

 取值：ModifyInstanceAttribute。 |
|InstanceId|String|是|dbaudit-cn-78v1gc\*\*\*\*|审计的实例ID。

 可以通过调用[DescribeInstances](~~162343~~)接口获取的审计实例列表获取实例ID。 |
|Description|String|否|新购实例|实例的备注信息。 |
|RegionId|String|否|cn-hangzhou|数据库审计实例的地域ID。

 可以通过调用[DescribeRegions](~~162344~~)接口获取地域ID。 |

调用API时，除了本文中该API的请求参数，还需加入阿里云API公共请求参数。公共请求参数的详细介绍，请参见[公共参数](~~148151~~)。

调用API的请求格式，请参见本文示例中的请求示例。

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|54CFE6B5-A18A-43CD-ACE1-DF263CE0A506|本次请求的ID。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=ModifyInstanceAttribute
&InstanceId=dbaudit-cn-78v1gc****
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<ModifyInstanceAttribute>
  <RequestId>54CFE6B5-A18A-43CD-ACE1-DF263CE0A506</RequestId>
</ModifyInstanceAttribute>
```

`JSON`格式

```
{
	"RequestId":"54CFE6B5-A18A-43CD-ACE1-DF263CE0A506"
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Yundun-dbaudit)查看更多错误码。

