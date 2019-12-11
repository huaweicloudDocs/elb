# 查询API所有版本号<a name="zh-cn_topic_0134546378"></a>

## 功能介绍<a name="section3280114143010"></a>

查询ELB的API所有版本号。

## URI<a name="section1029091414304"></a>

GET /

## 请求消息<a name="section192941514193013"></a>

-   请求参数

    无

-   请求样例

    无


## 响应消息<a name="section12951814123017"></a>

-   响应参数

    **表 1**  响应参数

    <a name="table1829981433014"></a>
    <table><thead align="left"><tr id="row13525171413019"><th class="cellrowborder" valign="top" width="28.23%" id="mcps1.2.4.1.1"><p id="p15256149305"><a name="p15256149305"></a><a name="p15256149305"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="18.83%" id="mcps1.2.4.1.2"><p id="p165251714123013"><a name="p165251714123013"></a><a name="p165251714123013"></a>参数类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="52.94%" id="mcps1.2.4.1.3"><p id="p4448384817"><a name="p4448384817"></a><a name="p4448384817"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row1452511417307"><td class="cellrowborder" valign="top" width="28.23%" headers="mcps1.2.4.1.1 "><p id="p052513142301"><a name="p052513142301"></a><a name="p052513142301"></a>versions</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.83%" headers="mcps1.2.4.1.2 "><p id="p7525131413016"><a name="p7525131413016"></a><a name="p7525131413016"></a>Array</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.94%" headers="mcps1.2.4.1.3 "><p id="p55251814193016"><a name="p55251814193016"></a><a name="p55251814193016"></a>描述version 相关对象的列表。</p>
    </td>
    </tr>
    <tr id="row85258147302"><td class="cellrowborder" valign="top" width="28.23%" headers="mcps1.2.4.1.1 "><p id="p15525131473014"><a name="p15525131473014"></a><a name="p15525131473014"></a>id</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.83%" headers="mcps1.2.4.1.2 "><p id="p1752591416309"><a name="p1752591416309"></a><a name="p1752591416309"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.94%" headers="mcps1.2.4.1.3 "><p id="p6525814133015"><a name="p6525814133015"></a><a name="p6525814133015"></a>版本ID（版本号），如v1。</p>
    </td>
    </tr>
    <tr id="row185251714173016"><td class="cellrowborder" valign="top" width="28.23%" headers="mcps1.2.4.1.1 "><p id="p35258147305"><a name="p35258147305"></a><a name="p35258147305"></a>links</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.83%" headers="mcps1.2.4.1.2 "><p id="p552511411306"><a name="p552511411306"></a><a name="p552511411306"></a>Array</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.94%" headers="mcps1.2.4.1.3 "><p id="p1552541433016"><a name="p1552541433016"></a><a name="p1552541433016"></a>API的URL地址。</p>
    </td>
    </tr>
    <tr id="row55255149303"><td class="cellrowborder" valign="top" width="28.23%" headers="mcps1.2.4.1.1 "><p id="p152514149305"><a name="p152514149305"></a><a name="p152514149305"></a>href</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.83%" headers="mcps1.2.4.1.2 "><p id="p19777202015503"><a name="p19777202015503"></a><a name="p19777202015503"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.94%" headers="mcps1.2.4.1.3 "><p id="p1952661418305"><a name="p1952661418305"></a><a name="p1952661418305"></a>当前API版本的引用地址。</p>
    </td>
    </tr>
    <tr id="row1952661413303"><td class="cellrowborder" valign="top" width="28.23%" headers="mcps1.2.4.1.1 "><p id="p13526121413010"><a name="p13526121413010"></a><a name="p13526121413010"></a>rel</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.83%" headers="mcps1.2.4.1.2 "><p id="p1994962395012"><a name="p1994962395012"></a><a name="p1994962395012"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.94%" headers="mcps1.2.4.1.3 "><p id="p10526131410307"><a name="p10526131410307"></a><a name="p10526131410307"></a>当前API版本和被引用地址的关系。</p>
    </td>
    </tr>
    <tr id="row2052611443013"><td class="cellrowborder" valign="top" width="28.23%" headers="mcps1.2.4.1.1 "><p id="p55263143301"><a name="p55263143301"></a><a name="p55263143301"></a>version</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.83%" headers="mcps1.2.4.1.2 "><p id="p1152601413307"><a name="p1152601413307"></a><a name="p1152601413307"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.94%" headers="mcps1.2.4.1.3 "><p id="p14526514183016"><a name="p14526514183016"></a><a name="p14526514183016"></a>若该版本API支持微版本，则填支持的最大微版本号，如果不支持微版本，则填空</p>
    </td>
    </tr>
    <tr id="row1352681415300"><td class="cellrowborder" valign="top" width="28.23%" headers="mcps1.2.4.1.1 "><p id="p1252631416307"><a name="p1252631416307"></a><a name="p1252631416307"></a>status</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.83%" headers="mcps1.2.4.1.2 "><p id="p16526414193010"><a name="p16526414193010"></a><a name="p16526414193010"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.94%" headers="mcps1.2.4.1.3 "><p id="p1952616141302"><a name="p1952616141302"></a><a name="p1952616141302"></a>版本状态，为如下3种：</p>
    <p id="p17526201417305"><a name="p17526201417305"></a><a name="p17526201417305"></a>CURRENT：表示该版本为主推版本。</p>
    <p id="p19526111420306"><a name="p19526111420306"></a><a name="p19526111420306"></a>SUPPORTED：表示为老版本，但是现在还继续支持。</p>
    <p id="p175261814103010"><a name="p175261814103010"></a><a name="p175261814103010"></a>DEPRECATED：表示为废弃版本，存在后续删除的可能。</p>
    </td>
    </tr>
    <tr id="row17526914113012"><td class="cellrowborder" valign="top" width="28.23%" headers="mcps1.2.4.1.1 "><p id="p352611418308"><a name="p352611418308"></a><a name="p352611418308"></a>updated</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.83%" headers="mcps1.2.4.1.2 "><p id="p8526121414305"><a name="p8526121414305"></a><a name="p8526121414305"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.94%" headers="mcps1.2.4.1.3 "><p id="p1526181453010"><a name="p1526181453010"></a><a name="p1526181453010"></a>版本发布时间，要求用UTC时间表示。如v1发布的时间2014-06-28T12:20:21Z。</p>
    </td>
    </tr>
    <tr id="row852612147307"><td class="cellrowborder" valign="top" width="28.23%" headers="mcps1.2.4.1.1 "><p id="p952651415305"><a name="p952651415305"></a><a name="p952651415305"></a>min_version</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.83%" headers="mcps1.2.4.1.2 "><p id="p6189633115014"><a name="p6189633115014"></a><a name="p6189633115014"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.94%" headers="mcps1.2.4.1.3 "><p id="p16526914193017"><a name="p16526914193017"></a><a name="p16526914193017"></a>若该版本API 支持微版本，则填支持的最小微版本号，如果不支持微版本，则填空。</p>
    </td>
    </tr>
    </tbody>
    </table>

-   响应样例

    ```
    { 
       "versions": [ 
         { 
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
       ] 
     }
    ```


## 状态码<a name="section163541714123020"></a>

-   正常

    200

-   异常

    <a name="table835781418301"></a>
    <table><thead align="left"><tr id="row9526214113014"><th class="cellrowborder" valign="top" width="12.13%" id="mcps1.1.4.1.1"><p id="p1352614149300"><a name="p1352614149300"></a><a name="p1352614149300"></a>状态码</p>
    </th>
    <th class="cellrowborder" valign="top" width="52.38%" id="mcps1.1.4.1.2"><p id="p522343074810"><a name="p522343074810"></a><a name="p522343074810"></a>编码</p>
    </th>
    <th class="cellrowborder" valign="top" width="35.49%" id="mcps1.1.4.1.3"><p id="p1952681473010"><a name="p1952681473010"></a><a name="p1952681473010"></a>错误码说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row1752691483011"><td class="cellrowborder" valign="top" width="12.13%" headers="mcps1.1.4.1.1 "><p id="p1052641493017"><a name="p1052641493017"></a><a name="p1052641493017"></a>400</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.38%" headers="mcps1.1.4.1.2 "><p id="p5421540134813"><a name="p5421540134813"></a><a name="p5421540134813"></a>Bad Request</p>
    </td>
    <td class="cellrowborder" valign="top" width="35.49%" headers="mcps1.1.4.1.3 "><p id="p125261414183017"><a name="p125261414183017"></a><a name="p125261414183017"></a>请求错误。</p>
    </td>
    </tr>
    <tr id="row1352613145300"><td class="cellrowborder" valign="top" width="12.13%" headers="mcps1.1.4.1.1 "><p id="p16526314133013"><a name="p16526314133013"></a><a name="p16526314133013"></a>401</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.38%" headers="mcps1.1.4.1.2 "><p id="p104212040164813"><a name="p104212040164813"></a><a name="p104212040164813"></a>Unauthorized</p>
    </td>
    <td class="cellrowborder" valign="top" width="35.49%" headers="mcps1.1.4.1.3 "><p id="p85261914163019"><a name="p85261914163019"></a><a name="p85261914163019"></a>未提供认证信息，或认证信息错。</p>
    </td>
    </tr>
    <tr id="row135261014163016"><td class="cellrowborder" valign="top" width="12.13%" headers="mcps1.1.4.1.1 "><p id="p352611140306"><a name="p352611140306"></a><a name="p352611140306"></a>403</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.38%" headers="mcps1.1.4.1.2 "><p id="p74211540154810"><a name="p74211540154810"></a><a name="p74211540154810"></a>Forbidden</p>
    </td>
    <td class="cellrowborder" valign="top" width="35.49%" headers="mcps1.1.4.1.3 "><p id="p552681412306"><a name="p552681412306"></a><a name="p552681412306"></a>请求页面被禁止访问。</p>
    </td>
    </tr>
    <tr id="row18526414193016"><td class="cellrowborder" valign="top" width="12.13%" headers="mcps1.1.4.1.1 "><p id="p3526914183011"><a name="p3526914183011"></a><a name="p3526914183011"></a>404</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.38%" headers="mcps1.1.4.1.2 "><p id="p4421104084819"><a name="p4421104084819"></a><a name="p4421104084819"></a>Not Found</p>
    </td>
    <td class="cellrowborder" valign="top" width="35.49%" headers="mcps1.1.4.1.3 "><p id="p13526161419305"><a name="p13526161419305"></a><a name="p13526161419305"></a>请求资源不存在</p>
    </td>
    </tr>
    <tr id="row55268146301"><td class="cellrowborder" valign="top" width="12.13%" headers="mcps1.1.4.1.1 "><p id="p1852613141307"><a name="p1852613141307"></a><a name="p1852613141307"></a>408</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.38%" headers="mcps1.1.4.1.2 "><p id="p142174084820"><a name="p142174084820"></a><a name="p142174084820"></a>Request Timeout</p>
    </td>
    <td class="cellrowborder" valign="top" width="35.49%" headers="mcps1.1.4.1.3 "><p id="p11526171443016"><a name="p11526171443016"></a><a name="p11526171443016"></a>请求超出了服务器的等待时间。</p>
    </td>
    </tr>
    <tr id="row195266148306"><td class="cellrowborder" valign="top" width="12.13%" headers="mcps1.1.4.1.1 "><p id="p1152611410307"><a name="p1152611410307"></a><a name="p1152611410307"></a>429</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.38%" headers="mcps1.1.4.1.2 "><p id="p6421184013488"><a name="p6421184013488"></a><a name="p6421184013488"></a>Too Many Requests</p>
    </td>
    <td class="cellrowborder" valign="top" width="35.49%" headers="mcps1.1.4.1.3 "><p id="p1952651416303"><a name="p1952651416303"></a><a name="p1952651416303"></a>当前请求过多。</p>
    </td>
    </tr>
    <tr id="row452671473019"><td class="cellrowborder" valign="top" width="12.13%" headers="mcps1.1.4.1.1 "><p id="p4526214123016"><a name="p4526214123016"></a><a name="p4526214123016"></a>500</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.38%" headers="mcps1.1.4.1.2 "><p id="p8421940124817"><a name="p8421940124817"></a><a name="p8421940124817"></a>Internal Server Error</p>
    </td>
    <td class="cellrowborder" valign="top" width="35.49%" headers="mcps1.1.4.1.3 "><p id="p14528101418306"><a name="p14528101418306"></a><a name="p14528101418306"></a>请求未完成，服务异常。</p>
    </td>
    </tr>
    <tr id="row18528201420300"><td class="cellrowborder" valign="top" width="12.13%" headers="mcps1.1.4.1.1 "><p id="p352851417307"><a name="p352851417307"></a><a name="p352851417307"></a>503</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.38%" headers="mcps1.1.4.1.2 "><p id="p164211440114815"><a name="p164211440114815"></a><a name="p164211440114815"></a>Service Unavailable</p>
    </td>
    <td class="cellrowborder" valign="top" width="35.49%" headers="mcps1.1.4.1.3 "><p id="p1852851403019"><a name="p1852851403019"></a><a name="p1852851403019"></a>系统暂时不可用，请求受限。</p>
    </td>
    </tr>
    </tbody>
    </table>


