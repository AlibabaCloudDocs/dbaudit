# ListTagKeys

调用ListTagKeys查询某个资源下已经绑定的标签列表。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Yundun-dbaudit&api=ListTagKeys&type=RPC&version=2019-12-09)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|ListTagKeys|要执行的操作。

 取值：ListTagKeys。 |
|RegionId|String|是|cn-hangzhou|数据库审计实例的地域ID。

 可以通过调用[DescribeRegions](~~162344~~)接口获取地域ID。 |
|ResourceType|String|是|INSTANCE|资源类型定义。

 唯一取值：INSTANCE，表示审计实例。 |
|PageSize|Integer|否|10|分页查询时，显示的每页数据的最大条数。 |
|PageNumber|Integer|否|1|分页查询时，显示当前页的页码。 |

调用API时，除了本文中该API的请求参数，还需加入阿里云API公共请求参数。公共请求参数的详细介绍，请参见[公共参数](~~148151~~)。

调用API的请求格式，请参见本文示例中的请求示例。

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|PageNumber|Integer|10|分页查询时，显示当前页的页码。 |
|PageSize|Integer|1|分页查询时，显示的每页数据的最大条数。 |
|RequestId|String|F0C603E1-A1D8-4F5B-ACD1-F63D86D41B5E|本次请求的ID。 |
|TagKeys|Array of TagKey| |标签列表。 |
|TagCount|Integer|1|标签键的总数量。 |
|TagKey|String|test|标签键。 |
|TotalCount|Integer|2|标签的总数量。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=ListTagKeys
&RegionId=cn-hangzhou
&ResourceType=INSTANCE
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<ListTagKeys>
  <TotalCount>2</TotalCount>
  <PageSize>10</PageSize>
  <RequestId>F0C603E1-A1D8-4F5B-ACD1-F63D86D41B5E</RequestId>
  <PageNumber>1</PageNumber>
  <TagKeys>
        <TagCount>2</TagCount>
        <TagKey>test2</TagKey>
  </TagKeys>
  <TagKeys>
        <TagCount>1</TagCount>
        <TagKey>test</TagKey>
  </TagKeys>
</ListTagKeys>
```

`JSON`格式

```
{
	"TotalCount":2,
	"PageSize":10,
	"RequestId":"F0C603E1-A1D8-4F5B-ACD1-F63D86D41B5E",
	"PageNumber":1,
	"TagKeys":[
		{
			"TagCount":2,
			"TagKey":"test2"
		},
		{
			"TagCount":1,
			"TagKey":"test"
		}
	]
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Yundun-dbaudit)查看更多错误码。

