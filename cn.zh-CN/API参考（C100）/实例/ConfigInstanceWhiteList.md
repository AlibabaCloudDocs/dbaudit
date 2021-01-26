# ConfigInstanceWhiteList

调用ConfigInstanceWhiteList配置公网IP地址白名单。数据库审计实例默认拒绝所有公网审计流量，实例开启公网访问后，需要将指定公网IP地址配置到白名单中，允许来自公网IP的审计流量访问数据库审计实例。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Yundun-dbaudit&api=ConfigInstanceWhiteList&type=RPC&version=2019-12-09)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|ConfigInstanceWhiteList|要执行的操作。

 取值：ConfigInstanceWhiteList。 |
|InstanceId|String|是|dbaudit-cn-78v1gc\*\*\*\*|审计的实例ID。

 可以通过调用[DescribeInstances](~~162343~~)接口获取的审计实例列表获取实例ID。 |
|WhiteList.N|RepeatList|否|10.168.XX.XX/32|实例配置的白名单IP。

 N代表白名单的序号，N的取值范围：1~30。 |
|RegionId|String|否|cn-hangzhou|数据库审计实例的地域ID。

 可以通过调用[DescribeRegions](~~162344~~)接口获取地域ID。 |

调用API时，除了本文中该API的请求参数，还需加入阿里云API公共请求参数。公共请求参数的详细介绍，请参见[公共参数](~~148151~~)。

调用API的请求格式，请参见本文示例中的请求示例。

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|InstanceId|String|dbaudit-cn-78v1gc\*\*\*\*|本次请求的实例ID。 |
|RequestId|String|1B217656-2267-4FBF-B26C-CDD201BDC3B8|本次请求的ID。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=ConfigInstanceWhiteList
&InstanceId=dbaudit-cn-78v1gc****
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<ConfigInstanceWhiteList>
  <RequestId>1B217656-2267-4FBF-B26C-CDD201BDC3B8</RequestId>
  <InstanceId>dbaudit-cn-78v1gc****</InstanceId>
</ConfigInstanceWhiteList>
```

`JSON`格式

```
{
	"RequestId":"1B217656-2267-4FBF-B26C-CDD201BDC3B8",
	"InstanceId":"dbaudit-cn-78v1gc****"
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Yundun-dbaudit)查看更多错误码。

