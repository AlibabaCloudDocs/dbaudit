# RenewInstance

调用RenewInstance对实例进行续费。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=BssOpenApi&api=RenewInstance&type=RPC&version=2017-12-14)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|RenewInstance|要执行的操作。取值：RenewInstance。|
|InstanceId|String|是|dbaudit-cn-\*\*\*\*|本次请求的实例ID。|
|ProductCode|String|是|dbaudit|产品代码。数据库审计产品代码为**dbaudit**。 |
|RenewPeriod|Integer|是|6|预付费续费时长，单位：月。取值：

-   1~9。
-   12。
-   24。
-   36。 |
|ClientToken|String|否|JASIOFKVNVI\*\*\*\*|客户端幂等参数，服务端会查询是否有相同ClientToken的请求，如果有，直接返回上次调用结果。用于保证请求的幂等性，防止请求重复提交。|
|ProductType|String|否|dbaudit|产品类型。数据库审计产品类型为**dbaudit**。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|**Code**|String|Success|本次请求的状态码。|
|**Data**|Struct| |本次请求的返回信息。|
|**OrderId**|String|2026532523\*\*\*\*|创建成功的订单ID。|
|**Message**|String|Successful！|**Code**对应的状态码信息。|
|**RequestId**|String|6000EE23-274B-4E07-A697-FF2E999520A4|本次请求的ID。|
|**Success**|Boolean|true|本次请求是否成功。|

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=RenewInstance
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<RenewInstanceResponse>
      <Message>Successful!</Message>
      <RequestId>6000EE23-274B-4E07-A697-FF2E999520A4</RequestId>
      <Success>true</Success>
      <Code>Success</Code>
      <Data>
            <OrderId>2026532523****</OrderId>
      </Data>
</RenewInstanceResponse>
```

`JSON` 格式

```
{
    "Message": "Successful!",
    "RequestId": "6000EE23-274B-4E07-A697-FF2E999520A4",
    "Success": true,
    "Code": "Success",
    "Data": {
        "OrderId": 2026532523****
    }
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/BssOpenApi)查看更多错误码。

