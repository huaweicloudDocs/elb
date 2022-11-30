# 删除SSL证书<a name="elb_zq_zs_0005"></a>

## 功能介绍<a name="zh-cn_topic_0085859920_section2499709175535"></a>

删除指定的SSL证书。

## 接口约束<a name="zh-cn_topic_0085859920_section35450812175535"></a>

如果待删除证书被监听器使用，则该证书不允许被删除，同时系统会返回409响应。

## URI<a name="zh-cn_topic_0085859920_section64362641175535"></a>

DELETE /v2.0/lbaas/certificates/\{certificate\_id\}

**表 1**  参数说明

<a name="table76017424715"></a>
<table><thead align="left"><tr id="row1462910423715"><th class="cellrowborder" valign="top" width="21.42785721427857%" id="mcps1.2.5.1.1"><p id="p862914421178"><a name="p862914421178"></a><a name="p862914421178"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="21.42785721427857%" id="mcps1.2.5.1.2"><p id="p62271176316"><a name="p62271176316"></a><a name="p62271176316"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="14.288571142885711%" id="mcps1.2.5.1.3"><p id="p362914421274"><a name="p362914421274"></a><a name="p362914421274"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="42.85571442855714%" id="mcps1.2.5.1.4"><p id="p126291424718"><a name="p126291424718"></a><a name="p126291424718"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row362914421378"><td class="cellrowborder" valign="top" width="21.42785721427857%" headers="mcps1.2.5.1.1 "><p id="p46298424717"><a name="p46298424717"></a><a name="p46298424717"></a>certificate_id</p>
</td>
<td class="cellrowborder" valign="top" width="21.42785721427857%" headers="mcps1.2.5.1.2 "><p id="p36291421273"><a name="p36291421273"></a><a name="p36291421273"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="14.288571142885711%" headers="mcps1.2.5.1.3 "><p id="p126292426712"><a name="p126292426712"></a><a name="p126292426712"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="42.85571442855714%" headers="mcps1.2.5.1.4 "><p id="p1762911427714"><a name="p1762911427714"></a><a name="p1762911427714"></a>SSL证书ID。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="zh-cn_topic_0085859920_section124704175535"></a>

-   请求参数

    无


## 响应消息<a name="zh-cn_topic_0085859920_section14041166175535"></a>

-   响应参数

    无


## 请求示例<a name="section593018453355"></a>

-   请求样例1 删除SSL证书

    ```
    DELETE https://{Endpoint}/v2.0/lbaas/certificates/23ef9aad4ecb463580476d324a6c71af
    ```


## 响应示例<a name="section564371811435"></a>

-   响应样例1

    无


## 返回码<a name="zh-cn_topic_0049139664_section36936567"></a>

请参见[状态码](状态码.md)。

