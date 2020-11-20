# DisableInstancePublicAccess

调用DisableInstancePublicAccess关闭实例的公网访问能力。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Yundun-dbaudit&api=DisableInstancePublicAccess&type=RPC&version=2019-12-09)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DisableInstancePublicAccess|要执行的操作。

 取值：DisableInstancePublicAccess。 |
|InstanceId|String|是|dbaudit-cn-78v1gcxxxxx|实例ID。 |
|RegionId|String|否|cn-hangzhou|地域ID。 |

调用API时，除了本文中该API的请求参数，还需加入阿里云API公共请求参数。公共请求参数的详细介绍，请参见[公共参数](~~148151~~)。

调用API的请求格式，请参见本文示例中的请求示例。

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|InstanceId|String|dbaudit-cn-78v1gcxxxxx|实例ID。 |
|RequestId|String|4A1923F8-FD4F-4F97-B2CF-D0F4D878C26D|请求ID。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DisableInstancePublicAccess
&InstanceId=dbaudit-cn-78v1gcxxxxx
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<RequestId>4A1923F8-FD4F-4F97-B2CF-D0F4D878C26D</RequestId>
<InstanceId>dbaudit-cn-78v1gcxxxxx</InstanceId>
```

`JSON` 格式

```
{
	"RequestId":"4A1923F8-FD4F-4F97-B2CF-D0F4D878C26D",
	"InstanceId":"dbaudit-cn-78v1gcxxxxx"
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Yundun-dbaudit)查看更多错误码。

