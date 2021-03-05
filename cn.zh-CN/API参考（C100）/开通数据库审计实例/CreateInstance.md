# CreateInstance

调用CreateInstance创建一个实例，并自动支付。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=BssOpenApi&api=CreateInstance&type=RPC&version=2017-12-14)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|CreateInstance|要执行的操作。取值：CreateInstance。|
|Parameter.1.Code|String|是|SeriesCode|数据库审计第1组属性的Code配置，设置为**SeriesCode**，表示数据库审计的型号系列。|
|Parameter.1.Value|String|是|alpha|数据库审计的第1组属性的Value配置，设置为**alpha**，表示数据库审计的型号系列设置为C100。|
|Parameter.2.Code|String|是|NetworkType|数据库审计的第2组属性的Code配置，设置为**NetworkType**，表示数据库审计的网络。|
|Parameter.2.Value|String|是|vpc|数据库审计的第2组属性的Value配置，设置为**vpc**，表示数据库审计的网络取值为vpc-VPC。|
|Parameter.3.Code|String|是|PlanCode|数据库审计的第3组属性的Code配置，设置为**PlanCode**，表示数据库审计的版本。|
|Parameter.3.Value|String|是|alpha.basic|数据库审计的第3组属性的Value配置，数据库审计的版本类型，取值：-   **alpha.advance**：企业版支持25个实例的版本。
-   **alpha.advanceplus**：企业版支持50个实例的版本。
-   **alpha.professional**：专业版支持3个实例的版本。
-   **alpha.basic**：高级版支持5个实例的版本。
-   **alpha.premium**：高级增强版支持10个实例的版本。
-   **alpha.ultimate**：旗舰版支持80个实例的版本。 |
|Parameter.4.Code|String|是|LogStorage|数据库审计的第4组属性的Code配置，设置为**LogStorage**，表示数据库审计的日志存储。|
|Parameter.4.Value|String|是|5|数据库审计的第4组属性的Value配置，数据库审计的日志存储大小，取值范围：0 TB~20 TB。|
|Parameter.5.Code|String|是|RegionId|数据库审计的第5组属性的Code配置，设置为**RegionId**，表示数据库审计实例的地域。|
|Parameter.5.Value|String|是|cn-shanghai|数据库审计的第5组属性的Value配置，数据库审计开放售卖的地域，取值：-   **cn-hangzhou**：华东1（杭州）
-   **cn-shanghai**：华东2（上海）
-   **cn-qingdao**：华北1（青岛）
-   **cn-beijing**：华北2（北京）
-   **cn-zhangjiakou**：华北3（张家口）
-   **cn-huhehaote**：华北5（呼和浩特）
-   **cn-shenzhen**：华南1（深圳）
-   **cn-hongkong**：中国（香港）
-   **cn-chengdu**：西南1（成都）
-   **ap-northeast-1**：日本（东京）
-   **ap-southeast-1**：新加坡
-   **ap-southeast-2**：澳大利亚（悉尼）
-   **ap-southeast-3**：马来西亚（吉隆坡）
-   **ap-southeast-5**：印度尼西亚（雅加达）
-   **ap-south-1**：印度（孟买）
-   **eu-central-1**：德国（法兰克福）
-   **us-east-1**：美国（弗吉尼亚）
-   **us-west-1**：美国（硅谷） |
|ProductCode|String|是|dbaudit|产品代码。数据库审计产品代码为**dbaudit**。 |
|SubscriptionType|String|是|Subscription|付费类型。数据库审计需设置为**Subscription**，预付费类型。 |
|ProductType|String|否|dbaudit|产品类型。数据库审计产品类型为**dbaudit**。 |
|RenewPeriod|Integer|否|12|自动续费周期， 单位为月。

**说明：** 当设置**RenewalStatus**为**AutoRenewal**时，必须设置。 |
|Period|Integer|是|12|预付费周期。单位为月，按年付费产品请输入12的整数倍。**说明：** 当创建预付费实例时，必须设置。 |
|RenewalStatus|String|否|ManualRenewal|自动续费状态，取值：-   **AutoRenewal**：自动续费。
-   **ManualRenewal**：手动续费。

默认**ManualRenewal**。 |
|ClientToken|String|否|JASIOFKVNVI\*\*\*\*|客户端幂等参数，服务端会查询是否有相同ClientToken的请求，如果有，直接返回上次调用结果。|

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|String|Success|本次请求的状态码。|
|Data|Struct| |本次请求的返回信息。|
|InstanceId|String|dbaudit-cn-\*\*\*\*|本次请求的实例ID。|
|OrderId|String|20240\*\*\*\*|创建成功的订单ID。|
|Message|String|Successful！|**Code**对应的状态码信息。|
|RequestId|String|6000EE23-274B-4E07-A697-FF2E999520A4|本次请求的ID。|
|Success|Boolean|true|本次请求是否成功。取值：-   **true**：请求成功。
-   **false**：请求失败。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=CreateInstance
&Parameter.1.Code=SeriesCode
&Parameter.1.Value=alpha
&Parameter.2.Code=NetworkType
&Parameter.2.Value=vpc
&Parameter.3.Code=PlanCode
&Parameter.3.Value=alpha.basic
&Parameter.4.Code=LogStorage
&Parameter.4.Value=5
&Parameter.5.Code=RegionId
&Parameter.5.Value=cn-shanghai
&ProductCode=dbaudit
&SubscriptionType=Subscription
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<CreateInstanceResponse>
      <Message>Successful!</Message>
      <RequestId>6000EE23-274B-4E07-A697-FF2E999520A4</RequestId>
      <Success>true</Success>
      <Code>Success</Code>
      <Data>
            <InstanceId>dbaudit-cn-****</InstanceId>
            <OrderId>20240****</OrderId>
      </Data>
</CreateInstanceResponse>
```

`JSON` 格式

```
{
    "Message": "Successful!",
    "RequestId": "6000EE23-274B-4E07-A697-FF2E999520A4",
    "Success": true,
    "Code": "Success",
    "Data": {
        "InstanceId": "dbaudit-cn-****",
        "OrderId": "20240****"
    }
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/BssOpenApi)查看更多错误码。

