# 更新SSL证书<a name="zh-cn_topic_0096561585"></a>

## 功能介绍<a name="zh-cn_topic_0085859919_section48870738174959"></a>

更新SSL证书。

## URI<a name="zh-cn_topic_0085859919_section9730439174959"></a>

PUT /v2.0/lbaas/certificates/\{certificate\_id\}

**表 1**  参数说明

<a name="table1664412216716"></a>
<table><thead align="left"><tr id="row268472119719"><th class="cellrowborder" valign="top" width="21.42785721427857%" id="mcps1.2.5.1.1"><p id="p196855212718"><a name="p196855212718"></a><a name="p196855212718"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="21.42785721427857%" id="mcps1.2.5.1.2"><p id="p26859217717"><a name="p26859217717"></a><a name="p26859217717"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="14.288571142885711%" id="mcps1.2.5.1.3"><p id="p2068552113716"><a name="p2068552113716"></a><a name="p2068552113716"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="42.85571442855714%" id="mcps1.2.5.1.4"><p id="p7713181216"><a name="p7713181216"></a><a name="p7713181216"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row10685122111711"><td class="cellrowborder" valign="top" width="21.42785721427857%" headers="mcps1.2.5.1.1 "><p id="p14685821871"><a name="p14685821871"></a><a name="p14685821871"></a>certificate_id</p>
</td>
<td class="cellrowborder" valign="top" width="21.42785721427857%" headers="mcps1.2.5.1.2 "><p id="p5685121778"><a name="p5685121778"></a><a name="p5685121778"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="14.288571142885711%" headers="mcps1.2.5.1.3 "><p id="p368519213715"><a name="p368519213715"></a><a name="p368519213715"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="42.85571442855714%" headers="mcps1.2.5.1.4 "><p id="p1368515211714"><a name="p1368515211714"></a><a name="p1368515211714"></a>SSL证书ID。</p>
</td>
</tr>
</tbody>
</table>

## 接口约束<a name="zh-cn_topic_0085859919_section47166405174959"></a>

如果待更新域名为""的证书被监听器使用，则该证书域名不允许被更新为""，同时系统会返回409响应。

## 请求消息<a name="zh-cn_topic_0085859919_section38626650174959"></a>

**表 2**  请求参数

<a name="zh-cn_topic_0085859919_table62215390174959"></a>
<table><thead align="left"><tr id="zh-cn_topic_0085859919_row35879330174959"><th class="cellrowborder" valign="top" width="21.36%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0085859919_p52201676174959"><a name="zh-cn_topic_0085859919_p52201676174959"></a><a name="zh-cn_topic_0085859919_p52201676174959"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="11.110000000000001%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0085859919_p5280357174959"><a name="zh-cn_topic_0085859919_p5280357174959"></a><a name="zh-cn_topic_0085859919_p5280357174959"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="18.4%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0085859919_p2598936174959"><a name="zh-cn_topic_0085859919_p2598936174959"></a><a name="zh-cn_topic_0085859919_p2598936174959"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="49.13%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0085859919_p46936095174959"><a name="zh-cn_topic_0085859919_p46936095174959"></a><a name="zh-cn_topic_0085859919_p46936095174959"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row48584188318"><td class="cellrowborder" valign="top" width="21.36%" headers="mcps1.2.5.1.1 "><p id="p785841873113"><a name="p785841873113"></a><a name="p785841873113"></a>admin_state_up</p>
</td>
<td class="cellrowborder" valign="top" width="11.110000000000001%" headers="mcps1.2.5.1.2 "><p id="p7858131818319"><a name="p7858131818319"></a><a name="p7858131818319"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="18.4%" headers="mcps1.2.5.1.3 "><p id="p15858218103114"><a name="p15858218103114"></a><a name="p15858218103114"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="49.13%" headers="mcps1.2.5.1.4 "><p id="p189741017613"><a name="p189741017613"></a><a name="p189741017613"></a>SSL证书的管理状态；</p>
<p id="p189052592020"><a name="p189052592020"></a><a name="p189052592020"></a>取值范围： true/false。</p>
<p id="p81009155107"><a name="p81009155107"></a><a name="p81009155107"></a>该字段为预留字段，暂未启用。只支持设定为true。</p>
</td>
</tr>
<tr id="zh-cn_topic_0085859919_row29288134174959"><td class="cellrowborder" valign="top" width="21.36%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0085859919_p31165543174959"><a name="zh-cn_topic_0085859919_p31165543174959"></a><a name="zh-cn_topic_0085859919_p31165543174959"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="11.110000000000001%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0085859919_p34889889174959"><a name="zh-cn_topic_0085859919_p34889889174959"></a><a name="zh-cn_topic_0085859919_p34889889174959"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="18.4%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0085859919_p53796641174959"><a name="zh-cn_topic_0085859919_p53796641174959"></a><a name="zh-cn_topic_0085859919_p53796641174959"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="49.13%" headers="mcps1.2.5.1.4 "><p id="p034963734312"><a name="p034963734312"></a><a name="p034963734312"></a>SSL证书的名称。</p>
<p id="p1264211013318"><a name="p1264211013318"></a><a name="p1264211013318"></a>支持的最大字符长度：255</p>
</td>
</tr>
<tr id="zh-cn_topic_0085859919_row12347817174959"><td class="cellrowborder" valign="top" width="21.36%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0085859919_p9569533174959"><a name="zh-cn_topic_0085859919_p9569533174959"></a><a name="zh-cn_topic_0085859919_p9569533174959"></a>description</p>
</td>
<td class="cellrowborder" valign="top" width="11.110000000000001%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0085859919_p29495170174959"><a name="zh-cn_topic_0085859919_p29495170174959"></a><a name="zh-cn_topic_0085859919_p29495170174959"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="18.4%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0085859919_p59414857174959"><a name="zh-cn_topic_0085859919_p59414857174959"></a><a name="zh-cn_topic_0085859919_p59414857174959"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="49.13%" headers="mcps1.2.5.1.4 "><p id="p636474910435"><a name="p636474910435"></a><a name="p636474910435"></a>SSL证书的描述信息。</p>
<p id="p1442761811405"><a name="p1442761811405"></a><a name="p1442761811405"></a>支持的最大字符长度：255</p>
</td>
</tr>
<tr id="zh-cn_topic_0085859919_row25521469174959"><td class="cellrowborder" valign="top" width="21.36%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0085859919_p47787672174959"><a name="zh-cn_topic_0085859919_p47787672174959"></a><a name="zh-cn_topic_0085859919_p47787672174959"></a>domain</p>
</td>
<td class="cellrowborder" valign="top" width="11.110000000000001%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0085859919_p21932410174959"><a name="zh-cn_topic_0085859919_p21932410174959"></a><a name="zh-cn_topic_0085859919_p21932410174959"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="18.4%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0085859919_p2180173174959"><a name="zh-cn_topic_0085859919_p2180173174959"></a><a name="zh-cn_topic_0085859919_p2180173174959"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="49.13%" headers="mcps1.2.5.1.4 "><p id="p14884193271218"><a name="p14884193271218"></a><a name="p14884193271218"></a>服务端证书所签的域名。默认值：null；</p>
<p id="p15972220174018"><a name="p15972220174018"></a><a name="p15972220174018"></a>支持的最大字符长度：100</p>
<p id="p16305043131216"><a name="p16305043131216"></a><a name="p16305043131216"></a>取值范围：</p>
<a name="ul128048293014"></a><a name="ul128048293014"></a><ul id="ul128048293014"><li>普通域名由若干字符串组成，总长度为0-100，字符串间以"."分割，单个字符串长度不超过63个字符，只能包含英文字母、数字或"-"，且必须以字母或数字开头和结尾。</li><li>泛域名在普通域名的基础上仅允许首字母为"*"。该字段仅type为server时有效。</li></ul>
<div class="note" id="zh-cn_topic_0085859918_note3391807017458"><a name="zh-cn_topic_0085859918_note3391807017458"></a><a name="zh-cn_topic_0085859918_note3391807017458"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="zh-cn_topic_0085859918_p4119083617458"><a name="zh-cn_topic_0085859918_p4119083617458"></a><a name="zh-cn_topic_0085859918_p4119083617458"></a>该字段仅type为server时有效。</p>
</div></div>
</td>
</tr>
<tr id="zh-cn_topic_0085859919_row10022251174959"><td class="cellrowborder" valign="top" width="21.36%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0085859919_p57736676174959"><a name="zh-cn_topic_0085859919_p57736676174959"></a><a name="zh-cn_topic_0085859919_p57736676174959"></a>private_key</p>
</td>
<td class="cellrowborder" valign="top" width="11.110000000000001%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0085859919_p31369944174959"><a name="zh-cn_topic_0085859919_p31369944174959"></a><a name="zh-cn_topic_0085859919_p31369944174959"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="18.4%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0085859919_p27614681174959"><a name="zh-cn_topic_0085859919_p27614681174959"></a><a name="zh-cn_topic_0085859919_p27614681174959"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="49.13%" headers="mcps1.2.5.1.4 "><p id="p59621116158"><a name="p59621116158"></a><a name="p59621116158"></a>服务端的私有密钥。</p>
<p id="p1658134219251"><a name="p1658134219251"></a><a name="p1658134219251"></a>格式：私钥为PEM格式。</p>
<div class="note" id="zh-cn_topic_0085859918_note58901689174653"><a name="zh-cn_topic_0085859918_note58901689174653"></a><a name="zh-cn_topic_0085859918_note58901689174653"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p251432614204"><a name="p251432614204"></a><a name="p251432614204"></a><strong id="b16514226202016"><a name="b16514226202016"></a><a name="b16514226202016"></a></strong>该字段仅type为server时有效且为必选。</p>
<p id="zh-cn_topic_0085859918_p28975920174653"><a name="zh-cn_topic_0085859918_p28975920174653"></a><a name="zh-cn_topic_0085859918_p28975920174653"></a>该字段在type为client时无效。</p>
</div></div>
</td>
</tr>
<tr id="zh-cn_topic_0085859919_row18969603174959"><td class="cellrowborder" valign="top" width="21.36%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0085859919_p44096056174959"><a name="zh-cn_topic_0085859919_p44096056174959"></a><a name="zh-cn_topic_0085859919_p44096056174959"></a>certificate</p>
</td>
<td class="cellrowborder" valign="top" width="11.110000000000001%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0085859919_p3351721174959"><a name="zh-cn_topic_0085859919_p3351721174959"></a><a name="zh-cn_topic_0085859919_p3351721174959"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="18.4%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0085859919_p51899034174959"><a name="zh-cn_topic_0085859919_p51899034174959"></a><a name="zh-cn_topic_0085859919_p51899034174959"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="49.13%" headers="mcps1.2.5.1.4 "><p id="p56851334121510"><a name="p56851334121510"></a><a name="p56851334121510"></a>服务端公有密钥证书或者用于认证客户端证书的CA证书，由type字段区分。</p>
<p id="p8493444202513"><a name="p8493444202513"></a><a name="p8493444202513"></a>格式：证书为PEM格式。</p>
</td>
</tr>
</tbody>
</table>

## 响应消息<a name="zh-cn_topic_0085859919_section31160971174959"></a>

**表 3**  响应参数

<a name="zh-cn_topic_0085859919_table55952037174959"></a>
<table><thead align="left"><tr id="zh-cn_topic_0096561584_zh-cn_topic_0085859918_row11412198173534"><th class="cellrowborder" valign="top" width="21.099999999999998%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p66723761173534"><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p66723761173534"></a><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p66723761173534"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="18.9%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p31496314173534"><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p31496314173534"></a><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p31496314173534"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p5981838173534"><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p5981838173534"></a><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p5981838173534"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0096561584_zh-cn_topic_0085859918_row20744965173534"><td class="cellrowborder" valign="top" width="21.099999999999998%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p21724371173534"><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p21724371173534"></a><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p21724371173534"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="18.9%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0096561584_p11149359102718"><a name="zh-cn_topic_0096561584_p11149359102718"></a><a name="zh-cn_topic_0096561584_p11149359102718"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p4585726173534"><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p4585726173534"></a><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p4585726173534"></a>SSL证书ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0096561584_row1313561214274"><td class="cellrowborder" valign="top" width="21.099999999999998%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0096561584_p1913501218276"><a name="zh-cn_topic_0096561584_p1913501218276"></a><a name="zh-cn_topic_0096561584_p1913501218276"></a>tenant_id</p>
</td>
<td class="cellrowborder" valign="top" width="18.9%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0096561584_p16135161202717"><a name="zh-cn_topic_0096561584_p16135161202717"></a><a name="zh-cn_topic_0096561584_p16135161202717"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0096561584_p1413510125272"><a name="zh-cn_topic_0096561584_p1413510125272"></a><a name="zh-cn_topic_0096561584_p1413510125272"></a>SSL证书所在的项目ID。</p>
<p id="zh-cn_topic_0096561584_p12961124943614"><a name="zh-cn_topic_0096561584_p12961124943614"></a><a name="zh-cn_topic_0096561584_p12961124943614"></a>支持的最大字符长度：255</p>
</td>
</tr>
<tr id="zh-cn_topic_0096561584_row7916373278"><td class="cellrowborder" valign="top" width="21.099999999999998%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0096561584_p19161672277"><a name="zh-cn_topic_0096561584_p19161672277"></a><a name="zh-cn_topic_0096561584_p19161672277"></a>admin_state_up</p>
</td>
<td class="cellrowborder" valign="top" width="18.9%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0096561584_p191616732710"><a name="zh-cn_topic_0096561584_p191616732710"></a><a name="zh-cn_topic_0096561584_p191616732710"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0096561584_p274684451617"><a name="zh-cn_topic_0096561584_p274684451617"></a><a name="zh-cn_topic_0096561584_p274684451617"></a>SSL证书的管理状态；</p>
<p id="zh-cn_topic_0096561584_p1674619446167"><a name="zh-cn_topic_0096561584_p1674619446167"></a><a name="zh-cn_topic_0096561584_p1674619446167"></a>取值范围： true/false。</p>
</td>
</tr>
<tr id="zh-cn_topic_0096561584_zh-cn_topic_0085859918_row29191383173534"><td class="cellrowborder" valign="top" width="21.099999999999998%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p55607168173534"><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p55607168173534"></a><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p55607168173534"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="18.9%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p28026059173534"><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p28026059173534"></a><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p28026059173534"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p21173547173534"><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p21173547173534"></a><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p21173547173534"></a>SSL证书名称。</p>
<p id="zh-cn_topic_0096561584_p18170252113611"><a name="zh-cn_topic_0096561584_p18170252113611"></a><a name="zh-cn_topic_0096561584_p18170252113611"></a>支持的最大字符长度：255</p>
</td>
</tr>
<tr id="zh-cn_topic_0096561584_zh-cn_topic_0085859918_row41991314173534"><td class="cellrowborder" valign="top" width="21.099999999999998%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p63231950173534"><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p63231950173534"></a><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p63231950173534"></a>description</p>
</td>
<td class="cellrowborder" valign="top" width="18.9%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p35111452173534"><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p35111452173534"></a><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p35111452173534"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p49236727173534"><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p49236727173534"></a><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p49236727173534"></a>证书描述SSL证书描述。</p>
<p id="zh-cn_topic_0096561584_p71641548361"><a name="zh-cn_topic_0096561584_p71641548361"></a><a name="zh-cn_topic_0096561584_p71641548361"></a>支持的最大字符长度：255</p>
</td>
</tr>
<tr id="zh-cn_topic_0096561584_zh-cn_topic_0085859918_row27338318173534"><td class="cellrowborder" valign="top" width="21.099999999999998%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p43711802173534"><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p43711802173534"></a><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p43711802173534"></a>type</p>
</td>
<td class="cellrowborder" valign="top" width="18.9%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p16661086173534"><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p16661086173534"></a><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p16661086173534"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p47471091173534"><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p47471091173534"></a><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p47471091173534"></a>SSL证书的类型。</p>
<div class="p" id="zh-cn_topic_0096561584_p9834519174"><a name="zh-cn_topic_0096561584_p9834519174"></a><a name="zh-cn_topic_0096561584_p9834519174"></a>取值范围：<a name="zh-cn_topic_0096561584_ul48343181711"></a><a name="zh-cn_topic_0096561584_ul48343181711"></a><ul id="zh-cn_topic_0096561584_ul48343181711"><li>server：服务端证书；</li><li>client：客户端证书；</li></ul>
</div>
</td>
</tr>
<tr id="zh-cn_topic_0096561584_zh-cn_topic_0085859918_row57368822173534"><td class="cellrowborder" valign="top" width="21.099999999999998%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p66718031173534"><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p66718031173534"></a><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p66718031173534"></a>domain</p>
</td>
<td class="cellrowborder" valign="top" width="18.9%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p28969287173534"><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p28969287173534"></a><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p28969287173534"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p52667105173534"><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p52667105173534"></a><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p52667105173534"></a>服务端证书所签域名。</p>
<p id="zh-cn_topic_0096561584_p7145757123615"><a name="zh-cn_topic_0096561584_p7145757123615"></a><a name="zh-cn_topic_0096561584_p7145757123615"></a>支持的最大字符长度：100</p>
</td>
</tr>
<tr id="zh-cn_topic_0096561584_zh-cn_topic_0085859918_row32267386173534"><td class="cellrowborder" valign="top" width="21.099999999999998%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p2838320173534"><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p2838320173534"></a><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p2838320173534"></a>private_key</p>
</td>
<td class="cellrowborder" valign="top" width="18.9%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p43739651173534"><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p43739651173534"></a><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p43739651173534"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p12798312173534"><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p12798312173534"></a><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p12798312173534"></a>PEM格式的服务端私有密钥。</p>
</td>
</tr>
<tr id="zh-cn_topic_0096561584_zh-cn_topic_0085859918_row329105173534"><td class="cellrowborder" valign="top" width="21.099999999999998%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p10917956173534"><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p10917956173534"></a><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p10917956173534"></a>certificate</p>
</td>
<td class="cellrowborder" valign="top" width="18.9%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p50089397173534"><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p50089397173534"></a><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p50089397173534"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p47546713173534"><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p47546713173534"></a><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p47546713173534"></a>PEM格式的服务端公有密钥或者用于认证客户端证书的CA证书，由type字段区分。</p>
</td>
</tr>
<tr id="zh-cn_topic_0096561584_row5698184112395"><td class="cellrowborder" valign="top" width="21.099999999999998%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0096561584_p1169816414399"><a name="zh-cn_topic_0096561584_p1169816414399"></a><a name="zh-cn_topic_0096561584_p1169816414399"></a>expire_time</p>
</td>
<td class="cellrowborder" valign="top" width="18.9%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0096561584_p969874112392"><a name="zh-cn_topic_0096561584_p969874112392"></a><a name="zh-cn_topic_0096561584_p969874112392"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0096561584_p146981141133912"><a name="zh-cn_topic_0096561584_p146981141133912"></a><a name="zh-cn_topic_0096561584_p146981141133912"></a>SSL证书的过期时间。</p>
<p id="zh-cn_topic_0096561584_zh-cn_topic_0141008271_p52901417154816"><a name="zh-cn_topic_0096561584_zh-cn_topic_0141008271_p52901417154816"></a><a name="zh-cn_topic_0096561584_zh-cn_topic_0141008271_p52901417154816"></a>格式为UTC时间：YYYY-MM-DDTHH:MM:SS</p>
</td>
</tr>
<tr id="zh-cn_topic_0096561584_zh-cn_topic_0085859918_row58956881173534"><td class="cellrowborder" valign="top" width="21.099999999999998%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p28854566173534"><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p28854566173534"></a><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p28854566173534"></a>create_time</p>
</td>
<td class="cellrowborder" valign="top" width="18.9%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p41288654173534"><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p41288654173534"></a><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p41288654173534"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p14875840173534"><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p14875840173534"></a><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p14875840173534"></a>SSL证书的创建时间。</p>
<p id="zh-cn_topic_0096561584_p17245855710"><a name="zh-cn_topic_0096561584_p17245855710"></a><a name="zh-cn_topic_0096561584_p17245855710"></a>格式为UTC时间：YYYY-MM-DDTHH:MM:SS</p>
</td>
</tr>
<tr id="zh-cn_topic_0096561584_zh-cn_topic_0085859918_row43957201173534"><td class="cellrowborder" valign="top" width="21.099999999999998%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p57772843173534"><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p57772843173534"></a><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p57772843173534"></a>update_time</p>
</td>
<td class="cellrowborder" valign="top" width="18.9%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p43564658173534"><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p43564658173534"></a><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p43564658173534"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p4321549173534"><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p4321549173534"></a><a name="zh-cn_topic_0096561584_zh-cn_topic_0085859918_p4321549173534"></a>SSL证书的更新时间。</p>
<p id="zh-cn_topic_0096561584_p53376597572"><a name="zh-cn_topic_0096561584_p53376597572"></a><a name="zh-cn_topic_0096561584_p53376597572"></a>格式为UTC时间：YYYY-MM-DDTHH:MM:SS</p>
</td>
</tr>
</tbody>
</table>

## 示例<a name="section10945125163317"></a>

-   请求样例 更新SSL证书

    ```
    PUT https://{Endpoint}/v2.0/lbaas/certificates/23ef9aad4ecb463580476d324a6c71af 
    
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

-   响应样例

    ```
    {
        "certificate": "-----BEGIN CERTIFICATE-----\nMIIC4TCCAcmgAwIBAgICEREwDQYJKoZIhvcNAQELBQAwFzEVMBMGA1UEAxMMTXlD\nb21wYW55IENBMB4XDTE4MDcwMjEzMjU0N1oXDTQ1MTExNzEzMjU0N1owFDESMBAG\nA1UEAwwJbG9jYWxob3N0MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEA\n0FQGzi3ucTX+DNud1p/b4XVM6I3rY7+Cfge5GMLDIUXIHXCfCgp19Z3807yNpLF5\nU0NqPQZKUrZz3rQeLN9mYiUTJZPutYlFDDbB8CtlgV+eyU9yYJslWx/Bm5kWNPh9\n7B9Yu9pbp2u6zDA99IC4ekKD93KuzxlnLmSle4Y3dbYwk0LpMDL6lfCHKt/W7jaS\nIAzlsxD+QM6l7QjhWJ+kUx+UkboOISjTe7E9XmDLJR7u8LRAQylYKy4zgnv1tn/K\ny09cxLKAFtgoZWQD2FAZJf9F7k1kYNwqITz3CPlLZUUn7yw3nkOOtLMI28IEv0Wy\nYd7CMJQkS1NPJBKNOGfR/wIDAQABozowODAhBgNVHREEGjAYggpkb21haW4uY29t\nhwQKuUvJhwR/AAABMBMGA1UdJQQMMAoGCCsGAQUFBwMBMA0GCSqGSIb3DQEBCwUA\nA4IBAQA8lMQJxaTey7EjXtRLSVlEAMftAQPG6jijNQuvIBQYUDauDT4W2XUZ5wAn\njiOyQ83va672K1G9s8n6xlH+xwwdSNnozaKzC87vwSeZKIOdl9I5I98TGKI6OoDa\nezmzCwQYtHBMVQ4c7Ml8554Ft1mWSt4dMAK2rzNYjvPRLYlzp1HMnI6hkjPk4PCZ\nwKnha0dlScati9CCt3UzXSNJOSLalKdHErH08Iqd+1BchScxCfk0xNITn1HZZGmI\n+vbmunok3A2lucI14rnsrcbkGYqxGikySN6B2cRLBDK4Y3wChiW6NVYtVqcx5/mZ\niYsGDVN+9QBd0eYUHce+77s96i3I\n-----END CERTIFICATE-----",
        "expire_time": "2045-11-17 13:25:47",
        "create_time": "2017-02-25 09:35:27",
        "description": "description for certificate",
        "domain": "www.elb.com",
        "id": "23ef9aad4ecb463580476d324a6c71af",
        "admin_state_up": true,
        "tenant_id": "a31d2bdcf7604c0faaddb058e1e08819",
        "name": "https_certificate",
        "private_key": "-----BEGIN PRIVATE KEY-----
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
    \n-----END PRIVATE KEY-----",
        "type": "server",
        "update_time": "2017-02-25 09:38:27"
    }
    ```


## 返回码<a name="zh-cn_topic_0049139664_section36936567"></a>

请参见[增强型负载均衡返回码说明](增强型负载均衡返回码说明.md)。

