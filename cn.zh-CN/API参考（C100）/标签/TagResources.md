# TagResources

调用TagResources为指定的实例资源列表统一创建并绑定标签。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Yundun-dbaudit&api=TagResources&type=RPC&version=2019-12-09)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|TagResources|要执行的操作。

 取值：TagResources。 |
|RegionId|String|是|cn-hangzhou|数据库审计实例的地域ID。

 可以通过调用[DescribeRegions](~162344)接口获取地域ID。 |
|ResourceId.N|RepeatList|是|dbaudit-cn-78v1gc\*\*\*\*|审计的实例ID。

 N表示实例ID的序号，取值范围：1~20。

 可以通过调用[DescribeInstances](~162343)接口获取的审计实例列表获取实例ID。 |
|ResourceType|String|是|INSTANCE|资源类型定义。

 唯一取值：INSTANCE，表示审计实例。 |
|Tag.N.Key|String|否|test|实例的标签键。

 N表示标签键的序号，取值范围：1~20。当传入该值时，不允许为空字符串。最多支持128个字符，

 不能以`aliyun`和`acs:`开头，不能包含`http://`或者`https://`。 |
|Tag.N.Value|String|否|testapi|实例的标签值。

 N表示标签值的序号，取值范围：1~20。当传入该值时，可以为空字符串。最多支持128个字符，

 不能以`aliyun`和`acs:`开头，不能包含`http://`或者`https://`。 |

调用API时，除了本文中该API的请求参数，还需加入阿里云API公共请求参数。公共请求参数的详细介绍，请参见[公共参数](~~148151~~)。

调用API的请求格式，请参见本文示例中的请求示例。

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|23DD5EDB-EAC7-44A5-A68E-798BB085D27F|本次请求的ID。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=TagResources
&RegionId=cn-hangzhou
&ResourceId.1=dbaudit-cn-78v1gc****
&ResourceType=INSTANCE
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<TagResources>
  <RequestId>23DD5EDB-EAC7-44A5-A68E-798BB085D27F</RequestId>
</TagResources>
```

`JSON`格式

```
{
	"RequestId":"23DD5EDB-EAC7-44A5-A68E-798BB085D27F"
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Yundun-dbaudit)查看更多错误码。

