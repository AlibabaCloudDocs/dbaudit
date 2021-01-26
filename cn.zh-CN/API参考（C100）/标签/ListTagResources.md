# ListTagResources

调用ListTagResources查询一个或多个实例已经绑定的标签列表。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Yundun-dbaudit&api=ListTagResources&type=RPC&version=2019-12-09)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|ListTagResources|要执行的操作。

 取值：ListTagResources。 |
|RegionId|String|是|cn-hangzhou|数据库审计实例的地域ID。

 可以通过调用[DescribeRegions](~~162344~~)接口获取地域ID。 |
|ResourceType|String|是|INSTANCE|资源类型定义。

 唯一取值： INSTANCE，表示审计实例。 |
|ResourceId.N|RepeatList|否|dbaudit-cn-78v1gc\*\*\*\*|审计的实例ID。

 N表示实例ID的序号，取值范围：1~20。

 可以通过调用[DescribeInstances](~~162343~~)接口获取的审计实例列表获取实例ID。 |
|Tag.N.Key|String|否|test|实例的标签键。

 N表示标签键的序号，取值范围：1~20。 |
|Tag.N.Value|String|否|testapi|实例的标签值。

 N表示标签值的序号，取值范围：1~20。 |
|NextToken|String|否|52EcpzBpR86EEpcc.9xyfvym3cKAXsdV2SSFZnouWTRzf1|使用游标方式对数据进行分页存储的Token值。

 调用接口时可以输入上一次返回结果中**NextToken**的值，如无上一次返回结果中**NextToken**的值、可以为空。 |

调用API时，除了本文中该API的请求参数，还需加入阿里云API公共请求参数。公共请求参数的详细介绍，请参见[公共参数](~~148151~~)。

调用API的请求格式，请参见本文示例中的请求示例。

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|NextToken|String|52EcpzBpR86EEpcc.9xyfvym3cKAXsdV2SSFZnouWTRzf1|使用游标方式对数据进行分页存储的Token值。 |
|RequestId|String|E6A08A8A-F962-4FAD-AF0C-86B393E1F9C1|本次请求的ID。 |
|TagResources|Array of TagResource| |由实例及其标签组成的集合。

 包含了实例ID、资源类型和标签键值等信息。 |
|ResourceId|String|dbaudit-cn-78v1gc\*\*\*\*|本次请求的实例ID。 |
|ResourceType|String|INSTANCE|资源类型。

 唯一取值：INSTANCE，表示审计实例。 |
|TagKey|String|test|实例的标签键。 |
|TagValue|String|testapi|实例的标签值。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=ListTagResources
&RegionId=cn-hangzhou
&ResourceType=INSTANCE
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<ListTagResources>
  <NextToken>52EcpzBpR86EEpcc.9xyfvym3cKAXsdV2SSFZnouWTRzf1</NextToken>
  <RequestId>E6A08A8A-F962-4FAD-AF0C-86B393E1F9C1</RequestId>
  <TagResources>
        <ResourceId>dbaudit-cn-78v1gc****</ResourceId>
        <TagKey>test</TagKey>
        <ResourceType>INSTANCE</ResourceType>
        <TagValue>testapi</TagValue>
  </TagResources>
</ListTagResources>
```

`JSON`格式

```
{
	"NextToken":"52EcpzBpR86EEpcc.9xyfvym3cKAXsdV2SSFZnouWTRzf1",
	"RequestId":"E6A08A8A-F962-4FAD-AF0C-86B393E1F9C1",
	"TagResources":[
 {
 	"ResourceId":"dbaudit-cn-78v1gc****",
 	"TagKey":"test",
 	"ResourceType":"INSTANCE",
 	"TagValue":"testapi"
 }
	]
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Yundun-dbaudit)查看更多错误码。

