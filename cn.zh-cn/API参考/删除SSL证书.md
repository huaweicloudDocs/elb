# 删除SSL证书<a name="elb_qy_zs_0005"></a>

## 功能介绍<a name="elb_zq_zs_0005_zh-cn_topic_0085859920_section2499709175535"></a>

删除SSL证书。

## 接口约束<a name="elb_zq_zs_0005_zh-cn_topic_0085859920_section35450812175535"></a>

如果待删除证书被监听器使用，则该证书不允许被删除，同时系统会返回409响应。

## 调试<a name="section3683205810399"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=ELB&api=DeleteCertificate&version=v2)中直接运行调试该接口。

## URI<a name="elb_zq_zs_0005_zh-cn_topic_0085859920_section64362641175535"></a>

DELETE /v2/\{project\_id\}/elb/certificates/\{certificate\_id\}

**表 1**  参数说明

<a name="elb_zq_zs_0005_table76017424715"></a>
<table><thead align="left"><tr id="elb_zq_zs_0005_row1462910423715"><th class="cellrowborder" valign="top" width="24.717528247175284%" id="mcps1.2.5.1.1"><p id="elb_zq_zs_0005_p862914421178"><a name="elb_zq_zs_0005_p862914421178"></a><a name="elb_zq_zs_0005_p862914421178"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="16.478352164783523%" id="mcps1.2.5.1.2"><p id="elb_zq_zs_0005_p362914421274"><a name="elb_zq_zs_0005_p362914421274"></a><a name="elb_zq_zs_0005_p362914421274"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="9.37906209379062%" id="mcps1.2.5.1.3"><p id="elb_zq_zs_0005_p36291342170"><a name="elb_zq_zs_0005_p36291342170"></a><a name="elb_zq_zs_0005_p36291342170"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="49.42505749425058%" id="mcps1.2.5.1.4"><p id="elb_zq_zs_0005_p126291424718"><a name="elb_zq_zs_0005_p126291424718"></a><a name="elb_zq_zs_0005_p126291424718"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row0913563569"><td class="cellrowborder" valign="top" width="24.717528247175284%" headers="mcps1.2.5.1.1 "><p id="p1399071505415"><a name="p1399071505415"></a><a name="p1399071505415"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="16.478352164783523%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0020100158_p557643211309"><a name="zh-cn_topic_0020100158_p557643211309"></a><a name="zh-cn_topic_0020100158_p557643211309"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="9.37906209379062%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0020100158_p6162677511304"><a name="zh-cn_topic_0020100158_p6162677511304"></a><a name="zh-cn_topic_0020100158_p6162677511304"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="49.42505749425058%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0020100158_p35845144113012"><a name="zh-cn_topic_0020100158_p35845144113012"></a><a name="zh-cn_topic_0020100158_p35845144113012"></a>操作用户的项目ID。</p>
<p id="p8222164914610"><a name="p8222164914610"></a><a name="p8222164914610"></a>获取方法详见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
<tr id="elb_zq_zs_0005_row362914421378"><td class="cellrowborder" valign="top" width="24.717528247175284%" headers="mcps1.2.5.1.1 "><p id="elb_zq_zs_0005_p46298424717"><a name="elb_zq_zs_0005_p46298424717"></a><a name="elb_zq_zs_0005_p46298424717"></a>certificate_id</p>
</td>
<td class="cellrowborder" valign="top" width="16.478352164783523%" headers="mcps1.2.5.1.2 "><p id="elb_zq_zs_0005_p126292426712"><a name="elb_zq_zs_0005_p126292426712"></a><a name="elb_zq_zs_0005_p126292426712"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="9.37906209379062%" headers="mcps1.2.5.1.3 "><p id="p93751813122320"><a name="p93751813122320"></a><a name="p93751813122320"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="49.42505749425058%" headers="mcps1.2.5.1.4 "><p id="elb_zq_zs_0005_p1762911427714"><a name="elb_zq_zs_0005_p1762911427714"></a><a name="elb_zq_zs_0005_p1762911427714"></a>证书id。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="elb_zq_zs_0005_zh-cn_topic_0085859920_section124704175535"></a>

无

## 响应消息<a name="elb_zq_zs_0005_zh-cn_topic_0085859920_section14041166175535"></a>

无

## 请求示例<a name="section83946335311"></a>

-   请求样例 删除SSL证书

    ```
    DELETE https://{Endpoint}/v2/a31d2bdcf7604c0faaddb058e1e08819/elb/certificates/23ef9aad4ecb463580476d324a6c71af
    ```


## 响应示例<a name="section87401547113015"></a>

-   响应样例

    无


## 返回码<a name="elb_zq_zs_0005_zh-cn_topic_0049139664_section36936567"></a>

请参见[状态码](状态码.md)。

