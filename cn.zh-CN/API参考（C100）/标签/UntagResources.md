# UntagResources

调用UntagResources为指定的实例资源统一解绑并删除标签。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Yundun-dbaudit&api=UntagResources&type=RPC&version=2019-12-09)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|UntagResources|要执行的操作。

 取值：UntagResources。 |
|RegionId|String|是|cn-hangzhou|数据库审计实例的地域ID。

 可以通过调用[DescribeRegions](~~162344~~)接口获取地域ID。 |
|ResourceId.N|RepeatList|是|dbaudit-cn-test|审计的实例ID。

 N表示实例ID的序号，取值范围：1~20。

 可以通过调用[DescribeInstances](~~162343~~)接口获取的审计实例列表获取实例ID。 |
|ResourceType|String|是|INSTANCE|资源类型定义。

 唯一取值：INSTANCE，审计实例。 |
|TagKey.N|RepeatList|否|456|实例的标签键。

 N表示标签键的序号，取值范围：1~20。 |
|All|Boolean|否|false|实例上全部的标签。

 -   当请求中设置了TagKey.N时，All的取值为**false**，表述删除某个标签。
-   当请求中未设置TagKey.N时，All的取值为**true**，表示删除该实例上所有的标签。 |

调用API时，除了本文中该API的请求参数，还需加入阿里云API公共请求参数。公共请求参数的详细介绍，请参见[公共参数](~~148151~~)。

调用API的请求格式，请参见本文示例中的请求示例。

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|8EC13467-A84C-401F-A4A0-AF893066FBA1|本次请求的ID。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=UntagResources
&RegionId=cn-hangzhou
&ResourceId.1=dbaudit-cn-test
&ResourceType=INSTANCE
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<UntagResources>
  <RequestId>8EC13467-A84C-401F-A4A0-AF893066FBA1</RequestId>
</UntagResources>
```

`JSON`格式

```
{
	"RequestId":"8EC13467-A84C-401F-A4A0-AF893066FBA1"
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Yundun-dbaudit)查看更多错误码。

