# QueryAvailableInstances

调用QueryAvailableInstances查询用户已开通实例的列表。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=BssOpenApi&api=QueryAvailableInstances&type=RPC&version=2017-12-14)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|QueryAvailableInstances|要执行的操作。取值：QueryAvailableInstances。|
|Region|String|否|cn-hangzhou|地域，需要设置为**cn-hangzhou**。|
|PageNum|Integer|否|1|分页查询时，显示当前页的页码。|
|PageSize|Integer|否|20|分页查询时，显示的每页数据的最大条数。|
|ProductCode|String|否|dbaudit|产品代码。数据库审计产品代码为**dbaudit**。

**说明：** 当设置了**Region**时，不为空。 |
|ProductType|String|否|dbaudit|产品类型。数据库审计产品类型为**dbaudit**。 |
|SubscriptionType|String|否|Subscription|付费类型。数据库审计需设置为**Subscription**，表示预付费类型。 |
|InstanceIDs|String|否|dbaudit-cn-\*\*\*\*|实例ID。多个ID用英文逗号分隔，最大不超过100个。 |
|EndTimeStart|String|否|2020-05-23T12:00:00Z|实例到期时间的起始时间，符合ISO8601标准的UTC时间格式，例如2020-05-23T12:00:00Z。|
|EndTimeEnd|String|否|2020-05-23T12:00:00Z|实例到期时间的结束时间，符合ISO8601标准的UTC时间格式，例如2020-05-23T12:00:00Z。|
|CreateTimeStart|String|否|2020-05-23T12:00:00Z|开通实例的起始时间，符合ISO8601标准的UTC时间格式。|
|CreateTimeEnd|String|否|2020-05-23T12:00:00Z|开通实例的结束时间，符合ISO8601标准的UTC时间格式。|
|RenewStatus|String|否|AutoRenewal|续费状态，取值：-   **AutoRenewal**：自动续费。
-   **ManualRenewal**：手动续费。
-   **NotRenewal**：不续费。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Code|String|Success|本次请求的状态码。|
|Data|Struct| |本次请求的返回信息。|
|InstanceList|Array| |实例信息的列表。|
|CreateTime|String|2020-09-08T16:00:00Z|实例的创建时间。|
|EndTime|String|2020-11-07T16:00:00Z|实例的结束时间。|
|ExpectedReleaseTime|String|2020-11-07T16:00:00Z|期望释放实例的时间。|
|InstanceID|String|dbaudit-cn-\*\*\*\*|本次请求的实例ID。|
|OwnerId|Long|181\*\*\*\*|实例的所有者ID。|
|ProductCode|String|dbaudit|产品代码。|
|ProductType|String|dbaudit|产品类型。|
|Region|String|cn-hangzhou|实例的地域。|
|ReleaseTime|String|2020-11-07T16:00:00Z|实例的释放时间。|
|RenewStatus|String|ManualRenewal|续费状态，取值：-   **AutoRenewal**：自动续费。
-   **ManualRenewal**：手动续费。
-   **NotRenewal**：不续费。 |
|RenewalDuration|Integer|1|自动续费周期数量。|
|RenewalDurationUnit|String|M|自动续费周期单位，取值：-   **M**：月。
-   **Y**：年。 |
|Seller|String|26888|销售实例的卖方，可以是阿里云及其合作伙伴。|
|SellerId|Long|123123123|销售实例的卖方ID。|
|Status|String|Creating|实例的状态。|
|StopTime|String|2020-11-07T16:00:00Z|实例的停止时间。|
|SubStatus|String|Normal|实例的子状态。|
|SubscriptionType|String|Subscription|付费类型。数据库审计需设置为**Subscription**，表示预付费类型。 |
|PageNum|Integer|1|分页查询时，显示当前页的页码。|
|PageSize|Integer|10|分页查询时，显示的每页数据的最大条数。|
|TotalCount|Integer|11|实例列表的总记录数。|
|Message|String|Successful!|**Code**对应的状态码信息。|
|RequestId|String|C7C15585-8349-4C62-BEE4-5A391841B9BE|本次请求的ID。|
|Success|Boolean|true|本次请求是否成功。取值：-   **true**：请求成功。
-   **false**：请求失败。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=QueryAvailableInstances
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<QueryAvailableInstancesResponse>
      <Data>
            <TotalCount>51</TotalCount>
            <PageSize>20</PageSize>
            <PageNum>1</PageNum>
            <InstanceList>
                  <Status>Creating</Status>
                  <SubStatus>Normal</SubStatus>
                  <SubscriptionType>Subscription</SubscriptionType>
                  <RenewStatus>ManualRenewal</RenewStatus>
                  <InstanceID>dbaudit-cn-****</InstanceID>
                  <ProductCode>dbaudit</ProductCode>
                  <CreateTime>2020-09-08T16:00:00Z</CreateTime>
                  <OwnerId>181****</OwnerId>
                  <EndTime>2020-11-07T16:00:00Z</EndTime>
                  <Seller>26888</Seller>
            </InstanceList>
            <InstanceList>
                  <Status>Creating</Status>
                  <SubStatus>Normal</SubStatus>
                  <SubscriptionType>Subscription</SubscriptionType>
                  <RenewStatus>ManualRenewal</RenewStatus>
                  <InstanceID>dbaudit-cn-****</InstanceID>
                  <ProductCode>dbaudit</ProductCode>
                  <CreateTime>2020-09-08T16:00:00Z</CreateTime>
                  <OwnerId>181****</OwnerId>
                  <EndTime>2020-11-07T16:00:00Z</EndTime>
                  <Seller>26888</Seller>
            </InstanceList>
      </Data>
      <Message>Successful!</Message>
      <RequestId>C7C15585-8349-4C62-BEE4-5A391841B9BE</RequestId>
      <Success>true</Success>
      <Code>Success</Code>
</QueryAvailableInstancesResponse>
```

`JSON` 格式

```
{
    "Data": {
        "TotalCount": 51,
        "PageSize": 20,
        "PageNum": 1,
        "InstanceList": [
            {
                "Status": "Creating",
                "SubStatus": "Normal",
                "SubscriptionType": "Subscription",
                "RenewStatus": "ManualRenewal",
                "InstanceID": "dbaudit-cn-****",
                "ProductCode": "dbaudit",
                "CreateTime": "2020-09-08T16:00:00Z",
                "OwnerId": "181****",
                "EndTime": "2020-11-07T16:00:00Z",
                "Seller": 26888
            },
            {
                "Status": "Creating",
                "SubStatus": "Normal",
                "SubscriptionType": "Subscription",
                "RenewStatus": "ManualRenewal",
                "InstanceID": "dbaudit-cn-****",
                "ProductCode": "dbaudit",
                "CreateTime": "2020-09-08T16:00:00Z",
                "OwnerId": "181****",
                "EndTime": "2020-11-07T16:00:00Z",
                "Seller": 26888
            }
        ]
    },
    "Message": "Successful!",
    "RequestId": "C7C15585-8349-4C62-BEE4-5A391841B9BE",
    "Success": true,
    "Code": "Success"
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/BssOpenApi)查看更多错误码。

