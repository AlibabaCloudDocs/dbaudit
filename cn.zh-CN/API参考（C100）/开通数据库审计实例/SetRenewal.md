# SetRenewal

调用SetRenewal为一个实例设置自动续费服务。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=BssOpenApi&api=SetRenewal&type=RPC&version=2017-12-14)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|SetRenewal|要执行的操作。取值：SetRenewal。|
|InstanceIDs|String|是|dbaudit-cn-\*\*\*\*|实例ID。多个ID用英文逗号分隔，最大不超过100个包年包月实例。|
|RenewalStatus|String|是|AutoRenewal|续费状态，取值：

-   **AutoRenewal**：自动续费。
-   **ManualRenewal**：手动续费。
-   **NotRenewal**：不续费。 |
|RenewalPeriod|Integer|否|1|设置实例自动续费时长，单位为月，取值：

-   1
-   2
-   3
-   6
-   12

**说明：** 当**RenewalStatus**取值为**AutoRenewal**时，**RenewalPeriod**为必填参数。 |
|ProductCode|String|否|dbaudit|产品代码。数据库审计产品代码为**dbaudit**。 |
|ProductType|String|否|dbaudit|产品类型。数据库审计产品类型为**dbaudit**。 |
|SubscriptionType|String|否|Subscription|付费类型。数据库审计需设置为**Subscription**，表示预付费类型。 |
|RenewalPeriodUnit|String|否|M|自动续费周期单位，取值：

-   **M**：月。
-   **Y**：年。

**说明：** 当**RenewalStatus**取值为**AutoRenewal**时，**RenewalPeriodUnit**为必填参数。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|String|Success|本次请求的状态码。|
|Message|String|Successful|**Code**对应的状态码信息。|
|RequestId|String|6000EE23-274B-4E07-A697-FF2E999520A4|本次请求的ID。|
|Success|Boolean|true|本次请求是否成功。|

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=SetRenewal
&InstanceIDs=dbaudit-cn-****
&RenewalStatus=AutoRenewal
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<SetRenewalResponse>
      <Message>Successful!</Message>
      <RequestId>6000EE23-274B-4E07-A697-FF2E999520A4</RequestId>
      <Success>true</Success>
      <Code>Success</Code>
</SetRenewalResponse>
```

`JSON` 格式

```
{
    "Message": "Successful!",
    "RequestId": "6000EE23-274B-4E07-A697-FF2E999520A4",
    "Success": true,
    "Code": "Success"
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/BssOpenApi)查看更多错误码。

