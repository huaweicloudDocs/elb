# 添加HTTPS监听器<a name="elb_ug_jt_0009"></a>

## 操作场景<a name="section13358194520513"></a>

HTTPS协议适用于需要加密传输的应用。您可以添加一个HTTPS监听转发来自HTTPS协议的请求。ELB对于用户的HTTPS的请求进行解密，然后发送至后端服务器；后端服务器处理完请求后的返回包首先发送至ELB，由ELB进行加密后，再传回用户侧。

如果您不希望负载均衡器对HTTPS流量进行解密，可以通过配置相同端口的TCP监听器将HTTPS流量透传到后端服务器。具体原理参见[TCP监听器将HTTPS流量透传到后端服务器](#section19187181715231)。

## 添加增强型负载均衡HTTPS监听器<a name="section18262194013551"></a>

1.  登录管理控制台。
2.  在管理控制台左上角单击![](figures/zh-cn_image_0167652152.jpg)图标，选择区域和项目。
3.  选择“服务列表 \> 网络 \> 弹性负载均衡”。
4.  在“负载均衡器”界面，单击需要添加监听器的负载均衡名称。
5.  切换到“监听器”页签，单击“添加监听器”。
6.  配置监听器参数参见[表1](#table20377204713512)，单击“下一步”。

    **表 1**  增强型负载均衡配置监听器参数说明

    <a name="table20377204713512"></a>
    <table><thead align="left"><tr id="row1337215478357"><th class="cellrowborder" valign="top" width="23.41%" id="mcps1.2.4.1.1"><p id="p13372647103517"><a name="p13372647103517"></a><a name="p13372647103517"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="46.73%" id="mcps1.2.4.1.2"><p id="p15372647173513"><a name="p15372647173513"></a><a name="p15372647173513"></a>说明</p>
    </th>
    <th class="cellrowborder" valign="top" width="29.86%" id="mcps1.2.4.1.3"><p id="p13372647193520"><a name="p13372647193520"></a><a name="p13372647193520"></a>示例</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row113721747113516"><td class="cellrowborder" valign="top" width="23.41%" headers="mcps1.2.4.1.1 "><p id="p237294719359"><a name="p237294719359"></a><a name="p237294719359"></a>名称</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.73%" headers="mcps1.2.4.1.2 "><p id="p103726475354"><a name="p103726475354"></a><a name="p103726475354"></a>监听器名称。</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.86%" headers="mcps1.2.4.1.3 "><p id="p1237254713352"><a name="p1237254713352"></a><a name="p1237254713352"></a>listener-pnqy</p>
    </td>
    </tr>
    <tr id="row6373114743514"><td class="cellrowborder" valign="top" width="23.41%" headers="mcps1.2.4.1.1 "><p id="p937284733516"><a name="p937284733516"></a><a name="p937284733516"></a>前端协议/端口</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.73%" headers="mcps1.2.4.1.2 "><p id="p10373347163514"><a name="p10373347163514"></a><a name="p10373347163514"></a>负载分发的协议和端口。</p>
    <p id="p1373124793517"><a name="p1373124793517"></a><a name="p1373124793517"></a>选择HTTPS协议，端口取值范围[1-65535]。</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.86%" headers="mcps1.2.4.1.3 "><p id="p63739472356"><a name="p63739472356"></a><a name="p63739472356"></a>HTTPS/80</p>
    </td>
    </tr>
    <tr id="row1374147203519"><td class="cellrowborder" valign="top" width="23.41%" headers="mcps1.2.4.1.1 "><p id="p1737424715353"><a name="p1737424715353"></a><a name="p1737424715353"></a>服务器证书</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.73%" headers="mcps1.2.4.1.2 "><p id="p1837404717359"><a name="p1837404717359"></a><a name="p1837404717359"></a>协议类型为HTTPS时，需使用证书。</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.86%" headers="mcps1.2.4.1.3 "><p id="p1037414773517"><a name="p1037414773517"></a><a name="p1037414773517"></a>-</p>
    </td>
    </tr>
    <tr id="row2375154793512"><td class="cellrowborder" valign="top" width="23.41%" headers="mcps1.2.4.1.1 "><p id="p837454714357"><a name="p837454714357"></a><a name="p837454714357"></a>开启SNI</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.73%" headers="mcps1.2.4.1.2 "><p id="p19374164710355"><a name="p19374164710355"></a><a name="p19374164710355"></a>HTTPS协议的负载均衡选择是否开启SNI。</p>
    <p id="p133749470350"><a name="p133749470350"></a><a name="p133749470350"></a>SNI是为了解决一个服务器使用多个域名和证书的TLS扩展。开启SNI后，允许客户端在发起SSL握手请求时就提交请求的域名信息，ELB收到SSL请求后，会根据域名去查找证书，如果找到域名对应的证书，则返回该证书；如果没有找到域名对应的证书，则返回缺省证书。</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.86%" headers="mcps1.2.4.1.3 "><p id="p43753478353"><a name="p43753478353"></a><a name="p43753478353"></a>-</p>
    </td>
    </tr>
    <tr id="row737534793511"><td class="cellrowborder" valign="top" width="23.41%" headers="mcps1.2.4.1.1 "><p id="p237520471355"><a name="p237520471355"></a><a name="p237520471355"></a>SNI证书</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.73%" headers="mcps1.2.4.1.2 "><p id="p1637584716351"><a name="p1637584716351"></a><a name="p1637584716351"></a>HTTPS协议的负载均衡设置开启SNI后需要选择域名对应的证书。</p>
    <p id="p17375547153514"><a name="p17375547153514"></a><a name="p17375547153514"></a>可选择已创建或者创建新的SNI证书。</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.86%" headers="mcps1.2.4.1.3 "><p id="p103751347123519"><a name="p103751347123519"></a><a name="p103751347123519"></a>-</p>
    </td>
    </tr>
    <tr id="row2375164733519"><td class="cellrowborder" valign="top" width="23.41%" headers="mcps1.2.4.1.1 "><p id="p337544716354"><a name="p337544716354"></a><a name="p337544716354"></a>高级配置</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.73%" headers="mcps1.2.4.1.2 "><p id="p183751847203516"><a name="p183751847203516"></a><a name="p183751847203516"></a>可以自定义设置更多功能。</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.86%" headers="mcps1.2.4.1.3 "><p id="p19375154703512"><a name="p19375154703512"></a><a name="p19375154703512"></a>-</p>
    </td>
    </tr>
    <tr id="row737613471354"><td class="cellrowborder" valign="top" width="23.41%" headers="mcps1.2.4.1.1 "><p id="p2375047103512"><a name="p2375047103512"></a><a name="p2375047103512"></a>HTTP/2</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.73%" headers="mcps1.2.4.1.2 "><p id="p14375174712352"><a name="p14375174712352"></a><a name="p14375174712352"></a>协议类型为HTTPS时,可选择是否支持该协议类型。</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.86%" headers="mcps1.2.4.1.3 "><p id="p133761447133520"><a name="p133761447133520"></a><a name="p133761447133520"></a>-</p>
    </td>
    </tr>
    <tr id="row8376247103520"><td class="cellrowborder" valign="top" width="23.41%" headers="mcps1.2.4.1.1 "><p id="p1937624713351"><a name="p1937624713351"></a><a name="p1937624713351"></a>获取弹性公网IP</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.73%" headers="mcps1.2.4.1.2 "><p id="p1837614713512"><a name="p1837614713512"></a><a name="p1837614713512"></a>协议类型为HTTPS时，可根据需要设置该项。若您需要将ELB公网IP透传到后端，只需在创建HTTPS监听器时，打开该开关。</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.86%" headers="mcps1.2.4.1.3 "><p id="p837617479359"><a name="p837617479359"></a><a name="p837617479359"></a>-</p>
    </td>
    </tr>
    <tr id="row737615478354"><td class="cellrowborder" valign="top" width="23.41%" headers="mcps1.2.4.1.1 "><p id="p33761947113512"><a name="p33761947113512"></a><a name="p33761947113512"></a>双向认证</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.73%" headers="mcps1.2.4.1.2 "><p id="p6376184743520"><a name="p6376184743520"></a><a name="p6376184743520"></a>用户需要在HTTPS监听上同时绑定服务器证书与CA证书，才能进行服务端与客户端的双向认证。</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.86%" headers="mcps1.2.4.1.3 "><p id="p43761547103513"><a name="p43761547103513"></a><a name="p43761547103513"></a>-</p>
    </td>
    </tr>
    <tr id="row537615472358"><td class="cellrowborder" valign="top" width="23.41%" headers="mcps1.2.4.1.1 "><p id="p17376747203516"><a name="p17376747203516"></a><a name="p17376747203516"></a>CA证书</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.73%" headers="mcps1.2.4.1.2 "><p id="p937620473356"><a name="p937620473356"></a><a name="p937620473356"></a>协议类型为HTTPS时，需使用证书。且双向认证开关打开时为必选参数。</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.86%" headers="mcps1.2.4.1.3 "><p id="p1737684783517"><a name="p1737684783517"></a><a name="p1737684783517"></a>-</p>
    </td>
    </tr>
    <tr id="row143761647163518"><td class="cellrowborder" valign="top" width="23.41%" headers="mcps1.2.4.1.1 "><p id="p237634710356"><a name="p237634710356"></a><a name="p237634710356"></a>描述</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.73%" headers="mcps1.2.4.1.2 "><p id="p23761447103512"><a name="p23761447103512"></a><a name="p23761447103512"></a>对于监听器描述。</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.86%" headers="mcps1.2.4.1.3 "><p id="p437644773515"><a name="p437644773515"></a><a name="p437644773515"></a>-</p>
    </td>
    </tr>
    </tbody>
    </table>

7.  配置后端服务器组参数参见[表2](#table3561446373)，配置健康检查参数参见[表3](#table95680412371)，单击“完成”。

    **表 2**  增强型负载均衡配置后端服务器组参数说明

    <a name="table3561446373"></a>
    <table><thead align="left"><tr id="row11555104193715"><th class="cellrowborder" valign="top" width="23.419999999999998%" id="mcps1.2.4.1.1"><p id="p85551445373"><a name="p85551445373"></a><a name="p85551445373"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="46.72%" id="mcps1.2.4.1.2"><p id="p185555413375"><a name="p185555413375"></a><a name="p185555413375"></a>说明</p>
    </th>
    <th class="cellrowborder" valign="top" width="29.86%" id="mcps1.2.4.1.3"><p id="p755524163717"><a name="p755524163717"></a><a name="p755524163717"></a>示例</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row95561142372"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p1255518414378"><a name="p1255518414378"></a><a name="p1255518414378"></a>后端<span id="text201521911135314"><a name="text201521911135314"></a><a name="text201521911135314"></a>服务器</span>组</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.72%" headers="mcps1.2.4.1.2 "><p id="p1155517417374"><a name="p1155517417374"></a><a name="p1155517417374"></a>把具有相同特性的后端<span id="text261117326535"><a name="text261117326535"></a><a name="text261117326535"></a>服务器</span>放在一个组。</p>
    <a name="ul35562047371"></a><a name="ul35562047371"></a><ul id="ul35562047371"><li>新创建</li><li>使用已有</li></ul>
    </td>
    <td class="cellrowborder" valign="top" width="29.86%" headers="mcps1.2.4.1.3 "><p id="p18556194173710"><a name="p18556194173710"></a><a name="p18556194173710"></a>新创建</p>
    </td>
    </tr>
    <tr id="row1955634173711"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p195565417375"><a name="p195565417375"></a><a name="p195565417375"></a>名称</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.72%" headers="mcps1.2.4.1.2 "><p id="p155569413712"><a name="p155569413712"></a><a name="p155569413712"></a>后端<span id="text15466639115312"><a name="text15466639115312"></a><a name="text15466639115312"></a>服务器</span>组名称。</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.86%" headers="mcps1.2.4.1.3 "><p id="p655618416379"><a name="p655618416379"></a><a name="p655618416379"></a>server_group-sq4v</p>
    </td>
    </tr>
    <tr id="row3556114153716"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p1655616416379"><a name="p1655616416379"></a><a name="p1655616416379"></a>后端协议</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.72%" headers="mcps1.2.4.1.2 "><p id="p9556184133715"><a name="p9556184133715"></a><a name="p9556184133715"></a>云服务开通的协议。默认HTTP。</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.86%" headers="mcps1.2.4.1.3 "><p id="p3556348372"><a name="p3556348372"></a><a name="p3556348372"></a>HTTP</p>
    </td>
    </tr>
    <tr id="row555915403715"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p1755654113720"><a name="p1755654113720"></a><a name="p1755654113720"></a>分配策略类型</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.72%" headers="mcps1.2.4.1.2 "><p id="p175561746372"><a name="p175561746372"></a><a name="p175561746372"></a>负载均衡采用的算法。</p>
    <a name="ul95599453720"></a><a name="ul95599453720"></a><ul id="ul95599453720"><li>加权轮询算法：根据后端服务器的权重，按顺序依次将请求分发给不同的服务器。它用相应的权重表示服务器的处理性能，按照权重的高低以及轮询方式将请求分配给各服务器，相同权重的服务器处理相同数目的连接数。</li><li>加权最少连接：最少连接是通过当前活跃的连接数来估计服务器负载情况的一种动态调度算法。加权最少连接就是在最少连接数的基础上，根据服务器的不同处理能力，给每个服务器分配不同的权重，使其能够接受相应权值数的服务请求。</li><li>源IP算法：将请求的源IP地址进行Hash运算，得到一个具体的数值，同时对后端服务器进行编号，按照运算结果将请求分发到对应编号的服务器上。这可以使得对不同源IP的访问进行负载分发，同时使得同一个客户端IP的请求始终被派发至某特定的服务器。</li></ul>
    <div class="note" id="note7559845371"><a name="note7559845371"></a><a name="note7559845371"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="zh-cn_topic_0167652121_ul77115484370"></a><a name="zh-cn_topic_0167652121_ul77115484370"></a><ul id="zh-cn_topic_0167652121_ul77115484370"><li>用户可以根据自身需求选择相应的算法来分配用户访问流量，提升负载均衡能力。</li><li>对于加权轮询算法和加权最少连接，当服务器的权重为“0”时，将不会被分发访问请求。</li></ul>
    </div></div>
    </td>
    <td class="cellrowborder" valign="top" width="29.86%" headers="mcps1.2.4.1.3 "><p id="p105591463716"><a name="p105591463716"></a><a name="p105591463716"></a>加权轮询算法</p>
    </td>
    </tr>
    <tr id="row25605412371"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p15559104143712"><a name="p15559104143712"></a><a name="p15559104143712"></a>会话保持</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.72%" headers="mcps1.2.4.1.2 "><p id="p75601413375"><a name="p75601413375"></a><a name="p75601413375"></a>开启会话保持后，弹性负载均衡将属于同一个会话的请求都转发到同一个<span id="text1034734815317"><a name="text1034734815317"></a><a name="text1034734815317"></a>服务器</span>进行处理。</p>
    <div class="note" id="note14560848376"><a name="note14560848376"></a><a name="note14560848376"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="zh-cn_topic_0167652123_ul18240191212514"></a><a name="zh-cn_topic_0167652123_ul18240191212514"></a><ul id="zh-cn_topic_0167652123_ul18240191212514"><li>当分配策略类型为“加权轮询算法”时，可配置会话保持。</li><li>对于HTTP类型的监听器，变更会话保持的状态可能会导致本监听器访问出现秒级中断。</li></ul>
    </div></div>
    </td>
    <td class="cellrowborder" valign="top" width="29.86%" headers="mcps1.2.4.1.3 "><p id="p256011415372"><a name="p256011415372"></a><a name="p256011415372"></a>-</p>
    </td>
    </tr>
    <tr id="row8560204133710"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p17560144143718"><a name="p17560144143718"></a><a name="p17560144143718"></a>会话保持类型</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.72%" headers="mcps1.2.4.1.2 "><p id="p125601473720"><a name="p125601473720"></a><a name="p125601473720"></a>HTTPS协议支持HTTP cookie和应用程序 cookie类型。用户可根据自身需求选择相应的会话保持方式来分配用户访问流量，提升负载均衡能力。</p>
    <a name="ul156013423719"></a><a name="ul156013423719"></a><ul id="ul156013423719"><li>HTTP&nbsp;cookie：负载均衡器会根据客户端第一个请求生成一个cookie，后续所有包含这个cookie值的请求都会由同一个后端服务器处理。</li><li>应用程序cookie：该选项依赖于后端应用。后端应用生成一个cookie值，后续所有包含这个cookie值的请求都会由同一个后端服务器处理。</li></ul>
    </td>
    <td class="cellrowborder" valign="top" width="29.86%" headers="mcps1.2.4.1.3 "><p id="p1156044163717"><a name="p1156044163717"></a><a name="p1156044163717"></a>HTTP&nbsp;cookie</p>
    </td>
    </tr>
    <tr id="row195616413713"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p856117414372"><a name="p856117414372"></a><a name="p856117414372"></a>cookie名称</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.72%" headers="mcps1.2.4.1.2 "><p id="p356110417377"><a name="p356110417377"></a><a name="p356110417377"></a>当会话保持选择应用程序cookie时，需要填写cookie名称。</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.86%" headers="mcps1.2.4.1.3 "><p id="p195611446376"><a name="p195611446376"></a><a name="p195611446376"></a>cookieName-qsps</p>
    </td>
    </tr>
    <tr id="row16561745372"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p1856111415375"><a name="p1856111415375"></a><a name="p1856111415375"></a>会话保持时间（分钟）</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.72%" headers="mcps1.2.4.1.2 "><p id="p85611417378"><a name="p85611417378"></a><a name="p85611417378"></a>当分配策略类型选择“加权轮询算法”，会话保持开启后，会话保持择“HTTP&nbsp;cookie”，需添加会话保持时间。取值范围[1，1440]。</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.86%" headers="mcps1.2.4.1.3 "><p id="p205618423715"><a name="p205618423715"></a><a name="p205618423715"></a>20</p>
    </td>
    </tr>
    <tr id="row656113463715"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p1656119416373"><a name="p1656119416373"></a><a name="p1656119416373"></a>描述</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.72%" headers="mcps1.2.4.1.2 "><p id="p9561204183712"><a name="p9561204183712"></a><a name="p9561204183712"></a>后端<span id="text1353825610537"><a name="text1353825610537"></a><a name="text1353825610537"></a>服务器</span>组的描述</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.86%" headers="mcps1.2.4.1.3 "><p id="p155619417372"><a name="p155619417372"></a><a name="p155619417372"></a>-</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 3**  增强型负载均衡配置健康检查参数说明

    <a name="table95680412371"></a>
    <table><thead align="left"><tr id="row1256210411378"><th class="cellrowborder" valign="top" width="23.419999999999998%" id="mcps1.2.4.1.1"><p id="p156218414377"><a name="p156218414377"></a><a name="p156218414377"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="46.72%" id="mcps1.2.4.1.2"><p id="p45620443711"><a name="p45620443711"></a><a name="p45620443711"></a>说明</p>
    </th>
    <th class="cellrowborder" valign="top" width="29.86%" id="mcps1.2.4.1.3"><p id="p185622433710"><a name="p185622433710"></a><a name="p185622433710"></a>示例</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row456214163715"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p105621646371"><a name="p105621646371"></a><a name="p105621646371"></a>是否开启</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.72%" headers="mcps1.2.4.1.2 "><p id="p175623416377"><a name="p175623416377"></a><a name="p175623416377"></a>开启或者关闭健康检查。</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.86%" headers="mcps1.2.4.1.3 "><p id="p1756213415373"><a name="p1756213415373"></a><a name="p1756213415373"></a>-</p>
    </td>
    </tr>
    <tr id="row1556318453710"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p175624417375"><a name="p175624417375"></a><a name="p175624417375"></a>协议</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.72%" headers="mcps1.2.4.1.2 "><p id="p1475375182317"><a name="p1475375182317"></a><a name="p1475375182317"></a>健康检查支持TCP和HTTP方式，设置后不可修改。</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.86%" headers="mcps1.2.4.1.3 "><p id="p65626414372"><a name="p65626414372"></a><a name="p65626414372"></a>HTTP</p>
    </td>
    </tr>
    <tr id="row1456311413713"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p1563841377"><a name="p1563841377"></a><a name="p1563841377"></a>域名</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.72%" headers="mcps1.2.4.1.2 "><p id="p175631947374"><a name="p175631947374"></a><a name="p175631947374"></a>健康检查的请求域名。默认值为空，由数字、字母、‘-’、‘.’组成的字符串，只能以数字或字符开头。只有健康检查协议为HTTP时，需要设置。</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.86%" headers="mcps1.2.4.1.3 "><p id="p256311403714"><a name="p256311403714"></a><a name="p256311403714"></a>www.elb.com</p>
    </td>
    </tr>
    <tr id="row1756314153720"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p195631416374"><a name="p195631416374"></a><a name="p195631416374"></a>端口</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.72%" headers="mcps1.2.4.1.2 "><p id="p1956313417375"><a name="p1956313417375"></a><a name="p1956313417375"></a>健康检查端口号，取值范围[1，65535]，为可选参数。</p>
    <div class="note" id="note35631403712"><a name="note35631403712"></a><a name="note35631403712"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p1056315493716"><a name="p1056315493716"></a><a name="p1056315493716"></a>未配置健康检查端口时，默认使用后端云服务器端口进行健康检查。配置后，使用配置的健康检查端口进行健康检查。</p>
    </div></div>
    </td>
    <td class="cellrowborder" valign="top" width="29.86%" headers="mcps1.2.4.1.3 "><p id="p19563940375"><a name="p19563940375"></a><a name="p19563940375"></a>80</p>
    </td>
    </tr>
    <tr id="row1956312483717"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p456312433713"><a name="p456312433713"></a><a name="p456312433713"></a>高级配置</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.72%" headers="mcps1.2.4.1.2 "><p id="p356320423718"><a name="p356320423718"></a><a name="p356320423718"></a>分为默认设置和自定义设置。</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.86%" headers="mcps1.2.4.1.3 "><p id="p2056311473717"><a name="p2056311473717"></a><a name="p2056311473717"></a>默认设置</p>
    </td>
    </tr>
    <tr id="row456394163714"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p195635417372"><a name="p195635417372"></a><a name="p195635417372"></a>检查周期（秒）</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.72%" headers="mcps1.2.4.1.2 "><p id="p10563104203711"><a name="p10563104203711"></a><a name="p10563104203711"></a>每次健康检查响应的最大间隔时间。</p>
    <p id="p15639419374"><a name="p15639419374"></a><a name="p15639419374"></a>取值范围[1-50]。</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.86%" headers="mcps1.2.4.1.3 "><p id="p5563148375"><a name="p5563148375"></a><a name="p5563148375"></a>5</p>
    </td>
    </tr>
    <tr id="row205644443718"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p25631040376"><a name="p25631040376"></a><a name="p25631040376"></a>超时时间（秒）</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.72%" headers="mcps1.2.4.1.2 "><p id="p75641743371"><a name="p75641743371"></a><a name="p75641743371"></a>每次健康检查响应的最大超时时间。取值范围[1-50]。</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.86%" headers="mcps1.2.4.1.3 "><p id="p175641747374"><a name="p175641747374"></a><a name="p175641747374"></a>10</p>
    </td>
    </tr>
    <tr id="row155644493713"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p75647419370"><a name="p75647419370"></a><a name="p75647419370"></a>检查路径</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.72%" headers="mcps1.2.4.1.2 "><p id="p8564948375"><a name="p8564948375"></a><a name="p8564948375"></a>指定健康检查的URL地址的路径。当“协议”为HTTP时生效。长度范围[1-80]。</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.86%" headers="mcps1.2.4.1.3 "><p id="p45643417371"><a name="p45643417371"></a><a name="p45643417371"></a>/index.html</p>
    </td>
    </tr>
    <tr id="row16567144143718"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p356411463720"><a name="p356411463720"></a><a name="p356411463720"></a>最大重试次数</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.72%" headers="mcps1.2.4.1.2 "><p id="p3567184103716"><a name="p3567184103716"></a><a name="p3567184103716"></a>健康检查最大的重试次数，取值范围[1-10]。</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.86%" headers="mcps1.2.4.1.3 "><p id="p11567194133711"><a name="p11567194133711"></a><a name="p11567194133711"></a>3</p>
    </td>
    </tr>
    </tbody>
    </table>

8.  单击“确定”。

## 添加经典型负载均衡HTTPS监听器<a name="section7841311103416"></a>

1.  登录管理控制台。
2.  在管理控制台左上角单击![](figures/zh-cn_image_0167652153.jpg)图标，选择区域和项目。
3.  选择“服务列表 \> 网络 \> 弹性负载均衡”。
4.  在“负载均衡器”界面，切换“经典型”页签，单击需要添加监听器的负载均衡名称。
5.  在“监听器”区域，单击“添加监听器”，配置参数请参见[表4](#table3947759918410)。

    **表 4**  经典型负载均衡监听器参数说明

    <a name="table3947759918410"></a>
    <table><thead align="left"><tr id="row1918557218410"><th class="cellrowborder" valign="top" width="28.000000000000004%" id="mcps1.2.4.1.1"><p id="p25669989184122"><a name="p25669989184122"></a><a name="p25669989184122"></a><strong id="b9225239193651"><a name="b9225239193651"></a><a name="b9225239193651"></a>参数</strong></p>
    </th>
    <th class="cellrowborder" valign="top" width="53.89000000000001%" id="mcps1.2.4.1.2"><p id="p66003208184122"><a name="p66003208184122"></a><a name="p66003208184122"></a><strong id="b9046885193651"><a name="b9046885193651"></a><a name="b9046885193651"></a>说明</strong></p>
    </th>
    <th class="cellrowborder" valign="top" width="18.11%" id="mcps1.2.4.1.3"><p id="p44659603184122"><a name="p44659603184122"></a><a name="p44659603184122"></a><strong id="b61709088193651"><a name="b61709088193651"></a><a name="b61709088193651"></a>取值样例</strong></p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row3253628418410"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.4.1.1 "><p id="p9051947184122"><a name="p9051947184122"></a><a name="p9051947184122"></a>名称</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.89000000000001%" headers="mcps1.2.4.1.2 "><p id="p62119074184122"><a name="p62119074184122"></a><a name="p62119074184122"></a>监听器名称。</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.11%" headers="mcps1.2.4.1.3 "><p id="p59487507161644"><a name="p59487507161644"></a><a name="p59487507161644"></a>listener-ssgu</p>
    </td>
    </tr>
    <tr id="row66795703161723"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.4.1.1 "><p id="p55255176161725"><a name="p55255176161725"></a><a name="p55255176161725"></a>负载均衡器协议/端口</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.89000000000001%" headers="mcps1.2.4.1.2 "><p id="p566915862411"><a name="p566915862411"></a><a name="p566915862411"></a>负载分发的协议和端口。</p>
    <p id="p260014598538"><a name="p260014598538"></a><a name="p260014598538"></a>选择HTTPS协议，端口取值范围[1-65535]。</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.11%" headers="mcps1.2.4.1.3 "><p id="p34532864101423"><a name="p34532864101423"></a><a name="p34532864101423"></a>HTTPS/443</p>
    </td>
    </tr>
    <tr id="row49179263162422"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.4.1.1 "><p id="p39960184162422"><a name="p39960184162422"></a><a name="p39960184162422"></a>后端协议/端口</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.89000000000001%" headers="mcps1.2.4.1.2 "><p id="p15549454162422"><a name="p15549454162422"></a><a name="p15549454162422"></a>云服务开通的协议和端口。</p>
    <p id="p346510444541"><a name="p346510444541"></a><a name="p346510444541"></a>协议默认HTTP。端口取值范围[1，65535]。</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.11%" headers="mcps1.2.4.1.3 "><p id="p66231138124610"><a name="p66231138124610"></a><a name="p66231138124610"></a>HTTP/22</p>
    </td>
    </tr>
    <tr id="row62337098162422"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.4.1.1 "><p id="p24162975162422"><a name="p24162975162422"></a><a name="p24162975162422"></a>分配策略类型</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.89000000000001%" headers="mcps1.2.4.1.2 "><p id="p11043993162422"><a name="p11043993162422"></a><a name="p11043993162422"></a>负载均衡采用的算法。</p>
    <a name="ul5968188218551"></a><a name="ul5968188218551"></a><ul id="ul5968188218551"><li>轮询算法：按顺序把每个新的连接请求分配给下一个服务器，最终把所有请求平分给所有的服务器。</li><li>最少连接：通过当前活跃的连接数来估计服务器负载情况的一种动态调度算法，系统把新的连接请求分配给当前连接数目最少的服务器。</li><li>源IP算法：将请求的源IP地址进行Hash运算，得到一个具体的数值，同时对后端服务器进行编号，按照运算结果将请求分发到对应编号的服务器上。这可以使得对不同源IP的访问进行负载分发，同时使得同一个客户端IP的请求始终被派发至某特定的服务器。</li></ul>
    <div class="note" id="note449753855814"><a name="note449753855814"></a><a name="note449753855814"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p12497163811587"><a name="p12497163811587"></a><a name="p12497163811587"></a>用户可以根据自身需求选择相应的算法来分配用户访问流量，提升负载均衡能力。</p>
    </div></div>
    </td>
    <td class="cellrowborder" valign="top" width="18.11%" headers="mcps1.2.4.1.3 "><p id="p22148268162422"><a name="p22148268162422"></a><a name="p22148268162422"></a>轮询算法</p>
    </td>
    </tr>
    <tr id="row6077438093536"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.4.1.1 "><p id="p2377775393536"><a name="p2377775393536"></a><a name="p2377775393536"></a>默认证书</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.89000000000001%" headers="mcps1.2.4.1.2 "><p id="p4694985993536"><a name="p4694985993536"></a><a name="p4694985993536"></a>HTTPS协议的负载均衡使用的证书。</p>
    <p id="p4904405162422"><a name="p4904405162422"></a><a name="p4904405162422"></a>可选择已创建或新创建证书，新创建证书请参考<a href="https://support.huaweicloud.com/usermanual-elb/zh_cn_elb_03_0005.html" target="_blank" rel="noopener noreferrer">证书</a>章节。</p>
    <p id="p833794293717"><a name="p833794293717"></a><a name="p833794293717"></a>当负载均衡器协议为HTTPS时该选项才有效。</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.11%" headers="mcps1.2.4.1.3 "><p id="p4484222593536"><a name="p4484222593536"></a><a name="p4484222593536"></a>-</p>
    </td>
    </tr>
    <tr id="row46636939152656"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.4.1.1 "><p id="p65757227152739"><a name="p65757227152739"></a><a name="p65757227152739"></a>SSL协议</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.89000000000001%" headers="mcps1.2.4.1.2 "><p id="p24735162152739"><a name="p24735162152739"></a><a name="p24735162152739"></a>HTTPS协议的负载均衡使用的SSL协议。用于启动特定的加密协议。</p>
    <a name="ul57391130152739"></a><a name="ul57391130152739"></a><ul id="ul57391130152739"><li>TLSv1.2</li><li>TLSv1.2 TLSv1.1 TLSv1</li></ul>
    <p id="p29312012152739"><a name="p29312012152739"></a><a name="p29312012152739"></a>当负载均衡器协议为HTTPS时该选项才有效。</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.11%" headers="mcps1.2.4.1.3 "><p id="p27837997152739"><a name="p27837997152739"></a><a name="p27837997152739"></a>TLSv1.2</p>
    </td>
    </tr>
    <tr id="row52414897152722"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.4.1.1 "><p id="p27023193152739"><a name="p27023193152739"></a><a name="p27023193152739"></a>SSL密码</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.89000000000001%" headers="mcps1.2.4.1.2 "><p id="p41395063152739"><a name="p41395063152739"></a><a name="p41395063152739"></a>HTTPS协议的负载均衡使用的SSL密码。选择加密套件。</p>
    <a name="ul64665817152739"></a><a name="ul64665817152739"></a><ul id="ul64665817152739"><li>默认密码</li><li>扩展密码</li><li>严格密码</li></ul>
    <p id="p10192267152739"><a name="p10192267152739"></a><a name="p10192267152739"></a>当负载均衡器协议为HTTPS时该选项才有效。当SSL协议选择 "TLSv1.2 TLSv1.1 TLSv1”选项时，SSL密码仅支持扩展密码。</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.11%" headers="mcps1.2.4.1.3 "><p id="p48188037152739"><a name="p48188037152739"></a><a name="p48188037152739"></a>默认密码</p>
    </td>
    </tr>
    <tr id="row38569529152051"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.4.1.1 "><p id="p37941618152117"><a name="p37941618152117"></a><a name="p37941618152117"></a>会话保持</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.89000000000001%" headers="mcps1.2.4.1.2 "><p id="p53372194152117"><a name="p53372194152117"></a><a name="p53372194152117"></a>会话保持是否开启。</p>
    <p id="p10587703152117"><a name="p10587703152117"></a><a name="p10587703152117"></a>开启会话保持后，弹性负载均衡将属于同一个会话的请求都转发到同一个云服务器进行处理。</p>
    <div class="note" id="note586599751148"><a name="note586599751148"></a><a name="note586599751148"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p581777271148"><a name="p581777271148"></a><a name="p581777271148"></a>仅当负载方式是轮询算法的时候，才会支持会话保持功能。</p>
    </div></div>
    </td>
    <td class="cellrowborder" valign="top" width="18.11%" headers="mcps1.2.4.1.3 "><p id="p52297615152117"><a name="p52297615152117"></a><a name="p52297615152117"></a>-</p>
    </td>
    </tr>
    <tr id="row38165688152018"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.4.1.1 "><p id="p7946880152018"><a name="p7946880152018"></a><a name="p7946880152018"></a>会话保持时间（分钟）</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.89000000000001%" headers="mcps1.2.4.1.2 "><p id="p15559793153157"><a name="p15559793153157"></a><a name="p15559793153157"></a>当会话保持开启时，需添加会话保持时间。取值范围[1，1440]。</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.11%" headers="mcps1.2.4.1.3 "><p id="p63006969152018"><a name="p63006969152018"></a><a name="p63006969152018"></a>5</p>
    </td>
    </tr>
    <tr id="row1131412618410"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.4.1.1 "><p id="p1316186194114"><a name="p1316186194114"></a><a name="p1316186194114"></a>描述</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.89000000000001%" headers="mcps1.2.4.1.2 "><p id="p43164694115"><a name="p43164694115"></a><a name="p43164694115"></a>监听器的描述。</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.11%" headers="mcps1.2.4.1.3 "><p id="p1931696104111"><a name="p1931696104111"></a><a name="p1931696104111"></a>-</p>
    </td>
    </tr>
    <tr id="row37894296162422"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.4.1.1 "><p id="p5504344162422"><a name="p5504344162422"></a><a name="p5504344162422"></a>健康检查协议/端口</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.89000000000001%" headers="mcps1.2.4.1.2 "><p id="p71231155333"><a name="p71231155333"></a><a name="p71231155333"></a>对后端云服务器进行健康检查的协议和端口。</p>
    <p id="p9912137153318"><a name="p9912137153318"></a><a name="p9912137153318"></a>健康检查支持TCP和HTTP协议，设置后不可修改。</p>
    <p id="p43198726162422"><a name="p43198726162422"></a><a name="p43198726162422"></a>端口取值范围[1，65535]。</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.11%" headers="mcps1.2.4.1.3 "><p id="p9435957162422"><a name="p9435957162422"></a><a name="p9435957162422"></a>HTTP/80</p>
    </td>
    </tr>
    <tr id="row2064894118410"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.4.1.1 "><p id="p32956516184122"><a name="p32956516184122"></a><a name="p32956516184122"></a>间隔时间（秒）</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.89000000000001%" headers="mcps1.2.4.1.2 "><p id="p25870774163512"><a name="p25870774163512"></a><a name="p25870774163512"></a>每次健康检查响应的最大间隔时间。</p>
    <p id="p17123758558"><a name="p17123758558"></a><a name="p17123758558"></a>取值范围：[1，50]。</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.11%" headers="mcps1.2.4.1.3 "><p id="p32682136163516"><a name="p32682136163516"></a><a name="p32682136163516"></a>5</p>
    </td>
    </tr>
    <tr id="row577303118410"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.4.1.1 "><p id="p43486880184122"><a name="p43486880184122"></a><a name="p43486880184122"></a>超时时间（秒）</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.89000000000001%" headers="mcps1.2.4.1.2 "><p id="p6084546163512"><a name="p6084546163512"></a><a name="p6084546163512"></a>每次健康检查响应的最大超时时间。</p>
    <p id="p333347163818"><a name="p333347163818"></a><a name="p333347163818"></a>取值范围：[1，50]。</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.11%" headers="mcps1.2.4.1.3 "><p id="p20753786163516"><a name="p20753786163516"></a><a name="p20753786163516"></a>10</p>
    </td>
    </tr>
    <tr id="row1853746318410"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.4.1.1 "><p id="p61652718184122"><a name="p61652718184122"></a><a name="p61652718184122"></a>健康阈值</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.89000000000001%" headers="mcps1.2.4.1.2 "><p id="p58496162163512"><a name="p58496162163512"></a><a name="p58496162163512"></a>判定健康检查结果正常的阈值。即健康检查连续成功多少次后，将后端云服务器的健康检查结果由不正常改为正常。取值范围：[1，10]。</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.11%" headers="mcps1.2.4.1.3 "><p id="p7746215163516"><a name="p7746215163516"></a><a name="p7746215163516"></a>3</p>
    </td>
    </tr>
    <tr id="row51204614184116"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.4.1.1 "><p id="p53302206184122"><a name="p53302206184122"></a><a name="p53302206184122"></a>不健康阈值</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.89000000000001%" headers="mcps1.2.4.1.2 "><p id="p37642080163512"><a name="p37642080163512"></a><a name="p37642080163512"></a>判定健康检查结果为不正常的阈值。即健康检查连续失败多少次后，将后端云服务器的健康检查状态由正常改为不正常。取值范围：[1，10]。</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.11%" headers="mcps1.2.4.1.3 "><p id="p32899075163516"><a name="p32899075163516"></a><a name="p32899075163516"></a>3</p>
    </td>
    </tr>
    <tr id="row30656460163438"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.4.1.1 "><p id="p7472684163438"><a name="p7472684163438"></a><a name="p7472684163438"></a>检查路径</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.89000000000001%" headers="mcps1.2.4.1.2 "><p id="p1307686163438"><a name="p1307686163438"></a><a name="p1307686163438"></a>指定健康检查的URL地址的路径。当“健康检查协议”为HTTP时生效。长度范围：[1，80]。</p>
    <div class="note" id="note610554891062"><a name="note610554891062"></a><a name="note610554891062"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p126284931062"><a name="p126284931062"></a><a name="p126284931062"></a>路径中只能使用字母、数字、‘-’、‘/’、‘.’、‘%’、‘?’、‘#’、‘&amp;’、“_”、“=”这些字符。</p>
    </div></div>
    </td>
    <td class="cellrowborder" valign="top" width="18.11%" headers="mcps1.2.4.1.3 "><p id="p38813732163438"><a name="p38813732163438"></a><a name="p38813732163438"></a>/test.html</p>
    </td>
    </tr>
    </tbody>
    </table>

6.  配置完成后，单击“确定”。

## TCP监听器将HTTPS流量透传到后端服务器<a name="section19187181715231"></a>

如果您不希望负载均衡器对HTTPS流量进行解密，可以通过配置相同端口的TCP监听器将HTTPS流量透传到后端服务器。并且在实例的安全组配置相同端口的TCP入方向规则，以允许相同端口上来自负载均衡器的入站流量。

如下图所示，TCP监听器如何将端口为443的HTTPS流量进行无解密透传到后端服务器。

**图 1**  TCP透传HTTPS流量<a name="fig38284074215"></a>  
![](figures/TCP透传HTTPS流量.png "TCP透传HTTPS流量")

