# 更新SSL证书<a name="elb_qy_zs_0004"></a>

## 功能介绍<a name="elb_zq_zs_0004_zh-cn_topic_0085859919_section48870738174959"></a>

更新SSL证书。

## 调试<a name="section3683205810399"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=ELB&api=UpdateCertificate&version=v2)中直接运行调试该接口。

## URI<a name="elb_zq_zs_0004_zh-cn_topic_0085859919_section9730439174959"></a>

PUT /v2/\{project\_id\}/elb/certificates/\{certificate\_id\}

**表 1**  参数说明

<a name="elb_zq_zs_0004_table1664412216716"></a>
<table><thead align="left"><tr id="elb_zq_zs_0004_row268472119719"><th class="cellrowborder" valign="top" width="24.717528247175284%" id="mcps1.2.5.1.1"><p id="elb_zq_zs_0004_p196855212718"><a name="elb_zq_zs_0004_p196855212718"></a><a name="elb_zq_zs_0004_p196855212718"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="16.478352164783523%" id="mcps1.2.5.1.2"><p id="elb_zq_zs_0004_p2068552113716"><a name="elb_zq_zs_0004_p2068552113716"></a><a name="elb_zq_zs_0004_p2068552113716"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="9.37906209379062%" id="mcps1.2.5.1.3"><p id="elb_zq_zs_0004_p26859217717"><a name="elb_zq_zs_0004_p26859217717"></a><a name="elb_zq_zs_0004_p26859217717"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="49.42505749425058%" id="mcps1.2.5.1.4"><p id="elb_zq_zs_0004_p1268562113717"><a name="elb_zq_zs_0004_p1268562113717"></a><a name="elb_zq_zs_0004_p1268562113717"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row16990135613554"><td class="cellrowborder" valign="top" width="24.717528247175284%" headers="mcps1.2.5.1.1 "><p id="p1399071505415"><a name="p1399071505415"></a><a name="p1399071505415"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="16.478352164783523%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0020100158_p557643211309"><a name="zh-cn_topic_0020100158_p557643211309"></a><a name="zh-cn_topic_0020100158_p557643211309"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="9.37906209379062%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0020100158_p6162677511304"><a name="zh-cn_topic_0020100158_p6162677511304"></a><a name="zh-cn_topic_0020100158_p6162677511304"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="49.42505749425058%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0020100158_p35845144113012"><a name="zh-cn_topic_0020100158_p35845144113012"></a><a name="zh-cn_topic_0020100158_p35845144113012"></a>操作用户的项目ID。</p>
<p id="p8222164914610"><a name="p8222164914610"></a><a name="p8222164914610"></a>获取方法详见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
<tr id="elb_zq_zs_0004_row10685122111711"><td class="cellrowborder" valign="top" width="24.717528247175284%" headers="mcps1.2.5.1.1 "><p id="elb_zq_zs_0004_p14685821871"><a name="elb_zq_zs_0004_p14685821871"></a><a name="elb_zq_zs_0004_p14685821871"></a>certificate_id</p>
</td>
<td class="cellrowborder" valign="top" width="16.478352164783523%" headers="mcps1.2.5.1.2 "><p id="elb_zq_zs_0004_p368519213715"><a name="elb_zq_zs_0004_p368519213715"></a><a name="elb_zq_zs_0004_p368519213715"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="9.37906209379062%" headers="mcps1.2.5.1.3 "><p id="elb_zq_zs_0004_p5685121778"><a name="elb_zq_zs_0004_p5685121778"></a><a name="elb_zq_zs_0004_p5685121778"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="49.42505749425058%" headers="mcps1.2.5.1.4 "><p id="elb_zq_zs_0004_p1368515211714"><a name="elb_zq_zs_0004_p1368515211714"></a><a name="elb_zq_zs_0004_p1368515211714"></a>证书id。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="elb_zq_zs_0004_zh-cn_topic_0085859919_section38626650174959"></a>

**表 2**  请求参数

<a name="elb_zq_zs_0004_zh-cn_topic_0085859919_table62215390174959"></a>
<table><thead align="left"><tr id="elb_zq_zs_0004_zh-cn_topic_0085859919_row35879330174959"><th class="cellrowborder" valign="top" width="21.36%" id="mcps1.2.5.1.1"><p id="elb_zq_zs_0004_zh-cn_topic_0085859919_p52201676174959"><a name="elb_zq_zs_0004_zh-cn_topic_0085859919_p52201676174959"></a><a name="elb_zq_zs_0004_zh-cn_topic_0085859919_p52201676174959"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="11.110000000000001%" id="mcps1.2.5.1.2"><p id="elb_zq_zs_0004_zh-cn_topic_0085859919_p5280357174959"><a name="elb_zq_zs_0004_zh-cn_topic_0085859919_p5280357174959"></a><a name="elb_zq_zs_0004_zh-cn_topic_0085859919_p5280357174959"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="18.4%" id="mcps1.2.5.1.3"><p id="elb_zq_zs_0004_zh-cn_topic_0085859919_p2598936174959"><a name="elb_zq_zs_0004_zh-cn_topic_0085859919_p2598936174959"></a><a name="elb_zq_zs_0004_zh-cn_topic_0085859919_p2598936174959"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="49.13%" id="mcps1.2.5.1.4"><p id="elb_zq_zs_0004_zh-cn_topic_0085859919_p46936095174959"><a name="elb_zq_zs_0004_zh-cn_topic_0085859919_p46936095174959"></a><a name="elb_zq_zs_0004_zh-cn_topic_0085859919_p46936095174959"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="elb_zq_zs_0004_row48584188318"><td class="cellrowborder" valign="top" width="21.36%" headers="mcps1.2.5.1.1 "><p id="elb_zq_zs_0004_p785841873113"><a name="elb_zq_zs_0004_p785841873113"></a><a name="elb_zq_zs_0004_p785841873113"></a>admin_state_up</p>
</td>
<td class="cellrowborder" valign="top" width="11.110000000000001%" headers="mcps1.2.5.1.2 "><p id="elb_zq_zs_0004_p7858131818319"><a name="elb_zq_zs_0004_p7858131818319"></a><a name="elb_zq_zs_0004_p7858131818319"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="18.4%" headers="mcps1.2.5.1.3 "><p id="elb_zq_zs_0004_p15858218103114"><a name="elb_zq_zs_0004_p15858218103114"></a><a name="elb_zq_zs_0004_p15858218103114"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="49.13%" headers="mcps1.2.5.1.4 "><p id="elb_zq_zs_0004_p189741017613"><a name="elb_zq_zs_0004_p189741017613"></a><a name="elb_zq_zs_0004_p189741017613"></a>SSL证书的管理状态；</p>
<p id="p1685165224811"><a name="p1685165224811"></a><a name="p1685165224811"></a>该字段为预留字段，暂未启用。默认为true。</p>
</td>
</tr>
<tr id="elb_zq_zs_0004_zh-cn_topic_0085859919_row29288134174959"><td class="cellrowborder" valign="top" width="21.36%" headers="mcps1.2.5.1.1 "><p id="elb_zq_zs_0004_zh-cn_topic_0085859919_p31165543174959"><a name="elb_zq_zs_0004_zh-cn_topic_0085859919_p31165543174959"></a><a name="elb_zq_zs_0004_zh-cn_topic_0085859919_p31165543174959"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="11.110000000000001%" headers="mcps1.2.5.1.2 "><p id="elb_zq_zs_0004_zh-cn_topic_0085859919_p34889889174959"><a name="elb_zq_zs_0004_zh-cn_topic_0085859919_p34889889174959"></a><a name="elb_zq_zs_0004_zh-cn_topic_0085859919_p34889889174959"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="18.4%" headers="mcps1.2.5.1.3 "><p id="elb_zq_zs_0004_zh-cn_topic_0085859919_p53796641174959"><a name="elb_zq_zs_0004_zh-cn_topic_0085859919_p53796641174959"></a><a name="elb_zq_zs_0004_zh-cn_topic_0085859919_p53796641174959"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="49.13%" headers="mcps1.2.5.1.4 "><p id="elb_zq_zs_0004_p034963734312"><a name="elb_zq_zs_0004_p034963734312"></a><a name="elb_zq_zs_0004_p034963734312"></a>SSL证书的名称。</p>
<p id="elb_zq_zs_0004_p1264211013318"><a name="elb_zq_zs_0004_p1264211013318"></a><a name="elb_zq_zs_0004_p1264211013318"></a>支持的最大字符长度：255</p>
</td>
</tr>
<tr id="elb_zq_zs_0004_zh-cn_topic_0085859919_row12347817174959"><td class="cellrowborder" valign="top" width="21.36%" headers="mcps1.2.5.1.1 "><p id="elb_zq_zs_0004_zh-cn_topic_0085859919_p9569533174959"><a name="elb_zq_zs_0004_zh-cn_topic_0085859919_p9569533174959"></a><a name="elb_zq_zs_0004_zh-cn_topic_0085859919_p9569533174959"></a>description</p>
</td>
<td class="cellrowborder" valign="top" width="11.110000000000001%" headers="mcps1.2.5.1.2 "><p id="elb_zq_zs_0004_zh-cn_topic_0085859919_p29495170174959"><a name="elb_zq_zs_0004_zh-cn_topic_0085859919_p29495170174959"></a><a name="elb_zq_zs_0004_zh-cn_topic_0085859919_p29495170174959"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="18.4%" headers="mcps1.2.5.1.3 "><p id="elb_zq_zs_0004_zh-cn_topic_0085859919_p59414857174959"><a name="elb_zq_zs_0004_zh-cn_topic_0085859919_p59414857174959"></a><a name="elb_zq_zs_0004_zh-cn_topic_0085859919_p59414857174959"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="49.13%" headers="mcps1.2.5.1.4 "><p id="elb_zq_zs_0004_p636474910435"><a name="elb_zq_zs_0004_p636474910435"></a><a name="elb_zq_zs_0004_p636474910435"></a>SSL证书的描述信息。</p>
<p id="elb_zq_zs_0004_p1442761811405"><a name="elb_zq_zs_0004_p1442761811405"></a><a name="elb_zq_zs_0004_p1442761811405"></a>支持的最大字符长度：255</p>
</td>
</tr>
<tr id="elb_zq_zs_0004_zh-cn_topic_0085859919_row25521469174959"><td class="cellrowborder" valign="top" width="21.36%" headers="mcps1.2.5.1.1 "><p id="elb_zq_zs_0004_zh-cn_topic_0085859919_p47787672174959"><a name="elb_zq_zs_0004_zh-cn_topic_0085859919_p47787672174959"></a><a name="elb_zq_zs_0004_zh-cn_topic_0085859919_p47787672174959"></a>domain</p>
</td>
<td class="cellrowborder" valign="top" width="11.110000000000001%" headers="mcps1.2.5.1.2 "><p id="elb_zq_zs_0004_zh-cn_topic_0085859919_p21932410174959"><a name="elb_zq_zs_0004_zh-cn_topic_0085859919_p21932410174959"></a><a name="elb_zq_zs_0004_zh-cn_topic_0085859919_p21932410174959"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="18.4%" headers="mcps1.2.5.1.3 "><p id="elb_zq_zs_0004_zh-cn_topic_0085859919_p2180173174959"><a name="elb_zq_zs_0004_zh-cn_topic_0085859919_p2180173174959"></a><a name="elb_zq_zs_0004_zh-cn_topic_0085859919_p2180173174959"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="49.13%" headers="mcps1.2.5.1.4 "><p id="elb_zq_zs_0004_p14884193271218"><a name="elb_zq_zs_0004_p14884193271218"></a><a name="elb_zq_zs_0004_p14884193271218"></a>服务端证书所签的域名。默认值：null；</p>
<p id="elb_zq_zs_0004_p15972220174018"><a name="elb_zq_zs_0004_p15972220174018"></a><a name="elb_zq_zs_0004_p15972220174018"></a>支持的最大字符长度：100</p>
<p id="elb_zq_zs_0004_p16305043131216"><a name="elb_zq_zs_0004_p16305043131216"></a><a name="elb_zq_zs_0004_p16305043131216"></a>取值范围：</p>
<a name="elb_zq_zs_0004_ul128048293014"></a><a name="elb_zq_zs_0004_ul128048293014"></a><ul id="elb_zq_zs_0004_ul128048293014"><li>普通域名由若干字符串组成，总长度为0-100，字符串间以"."分割，单个字符串长度不超过63个字符，只能包含英文字母、数字或"-"，且必须以字母或数字开头和结尾。</li><li>泛域名在普通域名的基础上仅允许首字母为"*"。该字段仅type为server时有效。</li></ul>
<div class="note" id="elb_zq_zs_0004_zh-cn_topic_0085859918_note3391807017458"><a name="elb_zq_zs_0004_zh-cn_topic_0085859918_note3391807017458"></a><a name="elb_zq_zs_0004_zh-cn_topic_0085859918_note3391807017458"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="elb_zq_zs_0004_zh-cn_topic_0085859918_p4119083617458"><a name="elb_zq_zs_0004_zh-cn_topic_0085859918_p4119083617458"></a><a name="elb_zq_zs_0004_zh-cn_topic_0085859918_p4119083617458"></a>该字段仅type为server时有效。</p>
</div></div>
</td>
</tr>
<tr id="elb_zq_zs_0004_zh-cn_topic_0085859919_row10022251174959"><td class="cellrowborder" valign="top" width="21.36%" headers="mcps1.2.5.1.1 "><p id="elb_zq_zs_0004_zh-cn_topic_0085859919_p57736676174959"><a name="elb_zq_zs_0004_zh-cn_topic_0085859919_p57736676174959"></a><a name="elb_zq_zs_0004_zh-cn_topic_0085859919_p57736676174959"></a>private_key</p>
</td>
<td class="cellrowborder" valign="top" width="11.110000000000001%" headers="mcps1.2.5.1.2 "><p id="elb_zq_zs_0004_zh-cn_topic_0085859919_p31369944174959"><a name="elb_zq_zs_0004_zh-cn_topic_0085859919_p31369944174959"></a><a name="elb_zq_zs_0004_zh-cn_topic_0085859919_p31369944174959"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="18.4%" headers="mcps1.2.5.1.3 "><p id="elb_zq_zs_0004_zh-cn_topic_0085859919_p27614681174959"><a name="elb_zq_zs_0004_zh-cn_topic_0085859919_p27614681174959"></a><a name="elb_zq_zs_0004_zh-cn_topic_0085859919_p27614681174959"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="49.13%" headers="mcps1.2.5.1.4 "><p id="p1717817813215"><a name="p1717817813215"></a><a name="p1717817813215"></a>HTTPS协议使用的私钥，PEM编码格式。</p>
<a name="ul71783818210"></a><a name="ul71783818210"></a><ul id="ul71783818210"><li>当type为client时，该参数被忽略，不影响证书的创建和使用。且若不符合格式，则该字段会设置为空。</li><li>当type为server时，该字段必须符合格式要求，且私钥必须是有效的，否则会报错。</li></ul>
</td>
</tr>
<tr id="elb_zq_zs_0004_zh-cn_topic_0085859919_row18969603174959"><td class="cellrowborder" valign="top" width="21.36%" headers="mcps1.2.5.1.1 "><p id="elb_zq_zs_0004_zh-cn_topic_0085859919_p44096056174959"><a name="elb_zq_zs_0004_zh-cn_topic_0085859919_p44096056174959"></a><a name="elb_zq_zs_0004_zh-cn_topic_0085859919_p44096056174959"></a>certificate</p>
</td>
<td class="cellrowborder" valign="top" width="11.110000000000001%" headers="mcps1.2.5.1.2 "><p id="elb_zq_zs_0004_zh-cn_topic_0085859919_p3351721174959"><a name="elb_zq_zs_0004_zh-cn_topic_0085859919_p3351721174959"></a><a name="elb_zq_zs_0004_zh-cn_topic_0085859919_p3351721174959"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="18.4%" headers="mcps1.2.5.1.3 "><p id="elb_zq_zs_0004_zh-cn_topic_0085859919_p51899034174959"><a name="elb_zq_zs_0004_zh-cn_topic_0085859919_p51899034174959"></a><a name="elb_zq_zs_0004_zh-cn_topic_0085859919_p51899034174959"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="49.13%" headers="mcps1.2.5.1.4 "><p id="elb_zq_zs_0004_p56851334121510"><a name="elb_zq_zs_0004_p56851334121510"></a><a name="elb_zq_zs_0004_p56851334121510"></a>服务端公有密钥证书或者用于认证客户端证书的CA证书，由type字段区分。</p>
<p id="elb_zq_zs_0004_p8493444202513"><a name="elb_zq_zs_0004_p8493444202513"></a><a name="elb_zq_zs_0004_p8493444202513"></a>格式：证书为PEM格式。</p>
</td>
</tr>
</tbody>
</table>

## 响应消息<a name="elb_zq_zs_0004_zh-cn_topic_0085859919_section31160971174959"></a>

**表 3**  响应参数

<a name="elb_zq_zs_0004_zh-cn_topic_0085859919_table55952037174959"></a>
<table><thead align="left"><tr id="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_row11412198173534"><th class="cellrowborder" valign="top" width="21.099999999999998%" id="mcps1.2.4.1.1"><p id="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p66723761173534"><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p66723761173534"></a><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p66723761173534"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="18.9%" id="mcps1.2.4.1.2"><p id="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p31496314173534"><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p31496314173534"></a><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p31496314173534"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p5981838173534"><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p5981838173534"></a><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p5981838173534"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_row20744965173534"><td class="cellrowborder" valign="top" width="21.099999999999998%" headers="mcps1.2.4.1.1 "><p id="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p21724371173534"><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p21724371173534"></a><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p21724371173534"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="18.9%" headers="mcps1.2.4.1.2 "><p id="elb_qy_zs_0001_elb_zq_zs_0001_p11149359102718"><a name="elb_qy_zs_0001_elb_zq_zs_0001_p11149359102718"></a><a name="elb_qy_zs_0001_elb_zq_zs_0001_p11149359102718"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p4585726173534"><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p4585726173534"></a><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p4585726173534"></a>SSL证书ID。</p>
</td>
</tr>
<tr id="elb_qy_zs_0001_elb_zq_zs_0001_row1313561214274"><td class="cellrowborder" valign="top" width="21.099999999999998%" headers="mcps1.2.4.1.1 "><p id="elb_qy_zs_0001_elb_zq_zs_0001_p1913501218276"><a name="elb_qy_zs_0001_elb_zq_zs_0001_p1913501218276"></a><a name="elb_qy_zs_0001_elb_zq_zs_0001_p1913501218276"></a>tenant_id</p>
</td>
<td class="cellrowborder" valign="top" width="18.9%" headers="mcps1.2.4.1.2 "><p id="elb_qy_zs_0001_elb_zq_zs_0001_p16135161202717"><a name="elb_qy_zs_0001_elb_zq_zs_0001_p16135161202717"></a><a name="elb_qy_zs_0001_elb_zq_zs_0001_p16135161202717"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="elb_qy_zs_0001_elb_zq_zs_0001_p1413510125272"><a name="elb_qy_zs_0001_elb_zq_zs_0001_p1413510125272"></a><a name="elb_qy_zs_0001_elb_zq_zs_0001_p1413510125272"></a>SSL证书所在的项目ID。</p>
<p id="elb_qy_zs_0001_elb_zq_zs_0001_p12961124943614"><a name="elb_qy_zs_0001_elb_zq_zs_0001_p12961124943614"></a><a name="elb_qy_zs_0001_elb_zq_zs_0001_p12961124943614"></a>支持的最大字符长度：255</p>
</td>
</tr>
<tr id="elb_qy_zs_0001_elb_zq_zs_0001_row7916373278"><td class="cellrowborder" valign="top" width="21.099999999999998%" headers="mcps1.2.4.1.1 "><p id="elb_qy_zs_0001_elb_zq_zs_0001_p19161672277"><a name="elb_qy_zs_0001_elb_zq_zs_0001_p19161672277"></a><a name="elb_qy_zs_0001_elb_zq_zs_0001_p19161672277"></a>admin_state_up</p>
</td>
<td class="cellrowborder" valign="top" width="18.9%" headers="mcps1.2.4.1.2 "><p id="elb_qy_zs_0001_elb_zq_zs_0001_p191616732710"><a name="elb_qy_zs_0001_elb_zq_zs_0001_p191616732710"></a><a name="elb_qy_zs_0001_elb_zq_zs_0001_p191616732710"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="elb_qy_zs_0001_elb_zq_zs_0001_p274684451617"><a name="elb_qy_zs_0001_elb_zq_zs_0001_p274684451617"></a><a name="elb_qy_zs_0001_elb_zq_zs_0001_p274684451617"></a>SSL证书的管理状态；</p>
<p id="elb_qy_zs_0001_p81725912819"><a name="elb_qy_zs_0001_p81725912819"></a><a name="elb_qy_zs_0001_p81725912819"></a>该字段为预留字段，暂未启用。取值范围：true/false。</p>
<a name="elb_qy_zs_0001_ul1417218962818"></a><a name="elb_qy_zs_0001_ul1417218962818"></a><ul id="elb_qy_zs_0001_ul1417218962818"><li>true表示开启。</li><li>false表示关闭。</li></ul>
</td>
</tr>
<tr id="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_row29191383173534"><td class="cellrowborder" valign="top" width="21.099999999999998%" headers="mcps1.2.4.1.1 "><p id="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p55607168173534"><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p55607168173534"></a><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p55607168173534"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="18.9%" headers="mcps1.2.4.1.2 "><p id="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p28026059173534"><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p28026059173534"></a><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p28026059173534"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p21173547173534"><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p21173547173534"></a><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p21173547173534"></a>SSL证书名称。</p>
<p id="elb_qy_zs_0001_elb_zq_zs_0001_p18170252113611"><a name="elb_qy_zs_0001_elb_zq_zs_0001_p18170252113611"></a><a name="elb_qy_zs_0001_elb_zq_zs_0001_p18170252113611"></a>支持的最大字符长度：255</p>
</td>
</tr>
<tr id="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_row41991314173534"><td class="cellrowborder" valign="top" width="21.099999999999998%" headers="mcps1.2.4.1.1 "><p id="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p63231950173534"><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p63231950173534"></a><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p63231950173534"></a>description</p>
</td>
<td class="cellrowborder" valign="top" width="18.9%" headers="mcps1.2.4.1.2 "><p id="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p35111452173534"><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p35111452173534"></a><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p35111452173534"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p49236727173534"><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p49236727173534"></a><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p49236727173534"></a>证书描述SSL证书描述。</p>
<p id="elb_qy_zs_0001_elb_zq_zs_0001_p71641548361"><a name="elb_qy_zs_0001_elb_zq_zs_0001_p71641548361"></a><a name="elb_qy_zs_0001_elb_zq_zs_0001_p71641548361"></a>支持的最大字符长度：255</p>
</td>
</tr>
<tr id="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_row27338318173534"><td class="cellrowborder" valign="top" width="21.099999999999998%" headers="mcps1.2.4.1.1 "><p id="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p43711802173534"><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p43711802173534"></a><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p43711802173534"></a>type</p>
</td>
<td class="cellrowborder" valign="top" width="18.9%" headers="mcps1.2.4.1.2 "><p id="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p16661086173534"><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p16661086173534"></a><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p16661086173534"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p47471091173534"><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p47471091173534"></a><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p47471091173534"></a>SSL证书的类型。</p>
<div class="p" id="elb_qy_zs_0001_elb_zq_zs_0001_p9834519174"><a name="elb_qy_zs_0001_elb_zq_zs_0001_p9834519174"></a><a name="elb_qy_zs_0001_elb_zq_zs_0001_p9834519174"></a>取值范围：<a name="elb_qy_zs_0001_elb_zq_zs_0001_ul48343181711"></a><a name="elb_qy_zs_0001_elb_zq_zs_0001_ul48343181711"></a><ul id="elb_qy_zs_0001_elb_zq_zs_0001_ul48343181711"><li>server：服务端证书；</li><li>client：客户端证书；</li></ul>
</div>
</td>
</tr>
<tr id="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_row57368822173534"><td class="cellrowborder" valign="top" width="21.099999999999998%" headers="mcps1.2.4.1.1 "><p id="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p66718031173534"><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p66718031173534"></a><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p66718031173534"></a>domain</p>
</td>
<td class="cellrowborder" valign="top" width="18.9%" headers="mcps1.2.4.1.2 "><p id="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p28969287173534"><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p28969287173534"></a><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p28969287173534"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p52667105173534"><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p52667105173534"></a><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p52667105173534"></a>服务端证书所签域名。</p>
<p id="elb_qy_zs_0001_elb_zq_zs_0001_p7145757123615"><a name="elb_qy_zs_0001_elb_zq_zs_0001_p7145757123615"></a><a name="elb_qy_zs_0001_elb_zq_zs_0001_p7145757123615"></a>支持的最大字符长度：100</p>
</td>
</tr>
<tr id="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_row32267386173534"><td class="cellrowborder" valign="top" width="21.099999999999998%" headers="mcps1.2.4.1.1 "><p id="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p2838320173534"><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p2838320173534"></a><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p2838320173534"></a>private_key</p>
</td>
<td class="cellrowborder" valign="top" width="18.9%" headers="mcps1.2.4.1.2 "><p id="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p43739651173534"><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p43739651173534"></a><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p43739651173534"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p12798312173534"><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p12798312173534"></a><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p12798312173534"></a>PEM格式的服务端私有密钥。</p>
</td>
</tr>
<tr id="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_row329105173534"><td class="cellrowborder" valign="top" width="21.099999999999998%" headers="mcps1.2.4.1.1 "><p id="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p10917956173534"><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p10917956173534"></a><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p10917956173534"></a>certificate</p>
</td>
<td class="cellrowborder" valign="top" width="18.9%" headers="mcps1.2.4.1.2 "><p id="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p50089397173534"><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p50089397173534"></a><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p50089397173534"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p47546713173534"><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p47546713173534"></a><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p47546713173534"></a>PEM格式的服务端公有密钥或者用于认证客户端证书的CA证书，由type字段区分。</p>
</td>
</tr>
<tr id="elb_qy_zs_0001_elb_zq_zs_0001_row5698184112395"><td class="cellrowborder" valign="top" width="21.099999999999998%" headers="mcps1.2.4.1.1 "><p id="elb_qy_zs_0001_elb_zq_zs_0001_p1169816414399"><a name="elb_qy_zs_0001_elb_zq_zs_0001_p1169816414399"></a><a name="elb_qy_zs_0001_elb_zq_zs_0001_p1169816414399"></a>expire_time</p>
</td>
<td class="cellrowborder" valign="top" width="18.9%" headers="mcps1.2.4.1.2 "><p id="elb_qy_zs_0001_elb_zq_zs_0001_p969874112392"><a name="elb_qy_zs_0001_elb_zq_zs_0001_p969874112392"></a><a name="elb_qy_zs_0001_elb_zq_zs_0001_p969874112392"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="elb_qy_zs_0001_elb_zq_zs_0001_p146981141133912"><a name="elb_qy_zs_0001_elb_zq_zs_0001_p146981141133912"></a><a name="elb_qy_zs_0001_elb_zq_zs_0001_p146981141133912"></a>SSL证书的过期时间。</p>
<p id="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0141008271_p52901417154816"><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0141008271_p52901417154816"></a><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0141008271_p52901417154816"></a>格式为UTC时间：YYYY-MM-DDTHH:MM:SS</p>
</td>
</tr>
<tr id="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_row58956881173534"><td class="cellrowborder" valign="top" width="21.099999999999998%" headers="mcps1.2.4.1.1 "><p id="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p28854566173534"><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p28854566173534"></a><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p28854566173534"></a>create_time</p>
</td>
<td class="cellrowborder" valign="top" width="18.9%" headers="mcps1.2.4.1.2 "><p id="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p41288654173534"><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p41288654173534"></a><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p41288654173534"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p14875840173534"><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p14875840173534"></a><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p14875840173534"></a>SSL证书的创建时间。</p>
<p id="elb_qy_zs_0001_elb_zq_zs_0001_p17245855710"><a name="elb_qy_zs_0001_elb_zq_zs_0001_p17245855710"></a><a name="elb_qy_zs_0001_elb_zq_zs_0001_p17245855710"></a>格式为UTC时间：YYYY-MM-DDTHH:MM:SS</p>
</td>
</tr>
<tr id="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_row43957201173534"><td class="cellrowborder" valign="top" width="21.099999999999998%" headers="mcps1.2.4.1.1 "><p id="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p57772843173534"><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p57772843173534"></a><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p57772843173534"></a>update_time</p>
</td>
<td class="cellrowborder" valign="top" width="18.9%" headers="mcps1.2.4.1.2 "><p id="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p43564658173534"><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p43564658173534"></a><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p43564658173534"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p4321549173534"><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p4321549173534"></a><a name="elb_qy_zs_0001_elb_zq_zs_0001_zh-cn_topic_0085859918_p4321549173534"></a>SSL证书的更新时间。</p>
<p id="elb_qy_zs_0001_elb_zq_zs_0001_p53376597572"><a name="elb_qy_zs_0001_elb_zq_zs_0001_p53376597572"></a><a name="elb_qy_zs_0001_elb_zq_zs_0001_p53376597572"></a>格式为UTC时间：YYYY-MM-DDTHH:MM:SS</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="section15515121124716"></a>

-   请求样例1 更新SSL证书

    ```
    PUT https://{Endpoint}/v2/a31d2bdcf7604c0faaddb058e1e08819/elb/certificates/23ef9aad4ecb463580476d324a6c71af 
    
    {
        "certificate": 
    "-----BEGIN CERTIFICATE-----
    \nMIIC4TCCAcmgAwIBAgICEREwDQYJKoZIhvcNAQELBQAwFzEVMBMGA1UEAxMMTXlD
    \nb21wYW55IENBMB4XDTE4MDcwMjEzMjU0N1oXDTQ1MTExNzEzMjU0N1owFDESMBAG
    \nA1UEAwwJbG9jYWxob3N0MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEA
    \n0FQGzi3ucTX+DNud1p/b4XVM6I3rY7+Cfge5GMLDIUXIHXCfCgp19Z3807yNpLF5
    \nU0NqPQZKUrZz3rQeLN9mYiUTJZPutYlFDDbB8CtlgV+eyU9yYJslWx/Bm5kWNPh9
    \n7B9Yu9pbp2u6zDA99IC4ekKD93KuzxlnLmSle4Y3dbYwk0LpMDL6lfCHKt/W7jaS
    \nIAzlsxD+QM6l7QjhWJ+kUx+UkboOISjTe7E9XmDLJR7u8LRAQylYKy4zgnv1tn/K
    \ny09cxLKAFtgoZWQD2FAZJf9F7k1kYNwqITz3CPlLZUUn7yw3nkOOtLMI28IEv0Wy
    \nYd7CMJQkS1NPJBKNOGfR/wIDAQABozowODAhBgNVHREEGjAYggpkb21haW4uY29t
    \nhwQKuUvJhwR/AAABMBMGA1UdJQQMMAoGCCsGAQUFBwMBMA0GCSqGSIb3DQEBCwUA
    \nA4IBAQA8lMQJxaTey7EjXtRLSVlEAMftAQPG6jijNQuvIBQYUDauDT4W2XUZ5wAn
    \njiOyQ83va672K1G9s8n6xlH+xwwdSNnozaKzC87vwSeZKIOdl9I5I98TGKI6OoDa
    \nezmzCwQYtHBMVQ4c7Ml8554Ft1mWSt4dMAK2rzNYjvPRLYlzp1HMnI6hkjPk4PCZ
    \nwKnha0dlScati9CCt3UzXSNJOSLalKdHErH08Iqd+1BchScxCfk0xNITn1HZZGmI
    \n+vbmunok3A2lucI14rnsrcbkGYqxGikySN6B2cRLBDK4Y3wChiW6NVYtVqcx5/mZ
    \niYsGDVN+9QBd0eYUHce+77s96i3I
    \n-----END CERTIFICATE-----",
        "description": "description for certificate",
        "domain": "www.elb.com",
        "name": "https_certificate",
        "private_key": 
    "-----BEGIN PRIVATE KEY-----
    \nMIIEvgIBADANBgkqhkiG9w0BAQEFAASCBKgwggSkAgEAAoIBAQDQVAbOLe5xNf4M
    \n253Wn9vhdUzojetjv4J+B7kYwsMhRcgdcJ8KCnX1nfzTvI2ksXlTQ2o9BkpStnPe
    \ntB4s32ZiJRMlk+61iUUMNsHwK2WBX57JT3JgmyVbH8GbmRY0+H3sH1i72luna7rM
    \nMD30gLh6QoP3cq7PGWcuZKV7hjd1tjCTQukwMvqV8Icq39buNpIgDOWzEP5AzqXt
    \nCOFYn6RTH5SRug4hKNN7sT1eYMslHu7wtEBDKVgrLjOCe/W2f8rLT1zEsoAW2Chl
    \nZAPYUBkl/0XuTWRg3CohPPcI+UtlRSfvLDeeQ460swjbwgS/RbJh3sIwlCRLU08k
    \nEo04Z9H/AgMBAAECggEAEIeaQqHCWZk/HyYN0Am/GJSGFa2tD60SXY2fUieh8/Hl
    \nfvCArftGgMaYWPSNCJRMXB7tPwpQu19esjz4Z/cR2Je4fTLPrffGUsHFgZjv5OQB
    \nZVe4a5Hj1OcgJYhwCqPs2d9i2wToYNBbcfgh8lSETq8YaXngBO6vES9LMhHkNKKr
    \nciu9YkInNEHu6uRJ5g/eGGX3KQynTvVIhnOVGAJvjTXcoU6fm7gYdHAD6jk9lc9M
    \nEGpfYI6AdHIwFZcT/RNAxhP82lg2gUJSgAu66FfDjMwQXKbafKdP3zq4Up8a7Ale
    \nkrguPtfV1vWklg+bUFhgGaiAEYTpAUN9t2DVIiijgQKBgQDnYMMsaF0r557CM1CT
    \nXUqgCZo8MKeV2jf2drlxRRwRl33SksQbzAQ/qrLdT7GP3sCGqvkxWY2FPdFYf8kx
    \nGcCeZPcIeZYCQAM41pjtsaM8tVbLWVR8UtGBuQoPSph7JNF3Tm/JH/fbwjpjP7dt
    \nJ7n8EzkRUNE6aIMHOFEeych/PQKBgQDmf1bMogx63rTcwQ0PEZ9Vt7mTgKYK4aLr
    \niWgTWHXPZxUQaYhpjXo6+lMI6DpExiDgBAkMzJGIvS7yQiYWU+wthAr9urbWYdGZ
    \nlS6VjoTkF6r7VZoILXX0fbuXh6lm8K8IQRfBpJff56p9phMwaBpDNDrfpHB5utBU
    \nxs40yIdp6wKBgQC69Cp/xUwTX7GdxQzEJctYiKnBHKcspAg38zJf3bGSXU/jR4eB
    \n1lVQhELGI9CbKSdzKM71GyEImix/T7FnJSHIWlho1qVo6AQyduNWnAQD15pr8KAd
    \nXGXAZZ1FQcb3KYa+2fflERmazdOTwjYZ0tGqZnXkEeMdSLkmqlCRigWhGQKBgDak
    \n/735uP20KKqhNehZpC2dJei7OiIgRhCS/dKASUXHSW4fptBnUxACYocdDxtY4Vha
    \nfI7FPMdvGl8ioYbvlHFh+X0Xs9r1S8yeWnHoXMb6eXWmYKMJrAoveLa+2cFm1Agf
    \n7nLhA4R4lqm9IpV6SKegDUkR4fxp9pPyodZPqBLLAoGBAJkD4wHW54Pwd4Ctfk9o
    \njHjWB7pQlUYpTZO9dm+4fpCMn9Okf43AE2yAOaAP94GdzdDJkxfciXKcsYr9IIuk
    \nfaoXgjKR7p1zERiWZuFF63SB4aiyX1H7IX0MwHDZQO38a5gZaOm/BUlGKMWXzuEd
    \n3fy+1rCUwzOp9LSjtJYf4ege
    \n-----END PRIVATE KEY-----"
    }
    ```


## 响应示例<a name="section17584172515301"></a>

-   响应样例1

    ```
    {
        "certificate": "-----BEGIN CERTIFICATE-----\nMIIC4TCCAcmgAwIBAgICEREwDQYJKoZIhvcNAQELBQAwFzEVMBMGA1UEAxMMTXlD\nb21wYW55IENBMB4XDTE4MDcwMjEzMjU0N1oXDTQ1MTExNzEzMjU0N1owFDESMBAG\nA1UEAwwJbG9jYWxob3N0MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEA\n0FQGzi3ucTX+DNud1p/b4XVM6I3rY7+Cfge5GMLDIUXIHXCfCgp19Z3807yNpLF5\nU0NqPQZKUrZz3rQeLN9mYiUTJZPutYlFDDbB8CtlgV+eyU9yYJslWx/Bm5kWNPh9\n7B9Yu9pbp2u6zDA99IC4ekKD93KuzxlnLmSle4Y3dbYwk0LpMDL6lfCHKt/W7jaS\nIAzlsxD+QM6l7QjhWJ+kUx+UkboOISjTe7E9XmDLJR7u8LRAQylYKy4zgnv1tn/K\ny09cxLKAFtgoZWQD2FAZJf9F7k1kYNwqITz3CPlLZUUn7yw3nkOOtLMI28IEv0Wy\nYd7CMJQkS1NPJBKNOGfR/wIDAQABozowODAhBgNVHREEGjAYggpkb21haW4uY29t\nhwQKuUvJhwR/AAABMBMGA1UdJQQMMAoGCCsGAQUFBwMBMA0GCSqGSIb3DQEBCwUA\nA4IBAQA8lMQJxaTey7EjXtRLSVlEAMftAQPG6jijNQuvIBQYUDauDT4W2XUZ5wAn\njiOyQ83va672K1G9s8n6xlH+xwwdSNnozaKzC87vwSeZKIOdl9I5I98TGKI6OoDa\nezmzCwQYtHBMVQ4c7Ml8554Ft1mWSt4dMAK2rzNYjvPRLYlzp1HMnI6hkjPk4PCZ\nwKnha0dlScati9CCt3UzXSNJOSLalKdHErH08Iqd+1BchScxCfk0xNITn1HZZGmI\n+vbmunok3A2lucI14rnsrcbkGYqxGikySN6B2cRLBDK4Y3wChiW6NVYtVqcx5/mZ\niYsGDVN+9QBd0eYUHce+77s96i3I\n-----END CERTIFICATE-----",
        "expire_time": "2045-11-17 13:25:47",
        "create_time": "2017-02-25 09:35:27",
        "update_time": "2017-02-25 09:38:27",
        "id": "23ef9aad4ecb463580476d324a6c71af",
        "description": "description for certificate",
        "domain": "www.elb.com",
        "type": "server",
        "admin_state_up": true,
        "tenant_id": "a31d2bdcf7604c0faaddb058e1e08819",
        "name": "https_certificate",
        "private_key": "-----BEGIN PRIVATE KEY-----\nMIIEvgIBADANBgkqhkiG9w0BAQEFAASCBKgwggSkAgEAAoIBAQDQVAbOLe5xNf4M\n253Wn9vhdUzojetjv4J+B7kYwsMhRcgdcJ8KCnX1nfzTvI2ksXlTQ2o9BkpStnPe\ntB4s32ZiJRMlk+61iUUMNsHwK2WBX57JT3JgmyVbH8GbmRY0+H3sH1i72luna7rM\nMD30gLh6QoP3cq7PGWcuZKV7hjd1tjCTQukwMvqV8Icq39buNpIgDOWzEP5AzqXt\nCOFYn6RTH5SRug4hKNN7sT1eYMslHu7wtEBDKVgrLjOCe/W2f8rLT1zEsoAW2Chl\nZAPYUBkl/0XuTWRg3CohPPcI+UtlRSfvLDeeQ460swjbwgS/RbJh3sIwlCRLU08k\nEo04Z9H/AgMBAAECggEAEIeaQqHCWZk/HyYN0Am/GJSGFa2tD60SXY2fUieh8/Hl\nfvCArftGgMaYWPSNCJRMXB7tPwpQu19esjz4Z/cR2Je4fTLPrffGUsHFgZjv5OQB\nZVe4a5Hj1OcgJYhwCqPs2d9i2wToYNBbcfgh8lSETq8YaXngBO6vES9LMhHkNKKr\nciu9YkInNEHu6uRJ5g/eGGX3KQynTvVIhnOVGAJvjTXcoU6fm7gYdHAD6jk9lc9M\nEGpfYI6AdHIwFZcT/RNAxhP82lg2gUJSgAu66FfDjMwQXKbafKdP3zq4Up8a7Ale\nkrguPtfV1vWklg+bUFhgGaiAEYTpAUN9t2DVIiijgQKBgQDnYMMsaF0r557CM1CT\nXUqgCZo8MKeV2jf2drlxRRwRl33SksQbzAQ/qrLdT7GP3sCGqvkxWY2FPdFYf8kx\nGcCeZPcIeZYCQAM41pjtsaM8tVbLWVR8UtGBuQoPSph7JNF3Tm/JH/fbwjpjP7dt\nJ7n8EzkRUNE6aIMHOFEeych/PQKBgQDmf1bMogx63rTcwQ0PEZ9Vt7mTgKYK4aLr\niWgTWHXPZxUQaYhpjXo6+lMI6DpExiDgBAkMzJGIvS7yQiYWU+wthAr9urbWYdGZ\nlS6VjoTkF6r7VZoILXX0fbuXh6lm8K8IQRfBpJff56p9phMwaBpDNDrfpHB5utBU\nxs40yIdp6wKBgQC69Cp/xUwTX7GdxQzEJctYiKnBHKcspAg38zJf3bGSXU/jR4eB\n1lVQhELGI9CbKSdzKM71GyEImix/T7FnJSHIWlho1qVo6AQyduNWnAQD15pr8KAd\nXGXAZZ1FQcb3KYa+2fflERmazdOTwjYZ0tGqZnXkEeMdSLkmqlCRigWhGQKBgDak\n/735uP20KKqhNehZpC2dJei7OiIgRhCS/dKASUXHSW4fptBnUxACYocdDxtY4Vha\nfI7FPMdvGl8ioYbvlHFh+X0Xs9r1S8yeWnHoXMb6eXWmYKMJrAoveLa+2cFm1Agf\n7nLhA4R4lqm9IpV6SKegDUkR4fxp9pPyodZPqBLLAoGBAJkD4wHW54Pwd4Ctfk9o\njHjWB7pQlUYpTZO9dm+4fpCMn9Okf43AE2yAOaAP94GdzdDJkxfciXKcsYr9IIuk\nfaoXgjKR7p1zERiWZuFF63SB4aiyX1H7IX0MwHDZQO38a5gZaOm/BUlGKMWXzuEd\n3fy+1rCUwzOp9LSjtJYf4ege\n-----END PRIVATE KEY-----"
    }
    ```


## 返回码<a name="elb_zq_zs_0004_zh-cn_topic_0049139664_section36936567"></a>

请参见[状态码](状态码.md)。

