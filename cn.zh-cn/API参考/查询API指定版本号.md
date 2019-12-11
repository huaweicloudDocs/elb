# 查询API指定版本号<a name="zh-cn_topic_0134546379"></a>

## 功能介绍<a name="section9828101517313"></a>

查询ELB的API指定版本号。

## URI<a name="section13830201510315"></a>

GET /\{api\_version\}

**表 1**  参数说明

<a name="table383815150316"></a>
<table><thead align="left"><tr id="row1614121683114"><th class="cellrowborder" valign="top" width="19.39%" id="mcps1.2.4.1.1"><p id="p111411516173117"><a name="p111411516173117"></a><a name="p111411516173117"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20.41%" id="mcps1.2.4.1.2"><p id="p2014121613110"><a name="p2014121613110"></a><a name="p2014121613110"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="60.199999999999996%" id="mcps1.2.4.1.3"><p id="p81411416113111"><a name="p81411416113111"></a><a name="p81411416113111"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row2142716173114"><td class="cellrowborder" valign="top" width="19.39%" headers="mcps1.2.4.1.1 "><p id="p11142121613118"><a name="p11142121613118"></a><a name="p11142121613118"></a>api_version</p>
</td>
<td class="cellrowborder" valign="top" width="20.41%" headers="mcps1.2.4.1.2 "><p id="p17142191619318"><a name="p17142191619318"></a><a name="p17142191619318"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="60.199999999999996%" headers="mcps1.2.4.1.3 "><p id="p1914201643118"><a name="p1914201643118"></a><a name="p1914201643118"></a>API版本号。</p>
</td>
</tr>
</tbody>
</table>

-   样例

    /v1.0


## 请求消息<a name="section9847121516313"></a>

-   请求参数

    无

-   请求样例

    无


## 响应消息<a name="section884711159311"></a>

-   响应参数

    **表 2**  响应参数

    <a name="table14855415113115"></a>
    <table><thead align="left"><tr id="row10142191613119"><th class="cellrowborder" valign="top" width="28.23%" id="mcps1.2.4.1.1"><p id="p181421162310"><a name="p181421162310"></a><a name="p181421162310"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="18.83%" id="mcps1.2.4.1.2"><p id="p17142181683113"><a name="p17142181683113"></a><a name="p17142181683113"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="52.94%" id="mcps1.2.4.1.3"><p id="p1614215167317"><a name="p1614215167317"></a><a name="p1614215167317"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row1914316163317"><td class="cellrowborder" valign="top" width="28.23%" headers="mcps1.2.4.1.1 "><p id="p814319169314"><a name="p814319169314"></a><a name="p814319169314"></a>version</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.83%" headers="mcps1.2.4.1.2 "><p id="p3143151663113"><a name="p3143151663113"></a><a name="p3143151663113"></a>Object</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.94%" headers="mcps1.2.4.1.3 "><p id="p17143116143116"><a name="p17143116143116"></a><a name="p17143116143116"></a>描述version 相关对象。</p>
    </td>
    </tr>
    <tr id="row201431116183115"><td class="cellrowborder" valign="top" width="28.23%" headers="mcps1.2.4.1.1 "><p id="p1514341613117"><a name="p1514341613117"></a><a name="p1514341613117"></a>id</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.83%" headers="mcps1.2.4.1.2 "><p id="p1650194025018"><a name="p1650194025018"></a><a name="p1650194025018"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.94%" headers="mcps1.2.4.1.3 "><p id="p8143161603116"><a name="p8143161603116"></a><a name="p8143161603116"></a>版本ID（版本号），如v1。</p>
    </td>
    </tr>
    <tr id="row1314318166312"><td class="cellrowborder" valign="top" width="28.23%" headers="mcps1.2.4.1.1 "><p id="p1514351683110"><a name="p1514351683110"></a><a name="p1514351683110"></a>links</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.83%" headers="mcps1.2.4.1.2 "><p id="p998517393811"><a name="p998517393811"></a><a name="p998517393811"></a>Array</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.94%" headers="mcps1.2.4.1.3 "><p id="p131431416103116"><a name="p131431416103116"></a><a name="p131431416103116"></a>API的URL地址。</p>
    </td>
    </tr>
    <tr id="row71431616123117"><td class="cellrowborder" valign="top" width="28.23%" headers="mcps1.2.4.1.1 "><p id="p17144216173119"><a name="p17144216173119"></a><a name="p17144216173119"></a>href</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.83%" headers="mcps1.2.4.1.2 "><p id="p61444162310"><a name="p61444162310"></a><a name="p61444162310"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.94%" headers="mcps1.2.4.1.3 "><p id="p16144131619312"><a name="p16144131619312"></a><a name="p16144131619312"></a>当前API版本的引用地址。</p>
    </td>
    </tr>
    <tr id="row0144141615318"><td class="cellrowborder" valign="top" width="28.23%" headers="mcps1.2.4.1.1 "><p id="p114471623115"><a name="p114471623115"></a><a name="p114471623115"></a>rel</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.83%" headers="mcps1.2.4.1.2 "><p id="p11444164317"><a name="p11444164317"></a><a name="p11444164317"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.94%" headers="mcps1.2.4.1.3 "><p id="p13144416113118"><a name="p13144416113118"></a><a name="p13144416113118"></a>当前API版本和被引用地址的关系。</p>
    </td>
    </tr>
    <tr id="row15144101663113"><td class="cellrowborder" valign="top" width="28.23%" headers="mcps1.2.4.1.1 "><p id="p0144151653113"><a name="p0144151653113"></a><a name="p0144151653113"></a>version</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.83%" headers="mcps1.2.4.1.2 "><p id="p191441816153116"><a name="p191441816153116"></a><a name="p191441816153116"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.94%" headers="mcps1.2.4.1.3 "><p id="p10144316163113"><a name="p10144316163113"></a><a name="p10144316163113"></a>若该版本API支持微版本，则填支持的最大微版本号，如果不支持微版本，则填空</p>
    </td>
    </tr>
    <tr id="row1014481653115"><td class="cellrowborder" valign="top" width="28.23%" headers="mcps1.2.4.1.1 "><p id="p51448168312"><a name="p51448168312"></a><a name="p51448168312"></a>status</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.83%" headers="mcps1.2.4.1.2 "><p id="p238824715508"><a name="p238824715508"></a><a name="p238824715508"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.94%" headers="mcps1.2.4.1.3 "><p id="p1414441612319"><a name="p1414441612319"></a><a name="p1414441612319"></a>版本状态，为如下3种：</p>
    <p id="p1214451614316"><a name="p1214451614316"></a><a name="p1214451614316"></a>CURRENT：表示该版本为主推版本。</p>
    <p id="p514491683115"><a name="p514491683115"></a><a name="p514491683115"></a>SUPPORTED：表示为老版本，但是现在还继续支持。</p>
    <p id="p81441816153119"><a name="p81441816153119"></a><a name="p81441816153119"></a>DEPRECATED：表示为废弃版本，存在后续删除的可能。</p>
    </td>
    </tr>
    <tr id="row1714401617318"><td class="cellrowborder" valign="top" width="28.23%" headers="mcps1.2.4.1.1 "><p id="p131441316163111"><a name="p131441316163111"></a><a name="p131441316163111"></a>updated</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.83%" headers="mcps1.2.4.1.2 "><p id="p19144101617317"><a name="p19144101617317"></a><a name="p19144101617317"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.94%" headers="mcps1.2.4.1.3 "><p id="p141449168315"><a name="p141449168315"></a><a name="p141449168315"></a>版本发布时间，要求用UTC时间表示。如v1发布的时间2014-06-28T12:20:21Z。</p>
    </td>
    </tr>
    <tr id="row15144316203118"><td class="cellrowborder" valign="top" width="28.23%" headers="mcps1.2.4.1.1 "><p id="p17144716183112"><a name="p17144716183112"></a><a name="p17144716183112"></a>min_version</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.83%" headers="mcps1.2.4.1.2 "><p id="p91441316193117"><a name="p91441316193117"></a><a name="p91441316193117"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.94%" headers="mcps1.2.4.1.3 "><p id="p514413164311"><a name="p514413164311"></a><a name="p514413164311"></a>若该版本API 支持微版本，则填支持的最小微版本号，如果不支持微版本，则填空。</p>
    </td>
    </tr>
    </tbody>
    </table>

-   响应样例

    ```
    {  
       "version": {  
           "id": "v1.0",  
           "links": [  
             {  
               "href": "https://{elb_endpoint}/v1.0/",  
               "rel": "self"  
             }  
           ],  
           "min_version": "",  
           "status": "CURRENT",  
           "updated": "2018-09-30T00:00:00Z",  
           "version": ""  
         }  
     }
    ```


## 状态码<a name="section1792221513312"></a>

-   正常

    200

-   异常

    <a name="table792881519311"></a>
    <table><thead align="left"><tr id="row1114621620318"><th class="cellrowborder" valign="top" width="10.040000000000001%" id="mcps1.1.4.1.1"><p id="p81466162315"><a name="p81466162315"></a><a name="p81466162315"></a>状态码</p>
    </th>
    <th class="cellrowborder" valign="top" width="54.47%" id="mcps1.1.4.1.2"><p id="p4515643155516"><a name="p4515643155516"></a><a name="p4515643155516"></a>编码</p>
    </th>
    <th class="cellrowborder" valign="top" width="35.49%" id="mcps1.1.4.1.3"><p id="p1714611611311"><a name="p1714611611311"></a><a name="p1714611611311"></a>错误码说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row10146141643115"><td class="cellrowborder" valign="top" width="10.040000000000001%" headers="mcps1.1.4.1.1 "><p id="p2146716183117"><a name="p2146716183117"></a><a name="p2146716183117"></a>400</p>
    </td>
    <td class="cellrowborder" valign="top" width="54.47%" headers="mcps1.1.4.1.2 "><p id="p2040805665518"><a name="p2040805665518"></a><a name="p2040805665518"></a>Bad Request</p>
    </td>
    <td class="cellrowborder" valign="top" width="35.49%" headers="mcps1.1.4.1.3 "><p id="p8146121673119"><a name="p8146121673119"></a><a name="p8146121673119"></a>请求错误。</p>
    </td>
    </tr>
    <tr id="row714611614312"><td class="cellrowborder" valign="top" width="10.040000000000001%" headers="mcps1.1.4.1.1 "><p id="p181461516163118"><a name="p181461516163118"></a><a name="p181461516163118"></a>401</p>
    </td>
    <td class="cellrowborder" valign="top" width="54.47%" headers="mcps1.1.4.1.2 "><p id="p10409556105516"><a name="p10409556105516"></a><a name="p10409556105516"></a>Unauthorized</p>
    </td>
    <td class="cellrowborder" valign="top" width="35.49%" headers="mcps1.1.4.1.3 "><p id="p18146111643116"><a name="p18146111643116"></a><a name="p18146111643116"></a>未提供认证信息，或认证信息错。</p>
    </td>
    </tr>
    <tr id="row16146316103114"><td class="cellrowborder" valign="top" width="10.040000000000001%" headers="mcps1.1.4.1.1 "><p id="p12146516113114"><a name="p12146516113114"></a><a name="p12146516113114"></a>403</p>
    </td>
    <td class="cellrowborder" valign="top" width="54.47%" headers="mcps1.1.4.1.2 "><p id="p104095561552"><a name="p104095561552"></a><a name="p104095561552"></a>Forbidden</p>
    </td>
    <td class="cellrowborder" valign="top" width="35.49%" headers="mcps1.1.4.1.3 "><p id="p1814621615316"><a name="p1814621615316"></a><a name="p1814621615316"></a>请求页面被禁止访问。</p>
    </td>
    </tr>
    <tr id="row10146191663115"><td class="cellrowborder" valign="top" width="10.040000000000001%" headers="mcps1.1.4.1.1 "><p id="p191461016143116"><a name="p191461016143116"></a><a name="p191461016143116"></a>404</p>
    </td>
    <td class="cellrowborder" valign="top" width="54.47%" headers="mcps1.1.4.1.2 "><p id="p4409165613553"><a name="p4409165613553"></a><a name="p4409165613553"></a>Not Found</p>
    </td>
    <td class="cellrowborder" valign="top" width="35.49%" headers="mcps1.1.4.1.3 "><p id="p121462165314"><a name="p121462165314"></a><a name="p121462165314"></a>请求资源不存在</p>
    </td>
    </tr>
    <tr id="row1146151613111"><td class="cellrowborder" valign="top" width="10.040000000000001%" headers="mcps1.1.4.1.1 "><p id="p7146201603114"><a name="p7146201603114"></a><a name="p7146201603114"></a>408</p>
    </td>
    <td class="cellrowborder" valign="top" width="54.47%" headers="mcps1.1.4.1.2 "><p id="p12409115645514"><a name="p12409115645514"></a><a name="p12409115645514"></a>Request Timeout</p>
    </td>
    <td class="cellrowborder" valign="top" width="35.49%" headers="mcps1.1.4.1.3 "><p id="p71475166314"><a name="p71475166314"></a><a name="p71475166314"></a>请求超出了服务器的等待时间。</p>
    </td>
    </tr>
    <tr id="row514710169314"><td class="cellrowborder" valign="top" width="10.040000000000001%" headers="mcps1.1.4.1.1 "><p id="p161471416173110"><a name="p161471416173110"></a><a name="p161471416173110"></a>429</p>
    </td>
    <td class="cellrowborder" valign="top" width="54.47%" headers="mcps1.1.4.1.2 "><p id="p1040914561558"><a name="p1040914561558"></a><a name="p1040914561558"></a>Too Many Requests</p>
    </td>
    <td class="cellrowborder" valign="top" width="35.49%" headers="mcps1.1.4.1.3 "><p id="p31471116103115"><a name="p31471116103115"></a><a name="p31471116103115"></a>当前请求过多。</p>
    </td>
    </tr>
    <tr id="row11147141610314"><td class="cellrowborder" valign="top" width="10.040000000000001%" headers="mcps1.1.4.1.1 "><p id="p1814731615311"><a name="p1814731615311"></a><a name="p1814731615311"></a>500</p>
    </td>
    <td class="cellrowborder" valign="top" width="54.47%" headers="mcps1.1.4.1.2 "><p id="p17409185610558"><a name="p17409185610558"></a><a name="p17409185610558"></a>Internal Server Error</p>
    </td>
    <td class="cellrowborder" valign="top" width="35.49%" headers="mcps1.1.4.1.3 "><p id="p214715161310"><a name="p214715161310"></a><a name="p214715161310"></a>请求未完成，服务异常。</p>
    </td>
    </tr>
    <tr id="row714701613314"><td class="cellrowborder" valign="top" width="10.040000000000001%" headers="mcps1.1.4.1.1 "><p id="p01474166312"><a name="p01474166312"></a><a name="p01474166312"></a>503</p>
    </td>
    <td class="cellrowborder" valign="top" width="54.47%" headers="mcps1.1.4.1.2 "><p id="p84091256155518"><a name="p84091256155518"></a><a name="p84091256155518"></a>Service Unavailable</p>
    </td>
    <td class="cellrowborder" valign="top" width="35.49%" headers="mcps1.1.4.1.3 "><p id="p1014717162317"><a name="p1014717162317"></a><a name="p1014717162317"></a>系统暂时不可用，请求受限。</p>
    </td>
    </tr>
    </tbody>
    </table>


