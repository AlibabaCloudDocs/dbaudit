# ClearInstanceStorage

调用ClearInstanceStorage清空指定实例存储。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Yundun-dbaudit&api=ClearInstanceStorage&type=RPC&version=2019-12-09)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|ClearInstanceStorage|要执行的操作。

取值：ClearInstanceStorage。 |
|InstanceId|String|是|dbaudit-cn-78v1gcxxxxx|审计的实例ID。 |
|StorageCategory|String|是|dbaudit-audit-dbaudit-cn-78v1gcxxxxx|存储类别（原始日志）。 |
|StorageSpace|String|是|dbaudit-cn-78v1gcxxxxx|存储空间。 |
|RegionId|String|否|cn-hangzhou|地域ID。 |

调用API时，除了本文中该API的请求参数，还需加入阿里云API公共请求参数。公共请求参数的详细介绍，请参见[公共参数](~~148151~~)。

调用API的请求格式，请参见本文示例中的请求示例。

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|InstanceId|String|dbaudit-cn-78v1gcxxxxx|实例ID。 |
|RequestId|String|482EF142-BFA5-43FF-B4B0-84A4B0763639|请求ID。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=ClearInstanceStorage
&InstanceId=dbaudit-cn-78v1gcxxxxx
&StorageCategory=dbaudit-audit-dbaudit-cn-78v1gcxxxxx
&StorageSpace=dbaudit-cn-78v1gcxxxxx
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<RequestId>482EF142-BFA5-43FF-B4B0-84A4B0763639</RequestId>
<InstanceId>dbaudit-cn-78v1gcxxxxx</InstanceId>
```

`JSON` 格式

```
{
    "RequestId":"482EF142-BFA5-43FF-B4B0-84A4B0763639",
    "InstanceId":"dbaudit-cn-78v1gcxxxxx"
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Yundun-dbaudit)查看更多错误码。

