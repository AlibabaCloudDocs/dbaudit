# DescribeInstanceAttribute

调用DescribeInstanceAttribute查询实例所有的属性信息，例如：实例ID、实例的备注信息。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Yundun-dbaudit&api=DescribeInstanceAttribute&type=RPC&version=2019-12-09)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeInstanceAttribute|要执行的操作。

 取值：DescribeInstanceAttribute。 |
|InstanceId|String|是|dbaudit-cn-78v1gc\*\*\*\*|审计的实例ID。

 可以通过调用[DescribeInstances](~~162343~~)接口获取的审计实例列表获取实例ID。 |
|RegionId|String|否|cn-hangzhou|数据库审计实例的地域ID。

 可以通过调用[DescribeRegions](~~162344~~)接口获取地域ID。 |

调用API时，除了本文中该API的请求参数，还需加入阿里云API公共请求参数。公共请求参数的详细介绍，请参见[公共参数](~~148151~~)。

调用API的请求格式，请参见本文示例中的请求示例。

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|InstanceAttribute|Struct| |实例属性信息。 |
|Description|String|API|实例的备注信息。 |
|ExpireTime|Long|1578067200000|实例的过期时间。

 单位：毫秒。 |
|InstanceId|String|dbaudit-cn-78v1gc\*\*\*\*|本次请求的实例ID。 |
|InstanceStatus|String|RUNNING|实例状态。取值：

 -   PENDING：未初始化
-   CREATING：创建中
-   RUNNING：运行中
-   EXPIRED：已过期
-   CREATE\_FAILED：创建失败
-   UPGRADING：变配中
-   UPGRADE\_FAILED：变配失败 |
|InternetEndpoint|String|tsiqvqjjlq-public.dbaudit.aliyuncs.com|实例的公网域名。 |
|IntranetEndpoint|String|tsiqvqjjlq.dbaudit.aliyuncs.com|实例的私网域名。 |
|LicenseCode|String|alpha.professional|实例的套餐Code。

 用户购买实例时选择的套餐对应的Code。 |
|PublicNetworkAccess|Boolean|true|是否可以通过公网访问该审计实例。

 -   **true**：可以通过公网访问该审计实例。
-   **false**：不能通过公网访问该审计实例。 |
|RegionId|String|cn-hangzhou|地域ID。 |
|SeriesCode|String|alpha|购买实例时的系列Code。 |
|StartTime|Long|1577437765000|实例的开始时间。

 用时间戳表示，即购买实例的时间。单位：毫秒。 |
|VpcId|String|vpc-bp1c85tzgqu1bf5b\*\*\*\*|实例绑定的VPC ID。 |
|VswitchId|String|vsw-bp1kep1f0k5fnyfs\*\*\*\*|实例绑定的交换机ID。 |
|WhiteList|List|\[10.168.XX.XX/32\]|允许审计流量访问数据库审计实例的公网IP列表。 |
|RequestId|String|28382024-466D-4641-A144-40FD0DD53766|本次请求的ID。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeInstanceAttribute
&InstanceId=dbaudit-cn-78v1gc****
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<DescribeInstanceAttribute>
  <RequestId>28382024-466D-4641-A144-40FD0DD53766</RequestId>
  <InstanceAttribute>
        <LicenseCode>alpha.professional</LicenseCode>
        <Description>API</Description>
        <InstanceId>dbaudit-cn-78v1gc****</InstanceId>
        <WhiteList>10.168.XX.XX/32</WhiteList>
        <StartTime>1577437765000</StartTime>
        <VswitchId>vsw-bp1kep1f0k5fnyfs****</VswitchId>
        <VpcId>vpc-bp1c85tzgqu1bf5b****</VpcId>
        <SeriesCode>alpha</SeriesCode>
        <InstanceStatus>RUNNING</InstanceStatus>
        <PublicNetworkAccess>true</PublicNetworkAccess>
        <InternetEndpoint>tsiqvqjjlq-public.dbaudit.aliyuncs.com</InternetEndpoint>
        <RegionId>cn-hangzhou</RegionId>
        <ExpireTime>1578067200000</ExpireTime>
        <IntranetEndpoint>tsiqvqjjlq.dbaudit.aliyuncs.com</IntranetEndpoint>
  </InstanceAttribute>
</DescribeInstanceAttribute>
```

`JSON`格式

```
{
	"RequestId":"28382024-466D-4641-A144-40FD0DD53766",
	"InstanceAttribute":{
 "LicenseCode":"alpha.professional",
 "Description":"API",
 "InstanceId":"dbaudit-cn-78v1gc****",
 "WhiteList":[
 	"10.168.XX.XX/32"
 ],
 "StartTime":1577437765000,
 "VswitchId":"vsw-bp1kep1f0k5fnyfs****",
 "VpcId":"vpc-bp1c85tzgqu1bf5b****",
 "SeriesCode":"alpha",
 "InstanceStatus":"RUNNING",
 "PublicNetworkAccess":true,
 "InternetEndpoint":"tsiqvqjjlq-public.dbaudit.aliyuncs.com",
 "RegionId":"cn-hangzhou",
 "ExpireTime":1578067200000,
 "IntranetEndpoint":"tsiqvqjjlq.dbaudit.aliyuncs.com"
	}
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Yundun-dbaudit)查看更多错误码。

