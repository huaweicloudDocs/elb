# 查询SSL证书详情<a name="zh-cn_topic_0141008501"></a>

## 功能介绍<a name="zh-cn_topic_0096561583_zh-cn_topic_0085859917_section20669223172659"></a>

查询指定SSL证书的详情信息。

## URI<a name="zh-cn_topic_0096561583_zh-cn_topic_0085859917_section23198423172659"></a>

GET /v2/\{project\_id\}/elb/certificates/\{certificate\_id\}

**表 1**  参数说明

<a name="zh-cn_topic_0096561583_table115396581764"></a>
<table><thead align="left"><tr id="zh-cn_topic_0096561583_row3571205812618"><th class="cellrowborder" valign="top" width="24.717528247175284%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0096561583_p15710589617"><a name="zh-cn_topic_0096561583_p15710589617"></a><a name="zh-cn_topic_0096561583_p15710589617"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="16.408359164083592%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0096561583_p10571658366"><a name="zh-cn_topic_0096561583_p10571658366"></a><a name="zh-cn_topic_0096561583_p10571658366"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="9.44905509449055%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0096561583_p35711958366"><a name="zh-cn_topic_0096561583_p35711958366"></a><a name="zh-cn_topic_0096561583_p35711958366"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="49.42505749425058%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0096561583_p957119581611"><a name="zh-cn_topic_0096561583_p957119581611"></a><a name="zh-cn_topic_0096561583_p957119581611"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row135411329165514"><td class="cellrowborder" valign="top" width="24.717528247175284%" headers="mcps1.2.5.1.1 "><p id="p1399071505415"><a name="p1399071505415"></a><a name="p1399071505415"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="16.408359164083592%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0020100158_p557643211309"><a name="zh-cn_topic_0020100158_p557643211309"></a><a name="zh-cn_topic_0020100158_p557643211309"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="9.44905509449055%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0020100158_p6162677511304"><a name="zh-cn_topic_0020100158_p6162677511304"></a><a name="zh-cn_topic_0020100158_p6162677511304"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="49.42505749425058%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0020100158_p35845144113012"><a name="zh-cn_topic_0020100158_p35845144113012"></a><a name="zh-cn_topic_0020100158_p35845144113012"></a>操作用户的项目ID。</p>
<p id="p8222164914610"><a name="p8222164914610"></a><a name="p8222164914610"></a>获取方法详见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
<tr id="zh-cn_topic_0096561583_row657118581961"><td class="cellrowborder" valign="top" width="24.717528247175284%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0096561583_p1357111580610"><a name="zh-cn_topic_0096561583_p1357111580610"></a><a name="zh-cn_topic_0096561583_p1357111580610"></a>certificate_id</p>
</td>
<td class="cellrowborder" valign="top" width="16.408359164083592%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0096561583_p8571105811614"><a name="zh-cn_topic_0096561583_p8571105811614"></a><a name="zh-cn_topic_0096561583_p8571105811614"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="9.44905509449055%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0096561583_p105711858666"><a name="zh-cn_topic_0096561583_p105711858666"></a><a name="zh-cn_topic_0096561583_p105711858666"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="49.42505749425058%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0096561583_p157116580613"><a name="zh-cn_topic_0096561583_p157116580613"></a><a name="zh-cn_topic_0096561583_p157116580613"></a>证书id。</p>
</td>
</tr>
</tbody>
</table>

## 接口约束<a name="zh-cn_topic_0096561583_zh-cn_topic_0085859917_section11109632172659"></a>

无。

## 请求消息<a name="zh-cn_topic_0096561583_zh-cn_topic_0085859917_section32916575172659"></a>

无

## 响应消息<a name="zh-cn_topic_0096561583_zh-cn_topic_0085859917_section31940794172659"></a>

**表 2**  响应参数

<a name="zh-cn_topic_0096561583_zh-cn_topic_0085859917_table45008640172659"></a>
<table><thead align="left"><tr id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_row11412198173534"><th class="cellrowborder" valign="top" width="21.099999999999998%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p66723761173534"><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p66723761173534"></a><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p66723761173534"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="18.9%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p31496314173534"><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p31496314173534"></a><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p31496314173534"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p5981838173534"><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p5981838173534"></a><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p5981838173534"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_row20744965173534"><td class="cellrowborder" valign="top" width="21.099999999999998%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p21724371173534"><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p21724371173534"></a><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p21724371173534"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="18.9%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_p11149359102718"><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_p11149359102718"></a><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_p11149359102718"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p4585726173534"><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p4585726173534"></a><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p4585726173534"></a>SSL证书ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_row1313561214274"><td class="cellrowborder" valign="top" width="21.099999999999998%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_p1913501218276"><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_p1913501218276"></a><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_p1913501218276"></a>tenant_id</p>
</td>
<td class="cellrowborder" valign="top" width="18.9%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_p16135161202717"><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_p16135161202717"></a><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_p16135161202717"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_p1413510125272"><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_p1413510125272"></a><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_p1413510125272"></a>SSL证书所在的项目ID。</p>
<p id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_p12961124943614"><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_p12961124943614"></a><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_p12961124943614"></a>支持的最大字符长度：255</p>
</td>
</tr>
<tr id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_row7916373278"><td class="cellrowborder" valign="top" width="21.099999999999998%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_p19161672277"><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_p19161672277"></a><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_p19161672277"></a>admin_state_up</p>
</td>
<td class="cellrowborder" valign="top" width="18.9%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_p191616732710"><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_p191616732710"></a><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_p191616732710"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_p274684451617"><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_p274684451617"></a><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_p274684451617"></a>SSL证书的管理状态；</p>
<p id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_p1674619446167"><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_p1674619446167"></a><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_p1674619446167"></a>取值范围： true/false。</p>
</td>
</tr>
<tr id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_row29191383173534"><td class="cellrowborder" valign="top" width="21.099999999999998%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p55607168173534"><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p55607168173534"></a><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p55607168173534"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="18.9%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p28026059173534"><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p28026059173534"></a><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p28026059173534"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p21173547173534"><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p21173547173534"></a><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p21173547173534"></a>SSL证书名称。</p>
<p id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_p18170252113611"><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_p18170252113611"></a><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_p18170252113611"></a>支持的最大字符长度：255</p>
</td>
</tr>
<tr id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_row41991314173534"><td class="cellrowborder" valign="top" width="21.099999999999998%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p63231950173534"><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p63231950173534"></a><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p63231950173534"></a>description</p>
</td>
<td class="cellrowborder" valign="top" width="18.9%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p35111452173534"><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p35111452173534"></a><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p35111452173534"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p49236727173534"><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p49236727173534"></a><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p49236727173534"></a>证书描述SSL证书描述。</p>
<p id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_p71641548361"><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_p71641548361"></a><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_p71641548361"></a>支持的最大字符长度：255</p>
</td>
</tr>
<tr id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_row27338318173534"><td class="cellrowborder" valign="top" width="21.099999999999998%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p43711802173534"><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p43711802173534"></a><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p43711802173534"></a>type</p>
</td>
<td class="cellrowborder" valign="top" width="18.9%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p16661086173534"><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p16661086173534"></a><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p16661086173534"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p47471091173534"><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p47471091173534"></a><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p47471091173534"></a>SSL证书的类型。</p>
<div class="p" id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_p9834519174"><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_p9834519174"></a><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_p9834519174"></a>取值范围：<a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_ul48343181711"></a><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_ul48343181711"></a><ul id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_ul48343181711"><li>server：服务端证书；</li><li>client：客户端证书；</li></ul>
</div>
</td>
</tr>
<tr id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_row57368822173534"><td class="cellrowborder" valign="top" width="21.099999999999998%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p66718031173534"><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p66718031173534"></a><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p66718031173534"></a>domain</p>
</td>
<td class="cellrowborder" valign="top" width="18.9%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p28969287173534"><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p28969287173534"></a><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p28969287173534"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p52667105173534"><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p52667105173534"></a><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p52667105173534"></a>服务端证书所签域名。</p>
<p id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_p7145757123615"><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_p7145757123615"></a><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_p7145757123615"></a>支持的最大字符长度：100</p>
</td>
</tr>
<tr id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_row32267386173534"><td class="cellrowborder" valign="top" width="21.099999999999998%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p2838320173534"><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p2838320173534"></a><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p2838320173534"></a>private_key</p>
</td>
<td class="cellrowborder" valign="top" width="18.9%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p43739651173534"><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p43739651173534"></a><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p43739651173534"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p12798312173534"><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p12798312173534"></a><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p12798312173534"></a>PEM格式的服务端私有密钥。</p>
</td>
</tr>
<tr id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_row329105173534"><td class="cellrowborder" valign="top" width="21.099999999999998%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p10917956173534"><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p10917956173534"></a><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p10917956173534"></a>certificate</p>
</td>
<td class="cellrowborder" valign="top" width="18.9%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p50089397173534"><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p50089397173534"></a><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p50089397173534"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p47546713173534"><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p47546713173534"></a><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p47546713173534"></a>PEM格式的服务端公有密钥或者用于认证客户端证书的CA证书，由type字段区分。</p>
</td>
</tr>
<tr id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_row5698184112395"><td class="cellrowborder" valign="top" width="21.099999999999998%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_p1169816414399"><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_p1169816414399"></a><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_p1169816414399"></a>expire_time</p>
</td>
<td class="cellrowborder" valign="top" width="18.9%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_p969874112392"><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_p969874112392"></a><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_p969874112392"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_p146981141133912"><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_p146981141133912"></a><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_p146981141133912"></a>SSL证书的过期时间。</p>
<p id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0141008271_p52901417154816"><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0141008271_p52901417154816"></a><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0141008271_p52901417154816"></a>格式为UTC时间：YYYY-MM-DDTHH:MM:SS</p>
</td>
</tr>
<tr id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_row58956881173534"><td class="cellrowborder" valign="top" width="21.099999999999998%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p28854566173534"><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p28854566173534"></a><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p28854566173534"></a>create_time</p>
</td>
<td class="cellrowborder" valign="top" width="18.9%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p41288654173534"><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p41288654173534"></a><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p41288654173534"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p14875840173534"><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p14875840173534"></a><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p14875840173534"></a>SSL证书的创建时间。</p>
<p id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_p17245855710"><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_p17245855710"></a><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_p17245855710"></a>格式为UTC时间：YYYY-MM-DDTHH:MM:SS</p>
</td>
</tr>
<tr id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_row43957201173534"><td class="cellrowborder" valign="top" width="21.099999999999998%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p57772843173534"><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p57772843173534"></a><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p57772843173534"></a>update_time</p>
</td>
<td class="cellrowborder" valign="top" width="18.9%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p43564658173534"><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p43564658173534"></a><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p43564658173534"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p4321549173534"><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p4321549173534"></a><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_zh-cn_topic_0085859918_p4321549173534"></a>SSL证书的更新时间。</p>
<p id="zh-cn_topic_0096561583_zh-cn_topic_0096561584_p53376597572"><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_p53376597572"></a><a name="zh-cn_topic_0096561583_zh-cn_topic_0096561584_p53376597572"></a>格式为UTC时间：YYYY-MM-DDTHH:MM:SS</p>
</td>
</tr>
</tbody>
</table>

## 示例<a name="section6545122316451"></a>

-   请求样例1 查询SSL证书详情

    ```
    GET https://{Endpoint}/v2/a31d2bdcf7604c0faaddb058e1e08819/elb/certificates/23ef9aad4ecb463580476d324a6c71af
    ```

-   响应样例1

    ```
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
        "create_time": "2017-02-25 09:35:27",
        "expire_time": "2045-11-17 13:25:47",
        "description": "description for certificate",
        "domain": "www.elb.com",
        "id": "23ef9aad4ecb463580476d324a6c71af",
        "tenant_id": "a31d2bdcf7604c0faaddb058e1e08819",
        "admin_state_up": true, 
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
    \n-----END PRIVATE KEY-----",
        "type": "server",
        "update_time": "2017-02-25 09:35:27"
    }
    ```


## 返回码<a name="zh-cn_topic_0096561583_zh-cn_topic_0049139664_section36936567"></a>

请参见[增强型负载均衡返回码说明](增强型负载均衡返回码说明.md)。

