# DescribeRegions

调用DescribeRegions查询数据库审计实例支持的阿里云地域。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Yundun-dbaudit&api=DescribeRegions&type=RPC&version=2019-12-09)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeRegions|需要执行的操作。

 取值：**DescribeRegions**。 |
|AcceptLanguage|String|否|zh-CN|根据中文、英文和日文筛选返回结果。默认值为**zh-CN**。取值：

 -   **zh-CN**：中文
-   **en-US**：英文
-   **ja**：日文 |
|RegionId|String|否|cn-hangzhou|区域ID。取值：

 -   **cn-hangzhou**：华东1（杭州）
-   **cn-shanghai**：华东2（上海）
-   **cn-qingdao**：华北1（青岛）
-   **cn-beijing**：华北2（北京）
-   **cn-zhangjiakou**：华北3（张家口）
-   **cn-huhehaote**：华北5（呼和浩特）
-   **cn-shenzhen**：华南1（深圳）
-   **cn-chengdu**：西南1（成都）
-   **cn-hongkong**：中国香港
-   **ap-southeast-1**：新加坡
-   **ap-southeast-2**：澳大利亚（悉尼）
-   **ap-southeast-3**：马来西亚（吉隆坡）
-   **ap-southeast-5**：印度尼西亚（雅加达）
-   **ap-northeast-1**：日本（东京）
-   **ap-south-1**：印度（孟买）
-   **eu-central-1**：德国（法兰克福）
-   **eu-west-1**：英国（伦敦）
-   **us-west-1**：美国（硅谷）
-   **us-east-1**：美国（弗吉尼亚）
-   **me-east-1**：阿联酋（迪拜） |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Regions|Array of Region| |数据库审计实例支持的地域信息。 |
|LocalName|String|华东1（杭州）|地域名称。 |
|RegionEndpoint|String|yundun-dbaudit.aliyuncs.com|地域对应的接入地址。 |
|RegionId|String|cn-hangzhou|地域ID。 |
|RequestId|String|6C277285-7179-4B87-A517-0D61CE4CFD09|阿里云为该请求生成的唯一标识符。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeRegions
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<DescribeRegionsResponse>
      <RequestId>6C277285-7179-4B87-A517-0D61CE4CFD09</RequestId>
      <Regions>
            <RegionId>cn-hangzhou</RegionId>
            <RegionEndpoint>yundun-dbaudit.aliyuncs.com</RegionEndpoint>
            <LocalName>华东1（杭州）</LocalName>
      </Regions>
      <Regions>
            <RegionId>cn-shanghai</RegionId>
            <RegionEndpoint>yundun-dbaudit.aliyuncs.com</RegionEndpoint>
            <LocalName>华东2（上海）</LocalName>
      </Regions>
      <Regions>
            <RegionId>cn-qingdao</RegionId>
            <RegionEndpoint>yundun-dbaudit.aliyuncs.com</RegionEndpoint>
            <LocalName>华北1（青岛）</LocalName>
      </Regions>
      <Regions>
            <RegionId>cn-beijing</RegionId>
            <RegionEndpoint>yundun-dbaudit.aliyuncs.com</RegionEndpoint>
            <LocalName>华北2（北京）</LocalName>
      </Regions>
      <Regions>
            <RegionId>cn-zhangjiakou</RegionId>
            <RegionEndpoint>yundun-dbaudit.aliyuncs.com</RegionEndpoint>
            <LocalName>华北3（张家口）</LocalName>
      </Regions>
      <Regions>
            <RegionId>cn-huhehaote</RegionId>
            <RegionEndpoint>yundun-dbaudit.aliyuncs.com</RegionEndpoint>
            <LocalName>华北5（呼和浩特）</LocalName>
      </Regions>
      <Regions>
            <RegionId>cn-shenzhen</RegionId>
            <RegionEndpoint>yundun-dbaudit.aliyuncs.com</RegionEndpoint>
            <LocalName>华南1（深圳）</LocalName>
      </Regions>
      <Regions>
            <RegionId>cn-chengdu</RegionId>
            <RegionEndpoint>yundun-dbaudit.aliyuncs.com</RegionEndpoint>
            <LocalName>西南1（成都）</LocalName>
      </Regions>
      <Regions>
            <RegionId>cn-hongkong</RegionId>
            <RegionEndpoint>yundun-dbaudit.aliyuncs.com</RegionEndpoint>
            <LocalName>中国香港</LocalName>
      </Regions>
      <Regions>
            <RegionId>ap-southeast-1</RegionId>
            <RegionEndpoint>yundun-dbaudit.aliyuncs.com</RegionEndpoint>
            <LocalName>新加坡</LocalName>
      </Regions>
      <Regions>
            <RegionId>ap-southeast-2</RegionId>
            <RegionEndpoint>yundun-dbaudit.aliyuncs.com</RegionEndpoint>
            <LocalName>澳大利亚（悉尼）</LocalName>
      </Regions>
      <Regions>
            <RegionId>ap-southeast-3</RegionId>
            <RegionEndpoint>yundun-dbaudit.aliyuncs.com</RegionEndpoint>
            <LocalName>马来西亚（吉隆坡）</LocalName>
      </Regions>
      <Regions>
            <RegionId>ap-southeast-5</RegionId>
            <RegionEndpoint>yundun-dbaudit.aliyuncs.com</RegionEndpoint>
            <LocalName>印度尼西亚（雅加达）</LocalName>
      </Regions>
      <Regions>
            <RegionId>ap-northeast-1</RegionId>
            <RegionEndpoint>yundun-dbaudit.aliyuncs.com</RegionEndpoint>
            <LocalName>日本（东京）</LocalName>
      </Regions>
      <Regions>
            <RegionId>ap-south-1</RegionId>
            <RegionEndpoint>yundun-dbaudit.aliyuncs.com</RegionEndpoint>
            <LocalName>印度（孟买）</LocalName>
      </Regions>
      <Regions>
            <RegionId>eu-central-1</RegionId>
            <RegionEndpoint>yundun-dbaudit.aliyuncs.com</RegionEndpoint>
            <LocalName>德国（法兰克福）</LocalName>
      </Regions>
      <Regions>
            <RegionId>eu-west-1</RegionId>
            <RegionEndpoint>yundun-dbaudit.aliyuncs.com</RegionEndpoint>
            <LocalName>英国（伦敦）</LocalName>
      </Regions>
      <Regions>
            <RegionId>us-west-1</RegionId>
            <RegionEndpoint>yundun-dbaudit.aliyuncs.com</RegionEndpoint>
            <LocalName>美国（硅谷）</LocalName>
      </Regions>
      <Regions>
            <RegionId>us-east-1</RegionId>
            <RegionEndpoint>yundun-dbaudit.aliyuncs.com</RegionEndpoint>
            <LocalName>美国（弗吉尼亚）</LocalName>
      </Regions>
      <Regions>
            <RegionId>me-east-1</RegionId>
            <RegionEndpoint>yundun-dbaudit.aliyuncs.com</RegionEndpoint>
            <LocalName>阿联酋（迪拜）</LocalName>
      </Regions>
</DescribeRegionsResponse>
```

`JSON` 格式

```
{
	"RequestId":"6C277285-7179-4B87-A517-0D61CE4CFD09",
	"Regions":[
		{
			"RegionId":"cn-hangzhou",
			"RegionEndpoint":"yundun-dbaudit.aliyuncs.com",
			"LocalName":"华东1（杭州）"
		},
		{
			"RegionId":"cn-shanghai",
			"RegionEndpoint":"yundun-dbaudit.aliyuncs.com",
			"LocalName":"华东2（上海）"
		},
		{
			"RegionId":"cn-qingdao",
			"RegionEndpoint":"yundun-dbaudit.aliyuncs.com",
			"LocalName":"华北1（青岛）"
		},
		{
			"RegionId":"cn-beijing",
			"RegionEndpoint":"yundun-dbaudit.aliyuncs.com",
			"LocalName":"华北2（北京）"
		},
		{
			"RegionId":"cn-zhangjiakou",
			"RegionEndpoint":"yundun-dbaudit.aliyuncs.com",
			"LocalName":"华北3（张家口）"
		},
		{
			"RegionId":"cn-huhehaote",
			"RegionEndpoint":"yundun-dbaudit.aliyuncs.com",
			"LocalName":"华北5（呼和浩特）"
		},
		{
			"RegionId":"cn-shenzhen",
			"RegionEndpoint":"yundun-dbaudit.aliyuncs.com",
			"LocalName":"华南1（深圳）"
		},
		{
			"RegionId":"cn-chengdu",
			"RegionEndpoint":"yundun-dbaudit.aliyuncs.com",
			"LocalName":"西南1（成都）"
		},
		{
			"RegionId":"cn-hongkong",
			"RegionEndpoint":"yundun-dbaudit.aliyuncs.com",
			"LocalName":"中国香港"
		},
		{
			"RegionId":"ap-southeast-1",
			"RegionEndpoint":"yundun-dbaudit.aliyuncs.com",
			"LocalName":"新加坡"
		},
		{
			"RegionId":"ap-southeast-2",
			"RegionEndpoint":"yundun-dbaudit.aliyuncs.com",
			"LocalName":"澳大利亚（悉尼）"
		},
		{
			"RegionId":"ap-southeast-3",
			"RegionEndpoint":"yundun-dbaudit.aliyuncs.com",
			"LocalName":"马来西亚（吉隆坡）"
		},
		{
			"RegionId":"ap-southeast-5",
			"RegionEndpoint":"yundun-dbaudit.aliyuncs.com",
			"LocalName":"印度尼西亚（雅加达）"
		},
		{
			"RegionId":"ap-northeast-1",
			"RegionEndpoint":"yundun-dbaudit.aliyuncs.com",
			"LocalName":"日本（东京）"
		},
		{
			"RegionId":"ap-south-1",
			"RegionEndpoint":"yundun-dbaudit.aliyuncs.com",
			"LocalName":"印度（孟买）"
		},
		{
			"RegionId":"eu-central-1",
			"RegionEndpoint":"yundun-dbaudit.aliyuncs.com",
			"LocalName":"德国（法兰克福）"
		},
		{
			"RegionId":"eu-west-1",
			"RegionEndpoint":"yundun-dbaudit.aliyuncs.com",
			"LocalName":"英国（伦敦）"
		},
		{
			"RegionId":"us-west-1",
			"RegionEndpoint":"yundun-dbaudit.aliyuncs.com",
			"LocalName":"美国（硅谷）"
		},
		{
			"RegionId":"us-east-1",
			"RegionEndpoint":"yundun-dbaudit.aliyuncs.com",
			"LocalName":"美国（弗吉尼亚）"
		},
		{
			"RegionId":"me-east-1",
			"RegionEndpoint":"yundun-dbaudit.aliyuncs.com",
			"LocalName":"阿联酋（迪拜）"
		}
	]
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Yundun-dbaudit)查看更多错误码。

