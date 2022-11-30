# 查询API版本列表信息<a name="ListApiVersions"></a>

## 功能介绍

返回ELB当前所有可用的API版本。

## 调试<a name="atuogenerate_1"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=ELB&api=ListApiVersions)中调试该接口，支持自动认证鉴权。API Explorer可以自动生成SDK代码示例，并提供SDK代码示例调试功能。

## URI

GET /versions

## 请求参数

无

## 响应参数

**状态码： 200**

**表 1**  响应Body参数

<a name="response_ListApiVersionsResponseBody"></a>
<table><thead align="left"><tr><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p>描述</p>
</th>
</tr>
</thead>
<tbody><tr><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p>versions</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p>Array of <a href="#response_ApiVersionInfo">ApiVersionInfo</a> objects</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p>可用API版本列表。</p>
</td>
</tr>
</tbody>
</table>

**表 2**  ApiVersionInfo

<a name="response_ApiVersionInfo"></a>
<table><thead align="left"><tr><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p>描述</p>
</th>
</tr>
</thead>
<tbody><tr><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p>API版本号。</p>
<p>取值：由高到低版本分别为v3，v2，v2.0。</p>
</td>
</tr>
<tr><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p>status</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p>API版本的状态。</p>
<p>取值：</p>
<ul><li><p>CURRENT：当前版本。</p>
</li><li><p>STABLE：稳定版本。</p>
</li><li><p>DEPRECATED：废弃版本。</p>
</li></ul>
<p>说明： 所有支持的API版本中最高版状态为CURRENT，其他版本状态为STABLE。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例

查询API版本列表信息

```
GET https://{ELB_Endpoint}/versions
```

## 响应示例

**状态码： 200**

操作正常返回。

```
{
  "versions" : [ {
    "id" : "v3",
    "status" : "CURRENT"
  }, {
    "id" : "v2",
    "status" : "STABLE"
  }, {
    "id" : "v2.0",
    "status" : "STABLE"
  } ]
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

