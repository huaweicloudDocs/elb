# 计算预占IP数<a name="CountPreoccupyIpNum"></a>

## 功能介绍

计算以下几种场景的预占用IP数量：

-   计算创建LB的第一个七层监听器后总占用IP数量： 传入loadbalancer\_id、l7\_flavor\_id为空、ip\_target\_enable不传或为false。

-   计算LB规格变更或开启跨VPC后总占用IP数量： 传入参数loadbalancer\_id，及l7\_flavor\_id不为空或ip\_target\_enable为true。

-   计算创建LB所需IP数量：传入参数availability\_zone\_id， 及可选参数l7\_flavor\_id、ip\_target\_enable、ip\_version，不能传loadbalancer\_id。


说明：

-   计算出来的预占IP数大于等于最终实际占用的IP数。

-   总占用IP数量，即整个LB所占用的IP数量。


## 调试<a name="atuogenerate_1"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=ELB&api=CountPreoccupyIpNum)中调试该接口，支持自动认证鉴权。API Explorer可以自动生成SDK代码示例，并提供SDK代码示例调试功能。

## URI

GET /v3/\{project\_id\}/elb/preoccupy-ip-num

**表 1**  路径参数

<table><thead align="left"><tr><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.2"><p>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="40%" id="mcps1.2.5.1.4"><p>描述</p>
</th>
</tr>
</thead>
<tbody><tr><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p>String</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.4 "><p>所属项目id。</p>
</td>
</tr>
</tbody>
</table>

**表 2**  Query参数

<table><thead align="left"><tr><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.2"><p>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="40%" id="mcps1.2.5.1.4"><p>描述</p>
</th>
</tr>
</thead>
<tbody><tr><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p>l7_flavor_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p>String</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.4 "><p>负载均衡器七层规格的ID。传入该字段表示计算创建该规格的LB，或变更LB的原七层规格到该规格所需要的预占IP。</p>
<p>适用场景：创建负LB，变更LB规格。</p>
</td>
</tr>
<tr><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p>ip_target_enable</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.4 "><p>是否开启跨VPC转发。</p>
<p>取值true表示计算创建或变更为开启跨VPC转发的LB的预占IP。</p>
<p>取值false表示计算创建或变更为不开启跨VPC转发的LB的预占IP。不传等价false。</p>
<p>适用场景：创建LB，变更LB规格。</p>
</td>
</tr>
<tr><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p>ip_version</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.4 "><p>负载均衡器IP地址类型，取值4，6 。</p>
<p>取值4表示计算创建支持IPv4地址的LB的预占IP。</p>
<p>取值6表示计算创建支持IPv6地址的LB的预占IP。</p>
<p>适用场景：创建LB。</p>
</td>
</tr>
<tr><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p>loadbalancer_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p>String</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.4 "><p>负载均衡器ID。计算LB规格变更或创建LB中的第一个七层监听器的预占IP。</p>
<p>适用场景：变更LB规格，创建LB中的第一个七层监听器。</p>
</td>
</tr>
<tr><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p>availability_zone_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p>Array</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.4 "><p>计算创建AZ列表为availability_zone_id的负载局衡器实例的预占IP。</p>
<p>适用场景：创建LB。</p>
<p>使用说明：传入loadbalancer_id时，该参数无效。</p>
</td>
</tr>
</tbody>
</table>

## 请求参数

**表 3**  请求Header参数

<a name="HeaderParameter"></a>
<table><thead align="left"><tr><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.2"><p>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="40%" id="mcps1.2.5.1.4"><p>描述</p>
</th>
</tr>
</thead>
<tbody><tr><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p>X-Auth-Token</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p>String</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.4 "><p>IAM鉴权Token。</p>
</td>
</tr>
</tbody>
</table>

## 响应参数

**状态码： 200**

**表 4**  响应Body参数

<a name="response_CountPreoccupyIpNumResponseBody"></a>
<table><thead align="left"><tr><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p>描述</p>
</th>
</tr>
</thead>
<tbody><tr><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p>preoccupy_ip</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p><a href="#response_PreoccupyIp">PreoccupyIp</a> object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p>预占IP信息</p>
</td>
</tr>
<tr><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p>request_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p>请求ID。</p>
<p>注：自动生成 。</p>
</td>
</tr>
</tbody>
</table>

**表 5**  PreoccupyIp

<a name="response_PreoccupyIp"></a>
<table><thead align="left"><tr><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p>描述</p>
</th>
</tr>
</thead>
<tbody><tr><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p>total</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p>预占IP总数</p>
</td>
</tr>
</tbody>
</table>

## 请求示例

-   查询变更LB的七层规格需要预占的ip数

    ```
    https://{ELB_Endpoint}/v3/060576782980d5762f9ec014dd2f1148/elb/preoccupy-ip-num?loadbalancer_id=aff4fc31-d635-4f59-a862-edadf32e407d&l7_flavor_id=0051bc4c-a562-4b7c-953b-a250b51d992b
    
    {
      "preoccupy_ip" : {
        "total" : 6
      },
      "request_id" : "8844e9a0-6a2d-44b7-aad9-15a7f75e4059"
    }
    ```

-   查询创建一个双az且开启跨VPC的LB需要预占的IP数

    ```
    GET /v3/{project_id}/elb/preoccupy-ip-num?l7_flavor_id=8278944d-f92c-4393-82b2-6fb9cc1d7e53&availability_zone_id=az1&availability_zone_id=az2&ip_target_enable=true
    
    {
      "preoccupy_ip" : {
        "total" : 20
      },
      "request_id" : "63388ec8-fa3c-4c99-b9c8-d2c83b2a9a68"
    }
    ```

-   查询指定LB中创建第一个7层监听器所需预占的IP数

    ```
    GET /v3/{project_id}/elb/preoccupy-ip-num?loadbalancer_id=aff4fc31-d635-4f59-a862-edadf32e407d
    
    {
      "preoccupy_ip" : {
        "total" : 2
      },
      "request_id" : "febfce48-318d-45ba-a9d9-855462123f3b"
    }
    ```


## 响应示例

**状态码： 200**

操作正常返回。

```
{
  "preoccupy_ip" : {
    "total" : 20
  },
  "request_id" : "63388ec8-fa3c-4c99-b9c8-d2c83b2a9a68"
}
```

## 状态码

<a name="status_code"></a>
<table><thead align="left"><tr><th class="cellrowborder" valign="top" width="15%" id="mcps1.1.3.1.1"><p>状态码 </p>
</th>
<th class="cellrowborder" valign="top" width="85%" id="mcps1.1.3.1.2"><p>描述</p>
</th>
</tr>
</thead>
<tbody><tr><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p>200</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p>操作正常返回。</p>
</td>
</tr>
</tbody>
</table>

## 错误码

请参见[错误码](错误码.md)。

