# DescribeInstances

调用DescribeInstances查询实例的列表信息。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Yundun-dbaudit&api=DescribeInstances&type=RPC&version=2019-12-09)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeInstances|要执行的操作。

 取值：DescribeInstances。 |
|PageSize|Integer|否|10|输入时设置的每页行数。

 默认取值为20，最大值为100。 |
|PageNumber|Integer|否|1|实例列表的当前页码。 |
|RegionId|String|否|cn-hangzhou|数据库审计实例的地域ID。

 可以通过调用[DescribeRegions](~~162344~~)接口获取地域ID。 |
|InstanceStatus|String|否|RUNNING|实例状态。取值：

 -   PENDING：未初始化
-   CREATING：创建中
-   RUNNING：运行中
-   EXPIRED：已过期
-   CREATE\_FAILED：创建失败
-   UPGRADING：变配中
-   UPGRADE\_FAILED：变配失败 |
|ResourceGroupId|String|否|rg-acfm26ougij6\*\*\*\*|实例所在的企业资源组ID。 |
|InstanceId.N|RepeatList|否|dbaudit-cn-78v1gc\*\*\*\*|审计的实例ID。

 N表示实例ID的序号，取值范围：1~20。 |
|Tag.N.Key|String|否|test|实例的标签键。

 N表示标签键的序号，取值范围：1~20。 |
|Tag.N.Value|String|否|testapi|实例的标签值。

 N表示标签值的序号，取值范围：1~20。 |

调用API时，除了本文中该API的请求参数，还需加入阿里云API公共请求参数。公共请求参数的详细介绍，请参见[公共参数](~~148151~~)。

调用API的请求格式，请参见本文示例中的请求示例。

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Instances|Array of Instance| |实例列表信息。 |
|Description|String|新购实例|实例的备注信息。 |
|ExpireTime|Long|1578067200000|实例的过期时间。

 单位：毫秒。 |
|InstanceId|String|dbaudit-cn-78v1gc\*\*\*\*|本次请求的实例ID。 |
|InstanceStatus|String|RUNNING|实例状态。取值：

 -   **PENDING**：未初始化
-   **CREATING**：创建中
-   **RUNNING**：运行中
-   **EXPIRED**：已过期
-   **CREATE\_FAILED**：创建失败
-   **UPGRADING**：变配中
-   **UPGRADE\_FAILED**：变配失败 |
|InternetEndpoint|String|tsiqvqjjlq-public.dbaudit.aliyuncs.com|实例的公网域名。 |
|IntranetEndpoint|String|tsiqvqjjlq.dbaudit.aliyuncs.com|实例的私网域名。 |
|LicenseCode|String|alpha.professional|实例的套餐Code。

 用户购买实例时选择的套餐对应的Code。 |
|PublicNetworkAccess|Boolean|true|是否可以通过公网访问该审计实例。默认值为**false**。

 -   **true**：可以通过公网访问该审计实例。
-   **false**：不能通过公网访问该审计实例。 |
|RegionId|String|cn-hangzhou|地域ID。 |
|SeriesCode|String|alpha|购买实例时的系列Code。 |
|StartTime|Long|1577437765000|实例的开始时间。

 用时间戳表示，即购买实例的时间。单位：毫秒。 |
|VpcId|String|vpc-bp1c85tzgqu1bf5b\*\*\*\*|实例绑定的VPC ID。 |
|VswitchId|String|vsw-bp1kep1f0k5fnyfs\*\*\*\*|实例绑定的交换机ID。 |
|RequestId|String|12AA0353-F01D-43E2-A85C-9040F7A35D93|本次请求的ID。 |
|TotalCount|Long|18|实例总数量。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DescribeInstances
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<DescribeInstances>
  <Instances>
        <LicenseCode>alpha.ultimate</LicenseCode>
        <Description>zqytest</Description>
        <InstanceId>dbaudit-cn-78v1gi****</InstanceId>
        <StartTime>1577692358000</StartTime>
        <VswitchId>vsw-bp1xfwzzfti0kjbf****</VswitchId>
        <VpcId>vpc-bp1c85tzgqu1bf5b****</VpcId>
        <SeriesCode>alpha</SeriesCode>
        <InstanceStatus>RUNNING</InstanceStatus>
        <PublicNetworkAccess>true</PublicNetworkAccess>
        <InternetEndpoint>bwkjvpoiak-public.dbaudit.aliyuncs.com</InternetEndpoint>
        <RegionId>cn-hangzhou</RegionId>
        <ExpireTime>1673020800000</ExpireTime>
        <IntranetEndpoint>bwkjvpoiak.dbaudit.aliyuncs.com</IntranetEndpoint>
  </Instances>
  <Instances>
        <LicenseCode>alpha.ultimate</LicenseCode>
        <Description>zqytest</Description>
        <VpcId>vpc-bp1c85tzgqu1bf5b****</VpcId>
        <SeriesCode>alpha</SeriesCode>
        <InstanceId>dbaudit-cn-78v1gi****</InstanceId>
        <InstanceStatus>RUNNING</InstanceStatus>
        <PublicNetworkAccess>false</PublicNetworkAccess>
        <StartTime>1577692131000</StartTime>
        <RegionId>cn-hangzhou</RegionId>
        <ExpireTime>1641484800000</ExpireTime>
        <VswitchId>vsw-bp1xfwzzfti0kjbf****</VswitchId>
        <IntranetEndpoint>mpjuwtmrne.dbaudit.aliyuncs.com</IntranetEndpoint>
  </Instances>
  <Instances>
        <LicenseCode>alpha.advanceplus</LicenseCode>
        <Description>zqytest</Description>
        <VpcId>vpc-bp1c85tzgqu1bf5b****</VpcId>
        <SeriesCode>alpha</SeriesCode>
        <InstanceId>dbaudit-cn-78v1gi****</InstanceId>
        <InstanceStatus>RUNNING</InstanceStatus>
        <PublicNetworkAccess>false</PublicNetworkAccess>
        <StartTime>1577691982000</StartTime>
        <RegionId>cn-hangzhou</RegionId>
        <ExpireTime>1609948800000</ExpireTime>
        <VswitchId>vsw-bp1xfwzzfti0kjbf****</VswitchId>
        <IntranetEndpoint>pgcmjjnxem.dbaudit.aliyuncs.com</IntranetEndpoint>
  </Instances>
  <Instances>
        <LicenseCode>alpha.advance</LicenseCode>
        <Description>zqytest</Description>
        <VpcId>vpc-bp1c85tzgqu1bf5b****</VpcId>
        <SeriesCode>alpha</SeriesCode>
        <InstanceId>dbaudit-cn-78v1gi****</InstanceId>
        <InstanceStatus>RUNNING</InstanceStatus>
        <PublicNetworkAccess>false</PublicNetworkAccess>
        <StartTime>1577691688000</StartTime>
        <RegionId>cn-hangzhou</RegionId>
        <ExpireTime>1594051200000</ExpireTime>
        <VswitchId>vsw-bp1xfwzzfti0kjbf****</VswitchId>
        <IntranetEndpoint>pbglirkagy.dbaudit.aliyuncs.com</IntranetEndpoint>
  </Instances>
  <Instances>
        <LicenseCode>alpha.premium</LicenseCode>
        <Description>zqytest</Description>
        <VpcId>vpc-bp1c85tzgqu1bf5b****</VpcId>
        <SeriesCode>alpha</SeriesCode>
        <InstanceId>dbaudit-cn-78v1gi****</InstanceId>
        <InstanceStatus>RUNNING</InstanceStatus>
        <PublicNetworkAccess>false</PublicNetworkAccess>
        <StartTime>1577690912000</StartTime>
        <RegionId>cn-hangzhou</RegionId>
        <ExpireTime>1586188800000</ExpireTime>
        <VswitchId>vsw-bp1xfwzzfti0kjbf****</VswitchId>
        <IntranetEndpoint>mermmouqlb.dbaudit.aliyuncs.com</IntranetEndpoint>
  </Instances>
  <Instances>
        <LicenseCode>alpha.basic</LicenseCode>
        <Description>zqytest</Description>
        <VpcId>vpc-bp1c85tzgqu1bf5b****</VpcId>
        <SeriesCode>alpha</SeriesCode>
        <InstanceId>dbaudit-cn-o401gh****</InstanceId>
        <InstanceStatus>RUNNING</InstanceStatus>
        <PublicNetworkAccess>false</PublicNetworkAccess>
        <StartTime>1577686183000</StartTime>
        <RegionId>cn-hangzhou</RegionId>
        <ExpireTime>1581004800000</ExpireTime>
        <VswitchId>vsw-bp1xfwzzfti0kjbf****</VswitchId>
        <IntranetEndpoint>eqyqivsqny.dbaudit.aliyuncs.com</IntranetEndpoint>
  </Instances>
  <Instances>
        <LicenseCode>alpha.premium</LicenseCode>
        <Description>2216测试10实例</Description>
        <VpcId>vpc-bp1411rrm10vr9x2****</VpcId>
        <SeriesCode>alpha</SeriesCode>
        <InstanceId>dbaudit-cn-78v1gh****</InstanceId>
        <InstanceStatus>RUNNING</InstanceStatus>
        <PublicNetworkAccess>false</PublicNetworkAccess>
        <StartTime>1577673845000</StartTime>
        <RegionId>cn-hangzhou</RegionId>
        <ExpireTime>1578326400000</ExpireTime>
        <VswitchId>vsw-bp1myai68sgektqr****</VswitchId>
        <IntranetEndpoint>jgdtirwwlj.dbaudit.aliyuncs.com</IntranetEndpoint>
  </Instances>
  <Instances>
        <LicenseCode>alpha.professional</LicenseCode>
        <VpcId>vpc-bp1c85tzgqu1bf5b****</VpcId>
        <SeriesCode>alpha</SeriesCode>
        <InstanceId>dbaudit-cn-v0h1gg****</InstanceId>
        <InstanceStatus>RUNNING</InstanceStatus>
        <PublicNetworkAccess>false</PublicNetworkAccess>
        <StartTime>1577630757000</StartTime>
        <RegionId>cn-hangzhou</RegionId>
        <ExpireTime>1578240000000</ExpireTime>
        <VswitchId>vsw-bp1kybm1l2ybnbwm****</VswitchId>
        <IntranetEndpoint>gprnimowey.dbaudit.aliyuncs.com</IntranetEndpoint>
  </Instances>
  <Instances>
        <LicenseCode>alpha.professional</LicenseCode>
        <Description>新购实例</Description>
        <InstanceId>dbaudit-cn-78v1gc****</InstanceId>
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
  </Instances>
  <Instances>
        <LicenseCode>alpha.basic</LicenseCode>
        <Description>2_2_16交付测试</Description>
        <VpcId>vpc-bp1411rrm10vr9x2****</VpcId>
        <SeriesCode>alpha</SeriesCode>
        <InstanceId>dbaudit-cn-4591gc****</InstanceId>
        <InstanceStatus>RUNNING</InstanceStatus>
        <PublicNetworkAccess>false</PublicNetworkAccess>
        <StartTime>1577424426000</StartTime>
        <RegionId>cn-hangzhou</RegionId>
        <ExpireTime>1578067200000</ExpireTime>
        <VswitchId>vsw-bp1myai68sgektqr****</VswitchId>
        <IntranetEndpoint>ijsvooheee.dbaudit.aliyuncs.com</IntranetEndpoint>
  </Instances>
  <Instances>
        <LicenseCode>alpha.professional</LicenseCode>
        <Description>2216IP端口限制自测</Description>
        <VpcId>vpc-bp1411rrm10vr9x2****</VpcId>
        <SeriesCode>alpha</SeriesCode>
        <InstanceId>dbaudit-cn-78v1gc****</InstanceId>
        <InstanceStatus>RUNNING</InstanceStatus>
        <PublicNetworkAccess>false</PublicNetworkAccess>
        <StartTime>1577419682000</StartTime>
        <RegionId>cn-hangzhou</RegionId>
        <ExpireTime>1578067200000</ExpireTime>
        <VswitchId>vsw-bp1myai68sgektqr****</VswitchId>
        <IntranetEndpoint>mtyrqhjpkm.dbaudit.aliyuncs.com</IntranetEndpoint>
  </Instances>
  <Instances>
        <LicenseCode>alpha.professional</LicenseCode>
        <SeriesCode>alpha</SeriesCode>
        <InstanceId>dbaudit-cn-4591gc****</InstanceId>
        <InstanceStatus>PENDING</InstanceStatus>
        <PublicNetworkAccess>false</PublicNetworkAccess>
        <StartTime>1577418638000</StartTime>
        <RegionId>cn-hangzhou</RegionId>
        <ExpireTime>1578067200000</ExpireTime>
  </Instances>
  <Instances>
        <LicenseCode>alpha.professional</LicenseCode>
        <Description>自测</Description>
        <VpcId>vpc-bp1411rrm10vr9x2****</VpcId>
        <SeriesCode>alpha</SeriesCode>
        <InstanceId>dbaudit-cn-4591gc****</InstanceId>
        <InstanceStatus>RUNNING</InstanceStatus>
        <PublicNetworkAccess>false</PublicNetworkAccess>
        <StartTime>1577414007000</StartTime>
        <RegionId>cn-hangzhou</RegionId>
        <ExpireTime>1578067200000</ExpireTime>
        <VswitchId>vsw-bp1myai68sgektqr****</VswitchId>
        <IntranetEndpoint>fxoqtqdrsf.dbaudit.aliyuncs.com</IntranetEndpoint>
  </Instances>
  <Instances>
        <LicenseCode>alpha.basic</LicenseCode>
        <VpcId>vpc-bp1c85tzgqu1bf5b****</VpcId>
        <SeriesCode>alpha</SeriesCode>
        <InstanceId>dbaudit-cn-0pp1gb****</InstanceId>
        <InstanceStatus>RUNNING</InstanceStatus>
        <PublicNetworkAccess>false</PublicNetworkAccess>
        <StartTime>1577361597000</StartTime>
        <RegionId>cn-hangzhou</RegionId>
        <ExpireTime>1580659200000</ExpireTime>
        <VswitchId>vsw-bp1xfwzzfti0kjbf****</VswitchId>
        <IntranetEndpoint>jqslxwsvvh.dbaudit.aliyuncs.com</IntranetEndpoint>
  </Instances>
  <Instances>
        <LicenseCode>alpha.professional</LicenseCode>
        <Description>2_2_15版本测试</Description>
        <InstanceId>dbaudit-cn-mp91g6****</InstanceId>
        <StartTime>1577154573000</StartTime>
        <VswitchId>vsw-bp1xfwzzfti0kjbf****</VswitchId>
        <VpcId>vpc-bp1c85tzgqu1bf5b****</VpcId>
        <SeriesCode>alpha</SeriesCode>
        <InstanceStatus>RUNNING</InstanceStatus>
        <PublicNetworkAccess>true</PublicNetworkAccess>
        <InternetEndpoint>fspttgbrui-public.dbaudit.aliyuncs.com</InternetEndpoint>
        <RegionId>cn-hangzhou</RegionId>
        <ExpireTime>1577808000000</ExpireTime>
        <IntranetEndpoint>fspttgbrui.dbaudit.aliyuncs.com</IntranetEndpoint>
  </Instances>
  <Instances>
        <LicenseCode>alpha.professional</LicenseCode>
        <Description>12</Description>
        <InstanceId>dbaudit-cn-0pp1g4****</InstanceId>
        <StartTime>1577072644000</StartTime>
        <VswitchId>vsw-bp1xfwzzfti0kjbf****</VswitchId>
        <VpcId>vpc-bp1c85tzgqu1bf5b****</VpcId>
        <SeriesCode>alpha</SeriesCode>
        <InstanceStatus>RUNNING</InstanceStatus>
        <PublicNetworkAccess>false</PublicNetworkAccess>
        <InternetEndpoint>ibwlpgbfuq-public.dbaudit.aliyuncs.com</InternetEndpoint>
        <RegionId>cn-hangzhou</RegionId>
        <ExpireTime>1577721600000</ExpireTime>
        <IntranetEndpoint>ibwlpgbfuq.dbaudit.aliyuncs.com</IntranetEndpoint>
  </Instances>
  <Instances>
        <LicenseCode>alpha.premium</LicenseCode>
        <Description>安恒开发用实例_请勿释放</Description>
        <InstanceId>dbaudit-cn-v641b8****</InstanceId>
        <StartTime>1568861065000</StartTime>
        <VswitchId>vsw-bp1myai68sgektqr****</VswitchId>
        <VpcId>vpc-bp1411rrm10vr9x2****</VpcId>
        <SeriesCode>alpha</SeriesCode>
        <InstanceStatus>RUNNING</InstanceStatus>
        <PublicNetworkAccess>false</PublicNetworkAccess>
        <InternetEndpoint>pyuyfpidsy-public.dbaudit.aliyuncs.com</InternetEndpoint>
        <RegionId>cn-hangzhou</RegionId>
        <ExpireTime>1601136000000</ExpireTime>
        <IntranetEndpoint>pyuyfpidsy.dbaudit.aliyuncs.com</IntranetEndpoint>
  </Instances>
  <Instances>
        <LicenseCode>alpha.advance</LicenseCode>
        <Description>线上联调实例代码更新_禁止变更</Description>
        <InstanceId>dbaudit-cn-v0h19i****</InstanceId>
        <StartTime>1565959995000</StartTime>
        <VswitchId>vsw-bp1myai68sgektqr****</VswitchId>
        <VpcId>vpc-bp1411rrm10vr9x2****</VpcId>
        <SeriesCode>alpha</SeriesCode>
        <InstanceStatus>RUNNING</InstanceStatus>
        <PublicNetworkAccess>true</PublicNetworkAccess>
        <InternetEndpoint>rnqnscsbmr-public.dbaudit.aliyuncs.com</InternetEndpoint>
        <RegionId>cn-hangzhou</RegionId>
        <ExpireTime>1585238400000</ExpireTime>
        <IntranetEndpoint>rnqnscsbmr.dbaudit.aliyuncs.com</IntranetEndpoint>
  </Instances>
  <TotalCount>18</TotalCount>
  <RequestId>12AA0353-F01D-43E2-A85C-9040F7A35D93</RequestId>
</DescribeInstances>
```

`JSON`格式

```
{
	"Instances":[
		{
			"LicenseCode":"alpha.ultimate",
			"Description":"zqytest",
			"InstanceId":"dbaudit-cn-78v1gi****",
			"StartTime":1577692358000,
			"VswitchId":"vsw-bp1xfwzzfti0kjbf****",
			"VpcId":"vpc-bp1c85tzgqu1bf5b****",
			"SeriesCode":"alpha",
			"InstanceStatus":"RUNNING",
			"PublicNetworkAccess":true,
			"InternetEndpoint":"bwkjvpoiak-public.dbaudit.aliyuncs.com",
			"RegionId":"cn-hangzhou",
			"ExpireTime":1673020800000,
			"IntranetEndpoint":"bwkjvpoiak.dbaudit.aliyuncs.com"
		},
		{
			"LicenseCode":"alpha.ultimate",
			"Description":"zqytest",
			"VpcId":"vpc-bp1c85tzgqu1bf5b****",
			"SeriesCode":"alpha",
			"InstanceId":"dbaudit-cn-78v1gi****",
			"InstanceStatus":"RUNNING",
			"PublicNetworkAccess":false,
			"StartTime":1577692131000,
			"RegionId":"cn-hangzhou",
			"ExpireTime":1641484800000,
			"VswitchId":"vsw-bp1xfwzzfti0kjbf****",
			"IntranetEndpoint":"mpjuwtmrne.dbaudit.aliyuncs.com"
		},
		{
			"LicenseCode":"alpha.advanceplus",
			"Description":"zqytest",
			"VpcId":"vpc-bp1c85tzgqu1bf5b****",
			"SeriesCode":"alpha",
			"InstanceId":"dbaudit-cn-78v1gi****",
			"InstanceStatus":"RUNNING",
			"PublicNetworkAccess":false,
			"StartTime":1577691982000,
			"RegionId":"cn-hangzhou",
			"ExpireTime":1609948800000,
			"VswitchId":"vsw-bp1xfwzzfti0kjbf****",
			"IntranetEndpoint":"pgcmjjnxem.dbaudit.aliyuncs.com"
		},
		{
			"LicenseCode":"alpha.advance",
			"Description":"zqytest",
			"VpcId":"vpc-bp1c85tzgqu1bf5b****",
			"SeriesCode":"alpha",
			"InstanceId":"dbaudit-cn-78v1gi****",
			"InstanceStatus":"RUNNING",
			"PublicNetworkAccess":false,
			"StartTime":1577691688000,
			"RegionId":"cn-hangzhou",
			"ExpireTime":1594051200000,
			"VswitchId":"vsw-bp1xfwzzfti0kjbf****",
			"IntranetEndpoint":"pbglirkagy.dbaudit.aliyuncs.com"
		},
		{
			"LicenseCode":"alpha.premium",
			"Description":"zqytest",
			"VpcId":"vpc-bp1c85tzgqu1bf5b****",
			"SeriesCode":"alpha",
			"InstanceId":"dbaudit-cn-78v1gi****",
			"InstanceStatus":"RUNNING",
			"PublicNetworkAccess":false,
			"StartTime":1577690912000,
			"RegionId":"cn-hangzhou",
			"ExpireTime":1586188800000,
			"VswitchId":"vsw-bp1xfwzzfti0kjbf****",
			"IntranetEndpoint":"mermmouqlb.dbaudit.aliyuncs.com"
		},
		{
			"LicenseCode":"alpha.basic",
			"Description":"zqytest",
			"VpcId":"vpc-bp1c85tzgqu1bf5b****",
			"SeriesCode":"alpha",
			"InstanceId":"dbaudit-cn-o401gh****",
			"InstanceStatus":"RUNNING",
			"PublicNetworkAccess":false,
			"StartTime":1577686183000,
			"RegionId":"cn-hangzhou",
			"ExpireTime":1581004800000,
			"VswitchId":"vsw-bp1xfwzzfti0kjbf****",
			"IntranetEndpoint":"eqyqivsqny.dbaudit.aliyuncs.com"
		},
		{
			"LicenseCode":"alpha.premium",
			"Description":"2216测试10实例",
			"VpcId":"vpc-bp1411rrm10vr9x2****",
			"SeriesCode":"alpha",
			"InstanceId":"dbaudit-cn-78v1gh****",
			"InstanceStatus":"RUNNING",
			"PublicNetworkAccess":false,
			"StartTime":1577673845000,
			"RegionId":"cn-hangzhou",
			"ExpireTime":1578326400000,
			"VswitchId":"vsw-bp1myai68sgektqr****",
			"IntranetEndpoint":"jgdtirwwlj.dbaudit.aliyuncs.com"
		},
		{
			"LicenseCode":"alpha.professional",
			"VpcId":"vpc-bp1c85tzgqu1bf5b****",
			"SeriesCode":"alpha",
			"InstanceId":"dbaudit-cn-v0h1gg****",
			"InstanceStatus":"RUNNING",
			"PublicNetworkAccess":false,
			"StartTime":1577630757000,
			"RegionId":"cn-hangzhou",
			"ExpireTime":1578240000000,
			"VswitchId":"vsw-bp1kybm1l2ybnbwm****",
			"IntranetEndpoint":"gprnimowey.dbaudit.aliyuncs.com"
		},
		{
			"LicenseCode":"alpha.professional",
			"Description":"新购实例",
			"InstanceId":"dbaudit-cn-78v1gc****",
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
		},
		{
			"LicenseCode":"alpha.basic",
			"Description":"2_2_16交付测试",
			"VpcId":"vpc-bp1411rrm10vr9x2****",
			"SeriesCode":"alpha",
			"InstanceId":"dbaudit-cn-4591gc****",
			"InstanceStatus":"RUNNING",
			"PublicNetworkAccess":false,
			"StartTime":1577424426000,
			"RegionId":"cn-hangzhou",
			"ExpireTime":1578067200000,
			"VswitchId":"vsw-bp1myai68sgektqr****",
			"IntranetEndpoint":"ijsvooheee.dbaudit.aliyuncs.com"
		},
		{
			"LicenseCode":"alpha.professional",
			"Description":"2216IP端口限制自测",
			"VpcId":"vpc-bp1411rrm10vr9x2****",
			"SeriesCode":"alpha",
			"InstanceId":"dbaudit-cn-78v1gc****",
			"InstanceStatus":"RUNNING",
			"PublicNetworkAccess":false,
			"StartTime":1577419682000,
			"RegionId":"cn-hangzhou",
			"ExpireTime":1578067200000,
			"VswitchId":"vsw-bp1myai68sgektqr****",
			"IntranetEndpoint":"mtyrqhjpkm.dbaudit.aliyuncs.com"
		},
		{
			"LicenseCode":"alpha.professional",
			"SeriesCode":"alpha",
			"InstanceId":"dbaudit-cn-4591gc****",
			"InstanceStatus":"PENDING",
			"PublicNetworkAccess":false,
			"StartTime":1577418638000,
			"RegionId":"cn-hangzhou",
			"ExpireTime":1578067200000
		},
		{
			"LicenseCode":"alpha.professional",
			"Description":"自测",
			"VpcId":"vpc-bp1411rrm10vr9x2****",
			"SeriesCode":"alpha",
			"InstanceId":"dbaudit-cn-4591gc****",
			"InstanceStatus":"RUNNING",
			"PublicNetworkAccess":false,
			"StartTime":1577414007000,
			"RegionId":"cn-hangzhou",
			"ExpireTime":1578067200000,
			"VswitchId":"vsw-bp1myai68sgektqr****",
			"IntranetEndpoint":"fxoqtqdrsf.dbaudit.aliyuncs.com"
		},
		{
			"LicenseCode":"alpha.basic",
			"VpcId":"vpc-bp1c85tzgqu1bf5b****",
			"SeriesCode":"alpha",
			"InstanceId":"dbaudit-cn-0pp1gb****",
			"InstanceStatus":"RUNNING",
			"PublicNetworkAccess":false,
			"StartTime":1577361597000,
			"RegionId":"cn-hangzhou",
			"ExpireTime":1580659200000,
			"VswitchId":"vsw-bp1xfwzzfti0kjbf****",
			"IntranetEndpoint":"jqslxwsvvh.dbaudit.aliyuncs.com"
		},
		{
			"LicenseCode":"alpha.professional",
			"Description":"2_2_15版本测试",
			"InstanceId":"dbaudit-cn-mp91g6****",
			"StartTime":1577154573000,
			"VswitchId":"vsw-bp1xfwzzfti0kjbf****",
			"VpcId":"vpc-bp1c85tzgqu1bf5b****",
			"SeriesCode":"alpha",
			"InstanceStatus":"RUNNING",
			"PublicNetworkAccess":true,
			"InternetEndpoint":"fspttgbrui-public.dbaudit.aliyuncs.com",
			"RegionId":"cn-hangzhou",
			"ExpireTime":1577808000000,
			"IntranetEndpoint":"fspttgbrui.dbaudit.aliyuncs.com"
		},
		{
			"LicenseCode":"alpha.professional",
			"Description":"12",
			"InstanceId":"dbaudit-cn-0pp1g4****",
			"StartTime":1577072644000,
			"VswitchId":"vsw-bp1xfwzzfti0kjbf****",
			"VpcId":"vpc-bp1c85tzgqu1bf5b****",
			"SeriesCode":"alpha",
			"InstanceStatus":"RUNNING",
			"PublicNetworkAccess":false,
			"InternetEndpoint":"ibwlpgbfuq-public.dbaudit.aliyuncs.com",
			"RegionId":"cn-hangzhou",
			"ExpireTime":1577721600000,
			"IntranetEndpoint":"ibwlpgbfuq.dbaudit.aliyuncs.com"
		},
		{
			"LicenseCode":"alpha.premium",
			"Description":"安恒开发用实例_请勿释放",
			"InstanceId":"dbaudit-cn-v641b8****",
			"StartTime":1568861065000,
			"VswitchId":"vsw-bp1myai68sgektqr****",
			"VpcId":"vpc-bp1411rrm10vr9x2****",
			"SeriesCode":"alpha",
			"InstanceStatus":"RUNNING",
			"PublicNetworkAccess":false,
			"InternetEndpoint":"pyuyfpidsy-public.dbaudit.aliyuncs.com",
			"RegionId":"cn-hangzhou",
			"ExpireTime":1601136000000,
			"IntranetEndpoint":"pyuyfpidsy.dbaudit.aliyuncs.com"
		},
		{
			"LicenseCode":"alpha.advance",
			"Description":"线上联调实例代码更新_禁止变更",
			"InstanceId":"dbaudit-cn-v0h19i****",
			"StartTime":1565959995000,
			"VswitchId":"vsw-bp1myai68sgektqr****",
			"VpcId":"vpc-bp1411rrm10vr9x2****",
			"SeriesCode":"alpha",
			"InstanceStatus":"RUNNING",
			"PublicNetworkAccess":true,
			"InternetEndpoint":"rnqnscsbmr-public.dbaudit.aliyuncs.com",
			"RegionId":"cn-hangzhou",
			"ExpireTime":1585238400000,
			"IntranetEndpoint":"rnqnscsbmr.dbaudit.aliyuncs.com"
		}
	],
	"TotalCount":18,
	"RequestId":"12AA0353-F01D-43E2-A85C-9040F7A35D93"
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Yundun-dbaudit)查看更多错误码。

