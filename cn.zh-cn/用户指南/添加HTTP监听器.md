# 添加HTTP监听器<a name="elb_ug_jt_0008"></a>

## 操作场景<a name="section13358194520513"></a>

HTTP协议适用于需要对数据内容进行识别的应用，如Web应用、小的手机游戏等。您可以添加一个HTTP监听器转发来自HTTP协议的请求。

>![](public_sys-resources/icon-caution.gif) **注意：** 
>-   前端协议为“HTTP”时，后端协议默认为“HTTP”，且不支持修改。
>-   如果您的独享型负载均衡实例类型为网络型（TCP/UDP），则无法创建HTTP监听器。

## 添加独享型负载均衡HTTP监听器<a name="section1399219525233"></a>

1.  登录管理控制台。
2.  在管理控制台左上角单击![](figures/icon-region.png)图标，选择区域和项目。
3.  单击页面左上角的![](figures/icon-position.png)，选择“网络 \> 弹性负载均衡”。
4.  在“负载均衡器”界面，单击需要添加监听器的负载均衡名称。
5.  切换到“监听器”页签，单击“添加监听器”，配置监听器。配置监听器参数参见[表1](#table16995152202318)。

    **表 1**  独享型负载均衡配置监听器参数说明

    <a name="table16995152202318"></a>
    <table><thead align="left"><tr id="row4995125218232"><th class="cellrowborder" valign="top" width="26.1%" id="mcps1.2.4.1.1"><p id="p799515210231"><a name="p799515210231"></a><a name="p799515210231"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="44.73%" id="mcps1.2.4.1.2"><p id="p1995155220238"><a name="p1995155220238"></a><a name="p1995155220238"></a>说明</p>
    </th>
    <th class="cellrowborder" valign="top" width="29.17%" id="mcps1.2.4.1.3"><p id="p20995125210237"><a name="p20995125210237"></a><a name="p20995125210237"></a>示例</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row189951352112318"><td class="cellrowborder" valign="top" width="26.1%" headers="mcps1.2.4.1.1 "><p id="p599585213230"><a name="p599585213230"></a><a name="p599585213230"></a>名称</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.73%" headers="mcps1.2.4.1.2 "><p id="p2099695292317"><a name="p2099695292317"></a><a name="p2099695292317"></a>监听器名称。</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.17%" headers="mcps1.2.4.1.3 "><p id="p399655212233"><a name="p399655212233"></a><a name="p399655212233"></a>listener-pnqy</p>
    </td>
    </tr>
    <tr id="row10996152192317"><td class="cellrowborder" valign="top" width="26.1%" headers="mcps1.2.4.1.1 "><p id="p3996185212235"><a name="p3996185212235"></a><a name="p3996185212235"></a>前端协议</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.73%" headers="mcps1.2.4.1.2 "><p id="p19961152142318"><a name="p19961152142318"></a><a name="p19961152142318"></a>客户端与负载均衡监听器建立流量分发连接的协议。</p>
    <p id="p7996195211233"><a name="p7996195211233"></a><a name="p7996195211233"></a>协议选择HTTP。</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.17%" headers="mcps1.2.4.1.3 "><p id="p199964521233"><a name="p199964521233"></a><a name="p199964521233"></a>HTTP</p>
    </td>
    </tr>
    <tr id="row146136503518"><td class="cellrowborder" valign="top" width="26.1%" headers="mcps1.2.4.1.1 "><p id="p1661314501454"><a name="p1661314501454"></a><a name="p1661314501454"></a>前端端口</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.73%" headers="mcps1.2.4.1.2 "><p id="p7381837184513"><a name="p7381837184513"></a><a name="p7381837184513"></a>客户端与负载均衡监听器建立流量分发连接的端口。</p>
    <p id="p1381143713457"><a name="p1381143713457"></a><a name="p1381143713457"></a>取值范围为：[1-65535]。</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.17%" headers="mcps1.2.4.1.3 "><p id="p56137501058"><a name="p56137501058"></a><a name="p56137501058"></a>80</p>
    </td>
    </tr>
    <tr id="row1973112511157"><td class="cellrowborder" valign="top" width="26.1%" headers="mcps1.2.4.1.1 "><p id="p3974425151515"><a name="p3974425151515"></a><a name="p3974425151515"></a>重定向</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.73%" headers="mcps1.2.4.1.2 "><p id="p1293052172513"><a name="p1293052172513"></a><a name="p1293052172513"></a>重定向开关是否开启。</p>
    <p id="p11373547183518"><a name="p11373547183518"></a><a name="p11373547183518"></a>协议类型为HTTP时，可根据需要设置该项。需要保证业务建立安全连接时，若同时创建了HTTPS监听器和HTTP监听器，可以通过重定向功能，将HTTP监听器访问重定向至HTTPS监听器。</p>
    <p id="p208661237165311"><a name="p208661237165311"></a><a name="p208661237165311"></a><span id="ph165481846115311"><a name="ph165481846115311"></a><a name="ph165481846115311"></a>HTTP监听器被重定向后，会返回301返回码。</span></p>
    </td>
    <td class="cellrowborder" valign="top" width="29.17%" headers="mcps1.2.4.1.3 "><p id="p149741625201519"><a name="p149741625201519"></a><a name="p149741625201519"></a>-</p>
    </td>
    </tr>
    <tr id="row15603114051613"><td class="cellrowborder" valign="top" width="26.1%" headers="mcps1.2.4.1.1 "><p id="p3603114010163"><a name="p3603114010163"></a><a name="p3603114010163"></a>重定向至</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.73%" headers="mcps1.2.4.1.2 "><p id="p756712251178"><a name="p756712251178"></a><a name="p756712251178"></a>选择需要重定向HTTPS监听器的名称。</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.17%" headers="mcps1.2.4.1.3 "><p id="p530234871818"><a name="p530234871818"></a><a name="p530234871818"></a>-listener-9ecd（HTTPS/443）</p>
    </td>
    </tr>
    <tr id="row1099695282315"><td class="cellrowborder" colspan="3" valign="top" headers="mcps1.2.4.1.1 mcps1.2.4.1.2 mcps1.2.4.1.3 "><p id="p399610526238"><a name="p399610526238"></a><a name="p399610526238"></a><strong id="b09961252122313"><a name="b09961252122313"></a><a name="b09961252122313"></a>高级配置</strong></p>
    </td>
    </tr>
    <tr id="row3996052142310"><td class="cellrowborder" valign="top" width="26.1%" headers="mcps1.2.4.1.1 "><p id="p15996195216233"><a name="p15996195216233"></a><a name="p15996195216233"></a>访问策略</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.73%" headers="mcps1.2.4.1.2 "><p id="p5997195216231"><a name="p5997195216231"></a><a name="p5997195216231"></a>支持通过白名单和黑名单进行访问控制，更多信息请参见<a href="访问控制策略.md">访问控制策略</a>：</p>
    <a name="ul1599719527235"></a><a name="ul1599719527235"></a><ul id="ul1599719527235"><li>允许所有IP访问</li><li>黑名单</li><li>白名单</li></ul>
    </td>
    <td class="cellrowborder" valign="top" width="29.17%" headers="mcps1.2.4.1.3 "><p id="p1099711528233"><a name="p1099711528233"></a><a name="p1099711528233"></a>黑名单</p>
    </td>
    </tr>
    <tr id="row09972052202318"><td class="cellrowborder" valign="top" width="26.1%" headers="mcps1.2.4.1.1 "><p id="p6997185262318"><a name="p6997185262318"></a><a name="p6997185262318"></a>IP地址组</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.73%" headers="mcps1.2.4.1.2 "><p id="p149979523230"><a name="p149979523230"></a><a name="p149979523230"></a>设置白名单或者黑名单时，必须选择一个IP地址组。如果还未创建IP地址组，需要先创建IP地址组，更多关于IP地址组的信息请参见<a href="IP地址组（黑名单-白名单）.md">IP地址组</a>。</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.17%" headers="mcps1.2.4.1.3 "><p id="p29972052102312"><a name="p29972052102312"></a><a name="p29972052102312"></a>ipGroup-b2</p>
    </td>
    </tr>
    <tr id="row6518155312191"><td class="cellrowborder" valign="top" width="26.1%" headers="mcps1.2.4.1.1 "><p id="p3518125315191"><a name="p3518125315191"></a><a name="p3518125315191"></a>获取弹性公网IP</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.73%" headers="mcps1.2.4.1.2 "><p id="p651825391919"><a name="p651825391919"></a><a name="p651825391919"></a>通过X-Forwarded-ELB-IP头字段获取ELB实例公网IP地址。</p>
    <p id="p16550639182514"><a name="p16550639182514"></a><a name="p16550639182514"></a>若您需要将ELB公网IP透传到后端，只需在创建HTTP监听器时，打开该开关。</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.17%" headers="mcps1.2.4.1.3 "><p id="p351825311192"><a name="p351825311192"></a><a name="p351825311192"></a>-</p>
    </td>
    </tr>
    <tr id="row83181647102112"><td class="cellrowborder" valign="top" width="26.1%" headers="mcps1.2.4.1.1 "><p id="p1831844718215"><a name="p1831844718215"></a><a name="p1831844718215"></a>获取监听器端口号</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.73%" headers="mcps1.2.4.1.2 "><p id="p10318247102118"><a name="p10318247102118"></a><a name="p10318247102118"></a>通过X-Forwarded-Port头字段获取ELB实例监听器端口号。</p>
    <p id="p1927265016266"><a name="p1927265016266"></a><a name="p1927265016266"></a>若您需要将ELB实例监听器的端口号透传到后端，只需在创建HTTP监听器时，打开该开关。</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.17%" headers="mcps1.2.4.1.3 "><p id="p1931815474210"><a name="p1931815474210"></a><a name="p1931815474210"></a>-</p>
    </td>
    </tr>
    <tr id="row1991125052116"><td class="cellrowborder" valign="top" width="26.1%" headers="mcps1.2.4.1.1 "><p id="p4911150172117"><a name="p4911150172117"></a><a name="p4911150172117"></a>获取客户端请求端口号</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.73%" headers="mcps1.2.4.1.2 "><p id="p1191135018211"><a name="p1191135018211"></a><a name="p1191135018211"></a>通过X-Forwarded-For-Port头字段获取客户端请求端口号。</p>
    <p id="p20534162112817"><a name="p20534162112817"></a><a name="p20534162112817"></a>若您需要将客户端请求的端口号透传到后端，只需在创建HTTP监听器时，打开该开关。</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.17%" headers="mcps1.2.4.1.3 "><p id="p11919504211"><a name="p11919504211"></a><a name="p11919504211"></a>-</p>
    </td>
    </tr>
    <tr id="row1039145842110"><td class="cellrowborder" valign="top" width="26.1%" headers="mcps1.2.4.1.1 "><p id="p11401658142110"><a name="p11401658142110"></a><a name="p11401658142110"></a>重写X-Forwarded-Host</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.73%" headers="mcps1.2.4.1.2 "><a name="ul577365472915"></a><a name="ul577365472915"></a><ul id="ul577365472915"><li>开关关闭：ELB透传客户端的X-Forwarded-Host。</li><li>开关开启：ELB以客户端请求头的Host重写X-Forwarded-Host向后端传输。</li></ul>
    </td>
    <td class="cellrowborder" valign="top" width="29.17%" headers="mcps1.2.4.1.3 "><p id="p184065811218"><a name="p184065811218"></a><a name="p184065811218"></a>-</p>
    </td>
    </tr>
    <tr id="row129973524234"><td class="cellrowborder" valign="top" width="26.1%" headers="mcps1.2.4.1.1 "><p id="p399785212237"><a name="p399785212237"></a><a name="p399785212237"></a>空闲超时时间（秒）</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.73%" headers="mcps1.2.4.1.2 "><p id="p1361255731812"><a name="p1361255731812"></a><a name="p1361255731812"></a>如果在超时时间内一直没有访问请求，负载均衡会中断当前连接，直到下一次请求到来时再重新建立新的连接。</p>
    <p id="p177911772117"><a name="p177911772117"></a><a name="p177911772117"></a>时间取值范围[0-4000]。</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.17%" headers="mcps1.2.4.1.3 "><p id="p3330454179"><a name="p3330454179"></a><a name="p3330454179"></a>60</p>
    </td>
    </tr>
    <tr id="row182286208237"><td class="cellrowborder" valign="top" width="26.1%" headers="mcps1.2.4.1.1 "><p id="p13751831122317"><a name="p13751831122317"></a><a name="p13751831122317"></a>请求超时时间（秒）</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.73%" headers="mcps1.2.4.1.2 "><p id="p11642204131711"><a name="p11642204131711"></a><a name="p11642204131711"></a>客户端向负载均衡发起请求，如果在超时时间内客户端没有完成整个请求的传输，负载均衡将放弃等待关闭连接。</p>
    <p id="p83451412813"><a name="p83451412813"></a><a name="p83451412813"></a>时间取值范围[1-300]。</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.17%" headers="mcps1.2.4.1.3 "><p id="p13642941131712"><a name="p13642941131712"></a><a name="p13642941131712"></a>60</p>
    </td>
    </tr>
    <tr id="row1545492422310"><td class="cellrowborder" valign="top" width="26.1%" headers="mcps1.2.4.1.1 "><p id="p7454172452317"><a name="p7454172452317"></a><a name="p7454172452317"></a>响应超时时间（秒）</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.73%" headers="mcps1.2.4.1.2 "><p id="p183841133131815"><a name="p183841133131815"></a><a name="p183841133131815"></a>负载均衡向后端服务器发起请求，如果超时时间内接收请求的后端服务器无响应，负载均衡会向其他后端服务器重试请求。如果重试期间后端服务器一直没有响应，则负载均衡会给客户端返回HTTP 504错误码。</p>
    <p id="p108706541619"><a name="p108706541619"></a><a name="p108706541619"></a>时间取值范围[1-300]。</p>
    <div class="note" id="note20281059202213"><a name="note20281059202213"></a><a name="note20281059202213"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p14281959152213"><a name="p14281959152213"></a><a name="p14281959152213"></a>当开启了会话保持功能时，响应超时时间内如果对应的后端服务器无响应，则直接会返回HTTP 504错误码。</p>
    </div></div>
    </td>
    <td class="cellrowborder" valign="top" width="29.17%" headers="mcps1.2.4.1.3 "><p id="p153584386179"><a name="p153584386179"></a><a name="p153584386179"></a>60</p>
    </td>
    </tr>
    <tr id="row29970521235"><td class="cellrowborder" valign="top" width="26.1%" headers="mcps1.2.4.1.1 "><p id="p18997152172312"><a name="p18997152172312"></a><a name="p18997152172312"></a>描述</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.73%" headers="mcps1.2.4.1.2 "><p id="p169976524239"><a name="p169976524239"></a><a name="p169976524239"></a>对于监听器描述。</p>
    <p id="p4997195212310"><a name="p4997195212310"></a><a name="p4997195212310"></a>字数范围：0/255。</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.17%" headers="mcps1.2.4.1.3 "><p id="p19997145219236"><a name="p19997145219236"></a><a name="p19997145219236"></a>-</p>
    </td>
    </tr>
    </tbody>
    </table>

6.  单击“下一步：配置后端分配策略”。配置后端服务器组参数请参见[表2](#table299811529239)。

    **表 2**  独享型负载均衡配置后端服务器组参数说明

    <a name="table299811529239"></a>
    <table><thead align="left"><tr id="row99989528236"><th class="cellrowborder" valign="top" width="23.419999999999998%" id="mcps1.2.4.1.1"><p id="p1799985232319"><a name="p1799985232319"></a><a name="p1799985232319"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="50.43%" id="mcps1.2.4.1.2"><p id="p49994524234"><a name="p49994524234"></a><a name="p49994524234"></a>说明</p>
    </th>
    <th class="cellrowborder" valign="top" width="26.150000000000002%" id="mcps1.2.4.1.3"><p id="p17999145292310"><a name="p17999145292310"></a><a name="p17999145292310"></a>示例</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row1999995222315"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p179991252112312"><a name="p179991252112312"></a><a name="p179991252112312"></a>后端<span id="text3999185252319"><a name="text3999185252319"></a><a name="text3999185252319"></a>服务器</span>组</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.43%" headers="mcps1.2.4.1.2 "><p id="p1199975222317"><a name="p1199975222317"></a><a name="p1199975222317"></a>把具有相同特性的后端<span id="text69991252182319"><a name="text69991252182319"></a><a name="text69991252182319"></a>服务器</span>放在一个组。</p>
    <a name="ul39994528231"></a><a name="ul39994528231"></a><ul id="ul39994528231"><li>新创建</li><li>使用已有<div class="note" id="note179991352122313"><a name="note179991352122313"></a><a name="note179991352122313"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="zh-cn_topic_0242751126_p1494711463437"><a name="zh-cn_topic_0242751126_p1494711463437"></a><a name="zh-cn_topic_0242751126_p1494711463437"></a><span id="zh-cn_topic_0242751126_ph157831728154313"><a name="zh-cn_topic_0242751126_ph157831728154313"></a><a name="zh-cn_topic_0242751126_ph157831728154313"></a>使用已有后端<span id="zh-cn_topic_0242751126_ph177241201433"><a name="zh-cn_topic_0242751126_ph177241201433"></a><a name="zh-cn_topic_0242751126_ph177241201433"></a>服务器</span>组时，请确保此后端<span id="zh-cn_topic_0242751126_ph10299216174319"><a name="zh-cn_topic_0242751126_ph10299216174319"></a><a name="zh-cn_topic_0242751126_ph10299216174319"></a>服务器</span>组未被使用。并且只能选择前端协议匹配的后端<span id="zh-cn_topic_0242751126_ph16724182224314"><a name="zh-cn_topic_0242751126_ph16724182224314"></a><a name="zh-cn_topic_0242751126_ph16724182224314"></a>服务器</span>组。例如前端协议是TCP时，后端协议只能是TCP。</span></p>
    </div></div>
    </li></ul>
    </td>
    <td class="cellrowborder" valign="top" width="26.150000000000002%" headers="mcps1.2.4.1.3 "><p id="p13019531238"><a name="p13019531238"></a><a name="p13019531238"></a>新创建</p>
    </td>
    </tr>
    <tr id="row20853182317"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p160105318236"><a name="p160105318236"></a><a name="p160105318236"></a>名称</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.43%" headers="mcps1.2.4.1.2 "><p id="p12011538239"><a name="p12011538239"></a><a name="p12011538239"></a>后端<span id="text17065310230"><a name="text17065310230"></a><a name="text17065310230"></a>服务器</span>组名称。</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.150000000000002%" headers="mcps1.2.4.1.3 "><p id="p309533232"><a name="p309533232"></a><a name="p309533232"></a>server_group-sq4v</p>
    </td>
    </tr>
    <tr id="row170953142319"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p1701353152312"><a name="p1701353152312"></a><a name="p1701353152312"></a>后端协议</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.43%" headers="mcps1.2.4.1.2 "><p id="p170153182312"><a name="p170153182312"></a><a name="p170153182312"></a>云服务器开通的协议。</p>
    <p id="p603535234"><a name="p603535234"></a><a name="p603535234"></a>前端协议为HTTP时，后端协议默认为HTTP，不支持修改。</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.150000000000002%" headers="mcps1.2.4.1.3 "><p id="p10145322312"><a name="p10145322312"></a><a name="p10145322312"></a>HTTP</p>
    </td>
    </tr>
    <tr id="row17055311233"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p1664310315543"><a name="p1664310315543"></a><a name="p1664310315543"></a>分配策略类型</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.43%" headers="mcps1.2.4.1.2 "><p id="p2001153142314"><a name="p2001153142314"></a><a name="p2001153142314"></a>负载均衡采用的算法。</p>
    <a name="ul8075372314"></a><a name="ul8075372314"></a><ul id="ul8075372314"><li>加权轮询算法：根据后端服务器的权重，按顺序依次将请求分发给不同的服务器。它用相应的权重表示服务器的处理性能，按照权重的高低以及轮询方式将请求分配给各服务器，相同权重的服务器处理相同数目的连接数。</li><li>加权最少连接：最少连接是通过当前活跃的连接数来估计服务器负载情况的一种动态调度算法。加权最少连接就是在最少连接数的基础上，根据服务器的不同处理能力，给每个服务器分配不同的权重，使其能够接受相应权值数的服务请求。</li><li>源IP算法：将请求的源IP地址进行一致性Hash运算，得到一个具体的数值，同时对后端服务器进行编号，按照运算结果将请求分发到对应编号的服务器上。这可以使得对不同源IP的访问进行负载分发，同时使得同一个客户端IP的请求始终被派发至某特定的服务器。</li></ul>
    <div class="note" id="note615537234"><a name="note615537234"></a><a name="note615537234"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="ul61125382312"></a><a name="ul61125382312"></a><ul id="ul61125382312"><li>用户可以根据自身需求选择相应的算法来分配用户访问流量，提升负载均衡能力。</li><li>对于加权轮询算法和加权最少连接，当服务器的权重为“0”时，将不会被分发访问请求。</li></ul>
    </div></div>
    </td>
    <td class="cellrowborder" valign="top" width="26.150000000000002%" headers="mcps1.2.4.1.3 "><p id="p811253132310"><a name="p811253132310"></a><a name="p811253132310"></a>加权轮询算法</p>
    </td>
    </tr>
    <tr id="row121653202313"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p111155320235"><a name="p111155320235"></a><a name="p111155320235"></a>会话保持</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.43%" headers="mcps1.2.4.1.2 "><p id="p1714537236"><a name="p1714537236"></a><a name="p1714537236"></a>开启会话保持后，弹性负载均衡将属于同一个会话的请求都转发到同一个<span id="text51175312310"><a name="text51175312310"></a><a name="text51175312310"></a>服务器</span>进行处理。</p>
    <div class="note" id="note181135342313"><a name="note181135342313"></a><a name="note181135342313"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p9185352315"><a name="p9185352315"></a><a name="p9185352315"></a>当分配策略类型为“加权轮询算法”或"加权最少连接”时，可配置会话保持。</p>
    </div></div>
    </td>
    <td class="cellrowborder" valign="top" width="26.150000000000002%" headers="mcps1.2.4.1.3 "><p id="p5105318231"><a name="p5105318231"></a><a name="p5105318231"></a>-</p>
    </td>
    </tr>
    <tr id="row3114532233"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p21153162312"><a name="p21153162312"></a><a name="p21153162312"></a>会话保持类型</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.43%" headers="mcps1.2.4.1.2 "><p id="p4977112513469"><a name="p4977112513469"></a><a name="p4977112513469"></a>前端协议为HTTP或HTTPS时，支持负载均衡器cookie类型的会话保持。</p>
    <a name="ul11561194235113"></a><a name="ul11561194235113"></a><ul id="ul11561194235113"><li><strong id="elb_ug_jt_0004_b253964721712"><a name="elb_ug_jt_0004_b253964721712"></a><a name="elb_ug_jt_0004_b253964721712"></a>负载均衡器cookie：</strong>负载均衡器会根据客户端第一个请求生成一个cookie，后续所有包含这个cookie值的请求都会由同一个后端<span id="elb_ug_jt_0004_ph197863419101"><a name="elb_ug_jt_0004_ph197863419101"></a><a name="elb_ug_jt_0004_ph197863419101"></a>服务器</span>处理。</li></ul>
    </td>
    <td class="cellrowborder" valign="top" width="26.150000000000002%" headers="mcps1.2.4.1.3 "><p id="p225534230"><a name="p225534230"></a><a name="p225534230"></a>负载均衡器cookie</p>
    </td>
    </tr>
    <tr id="row1121853132319"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p828535239"><a name="p828535239"></a><a name="p828535239"></a>会话保持时间（分钟）</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.43%" headers="mcps1.2.4.1.2 "><p id="p122175352319"><a name="p122175352319"></a><a name="p122175352319"></a>当分配策略类型选择“加权轮询算法”或“加权最少连接”，会话保持开启后，需添加会话保持时间。</p>
    <a name="ul1821153202318"></a><a name="ul1821153202318"></a><ul id="ul1821153202318"><li>四层会话保持的会话保持时间取值范围为[1，60]。</li><li>七层会话保持的会话保持时间取值范围为[1，1440]。</li></ul>
    </td>
    <td class="cellrowborder" valign="top" width="26.150000000000002%" headers="mcps1.2.4.1.3 "><p id="p1213539232"><a name="p1213539232"></a><a name="p1213539232"></a>20</p>
    </td>
    </tr>
    <tr id="row112115352317"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p102153102318"><a name="p102153102318"></a><a name="p102153102318"></a>描述</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.43%" headers="mcps1.2.4.1.2 "><p id="p2225372319"><a name="p2225372319"></a><a name="p2225372319"></a>后端<span id="text1922538231"><a name="text1922538231"></a><a name="text1922538231"></a>服务器</span>组的描述。</p>
    <p id="p20225332314"><a name="p20225332314"></a><a name="p20225332314"></a>字数范围：0/255。</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.150000000000002%" headers="mcps1.2.4.1.3 "><p id="p3295392318"><a name="p3295392318"></a><a name="p3295392318"></a>-</p>
    </td>
    </tr>
    </tbody>
    </table>

7.  单击“下一步：添加后端服务器”。添加后端服务器并配置健康检查。添加后端服务器详见[添加或移除后端服务器（独享型）](添加或移除后端服务器（独享型）.md)，配置健康检查参数请参见[表3](#table1022053182319)。

    **表 3**  独享型负载均衡配置健康检查参数说明

    <a name="table1022053182319"></a>
    <table><thead align="left"><tr id="row183253192312"><th class="cellrowborder" valign="top" width="23.419999999999998%" id="mcps1.2.4.1.1"><p id="p3335332313"><a name="p3335332313"></a><a name="p3335332313"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="52.470000000000006%" id="mcps1.2.4.1.2"><p id="p1039539238"><a name="p1039539238"></a><a name="p1039539238"></a>说明</p>
    </th>
    <th class="cellrowborder" valign="top" width="24.11%" id="mcps1.2.4.1.3"><p id="p12310533238"><a name="p12310533238"></a><a name="p12310533238"></a>示例</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row193105314234"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p193145315234"><a name="p193145315234"></a><a name="p193145315234"></a>是否开启</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.470000000000006%" headers="mcps1.2.4.1.2 "><p id="p123165316239"><a name="p123165316239"></a><a name="p123165316239"></a>开启或者关闭健康检查。</p>
    </td>
    <td class="cellrowborder" valign="top" width="24.11%" headers="mcps1.2.4.1.3 "><p id="p1961553162318"><a name="p1961553162318"></a><a name="p1961553162318"></a>-</p>
    </td>
    </tr>
    <tr id="row16645332313"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p20719538230"><a name="p20719538230"></a><a name="p20719538230"></a>协议</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.470000000000006%" headers="mcps1.2.4.1.2 "><p id="p187165332317"><a name="p187165332317"></a><a name="p187165332317"></a>健康检查支持HTTP、TCP、HTTPS协议，设置后不可修改。</p>
    </td>
    <td class="cellrowborder" valign="top" width="24.11%" headers="mcps1.2.4.1.3 "><p id="p47953122315"><a name="p47953122315"></a><a name="p47953122315"></a>HTTP</p>
    </td>
    </tr>
    <tr id="row127091533562"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p137185319231"><a name="p137185319231"></a><a name="p137185319231"></a>端口</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.470000000000006%" headers="mcps1.2.4.1.2 "><p id="p1171535239"><a name="p1171535239"></a><a name="p1171535239"></a>健康检查端口号，取值范围[1，65535]，为可选参数。</p>
    <div class="note" id="note157145322314"><a name="note157145322314"></a><a name="note157145322314"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p16715536231"><a name="p16715536231"></a><a name="p16715536231"></a>未配置健康检查端口时，默认使用后端云服务器端口进行健康检查。配置后，使用配置的健康检查端口进行健康检查。</p>
    </div></div>
    </td>
    <td class="cellrowborder" valign="top" width="24.11%" headers="mcps1.2.4.1.3 "><p id="p148115318234"><a name="p148115318234"></a><a name="p148115318234"></a>80</p>
    </td>
    </tr>
    <tr id="row1497319479114"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p16237545554"><a name="p16237545554"></a><a name="p16237545554"></a>域名</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.470000000000006%" headers="mcps1.2.4.1.2 "><p id="p17231354165514"><a name="p17231354165514"></a><a name="p17231354165514"></a>健康检查的请求域名。</p>
    <p id="p72365420558"><a name="p72365420558"></a><a name="p72365420558"></a>默认值为空，由数字、字母、‘-’、‘.’组成的字符串，只能以数字或字符开头。</p>
    <p id="p22312547558"><a name="p22312547558"></a><a name="p22312547558"></a>只有健康检查协议为HTTP时，需要设置。</p>
    </td>
    <td class="cellrowborder" valign="top" width="24.11%" headers="mcps1.2.4.1.3 "><p id="p1223155420552"><a name="p1223155420552"></a><a name="p1223155420552"></a>www.elb.com</p>
    </td>
    </tr>
    <tr id="row3885362315"><td class="cellrowborder" colspan="3" valign="top" headers="mcps1.2.4.1.1 mcps1.2.4.1.2 mcps1.2.4.1.3 "><p id="p58185318238"><a name="p58185318238"></a><a name="p58185318238"></a><strong id="b17845313235"><a name="b17845313235"></a><a name="b17845313235"></a>健康检查配置</strong></p>
    </td>
    </tr>
    <tr id="row15855342319"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p1280535238"><a name="p1280535238"></a><a name="p1280535238"></a>检查间隔（秒）</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.470000000000006%" headers="mcps1.2.4.1.2 "><p id="p3815538233"><a name="p3815538233"></a><a name="p3815538233"></a>每次健康检查响应的最大间隔时间。</p>
    <p id="p14815362320"><a name="p14815362320"></a><a name="p14815362320"></a>取值范围[1-50]。</p>
    </td>
    <td class="cellrowborder" valign="top" width="24.11%" headers="mcps1.2.4.1.3 "><p id="p1087537234"><a name="p1087537234"></a><a name="p1087537234"></a>5</p>
    </td>
    </tr>
    <tr id="row1581153152313"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p17945311234"><a name="p17945311234"></a><a name="p17945311234"></a>超时时间（秒）</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.470000000000006%" headers="mcps1.2.4.1.2 "><p id="p59165342319"><a name="p59165342319"></a><a name="p59165342319"></a>每次健康检查响应的最大超时时间。取值范围[1-50]。</p>
    </td>
    <td class="cellrowborder" valign="top" width="24.11%" headers="mcps1.2.4.1.3 "><p id="p1297536239"><a name="p1297536239"></a><a name="p1297536239"></a>3</p>
    </td>
    </tr>
    <tr id="row167077358544"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p2353591925"><a name="p2353591925"></a><a name="p2353591925"></a>检查路径</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.470000000000006%" headers="mcps1.2.4.1.2 "><p id="p12878163316150"><a name="p12878163316150"></a><a name="p12878163316150"></a>指定健康检查的URL地址。当“协议”为HTTP时生效。检查路径只能以/开头，长度范围[1-80]。</p>
    <p id="p16402112491514"><a name="p16402112491514"></a><a name="p16402112491514"></a>支持使用英文字母、数字和‘-’、‘/’、‘.’、‘%’、‘&amp;’以及特殊字符_~';@$*+,=!:()。</p>
    <div class="note" id="note179341602711"><a name="note179341602711"></a><a name="note179341602711"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p145105291177"><a name="p145105291177"></a><a name="p145105291177"></a>例如：</p>
    <p id="p1343017411767"><a name="p1343017411767"></a><a name="p1343017411767"></a>访问链接为：http://www.example.com/chat/try/，则检查路径填写“/chat/try/”。</p>
    <p id="p134302415611"><a name="p134302415611"></a><a name="p134302415611"></a>访问链接为：http://192.168.63.187:9096/chat/index.html，则检查路径填写“/chat/index.html”。</p>
    </div></div>
    </td>
    <td class="cellrowborder" valign="top" width="24.11%" headers="mcps1.2.4.1.3 "><p id="p10364591129"><a name="p10364591129"></a><a name="p10364591129"></a>/index.html</p>
    </td>
    </tr>
    <tr id="row3915314238"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p1995311231"><a name="p1995311231"></a><a name="p1995311231"></a>最大重试次数</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.470000000000006%" headers="mcps1.2.4.1.2 "><p id="p51019539239"><a name="p51019539239"></a><a name="p51019539239"></a>健康检查最大的重试次数，取值范围[1-10]。</p>
    </td>
    <td class="cellrowborder" valign="top" width="24.11%" headers="mcps1.2.4.1.3 "><p id="p121018539233"><a name="p121018539233"></a><a name="p121018539233"></a>3</p>
    </td>
    </tr>
    <tr id="row689065535313"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p1371712513442"><a name="p1371712513442"></a><a name="p1371712513442"></a>HTTP状态码</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.470000000000006%" headers="mcps1.2.4.1.2 "><p id="p4717162511446"><a name="p4717162511446"></a><a name="p4717162511446"></a>自定义健康检查返回的状态码。当“协议”为HTTP或HTTPS时生效。</p>
    <p id="p1040719418460"><a name="p1040719418460"></a><a name="p1040719418460"></a>可输入200-599范围内不重复的单个数字或正序的数字区间。多个HTTP状态码使用逗号隔开，最多支持5个。</p>
    <div class="note" id="note6346155819386"><a name="note6346155819386"></a><a name="note6346155819386"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p734665812387"><a name="p734665812387"></a><a name="p734665812387"></a>如果您要使用该特性，请进入至ELB服务控制台后，单击页面左下角的“体验新版”。目前新版控制台在公测中，待公测结束后即可正常使用。</p>
    </div></div>
    </td>
    <td class="cellrowborder" valign="top" width="24.11%" headers="mcps1.2.4.1.3 "><p id="p6718162517447"><a name="p6718162517447"></a><a name="p6718162517447"></a>200</p>
    </td>
    </tr>
    </tbody>
    </table>

8.  单击“下一步：确认配置”。
9.  确认配置无误后，单击“提交”。

## 添加共享型负载均衡HTTP监听器<a name="section18262194013551"></a>

1.  登录管理控制台。
2.  在管理控制台左上角单击![](figures/icon-region.png)图标，选择区域和项目。
3.  单击页面左上角的![](figures/icon-position.png)，选择“网络 \> 弹性负载均衡”。
4.  在“负载均衡器”界面，单击需要添加监听器的负载均衡名称。
5.  切换到“监听器”页签，单击“添加监听器”，配置监听器。配置监听器参数参见[表4](#table20377204713512)。

    **表 4** 共享型负载均衡配置监听器参数说明

    <a name="table20377204713512"></a>
    <table><thead align="left"><tr id="row1337215478357"><th class="cellrowborder" valign="top" width="23.419999999999998%" id="mcps1.2.4.1.1"><p id="p13372647103517"><a name="p13372647103517"></a><a name="p13372647103517"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="46.72%" id="mcps1.2.4.1.2"><p id="p15372647173513"><a name="p15372647173513"></a><a name="p15372647173513"></a>说明</p>
    </th>
    <th class="cellrowborder" valign="top" width="29.86%" id="mcps1.2.4.1.3"><p id="p13372647193520"><a name="p13372647193520"></a><a name="p13372647193520"></a>示例</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row113721747113516"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p237294719359"><a name="p237294719359"></a><a name="p237294719359"></a>名称</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.72%" headers="mcps1.2.4.1.2 "><p id="p103726475354"><a name="p103726475354"></a><a name="p103726475354"></a>监听器名称。</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.86%" headers="mcps1.2.4.1.3 "><p id="p1237254713352"><a name="p1237254713352"></a><a name="p1237254713352"></a>listener-pnqy</p>
    </td>
    </tr>
    <tr id="row6373114743514"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p74310441560"><a name="p74310441560"></a><a name="p74310441560"></a>前端协议</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.72%" headers="mcps1.2.4.1.2 "><p id="p743184415615"><a name="p743184415615"></a><a name="p743184415615"></a>客户端与负载均衡监听器建立流量分发连接的协议。</p>
    <p id="p94324415619"><a name="p94324415619"></a><a name="p94324415619"></a>协议选择HTTP。</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.86%" headers="mcps1.2.4.1.3 "><p id="p63739472356"><a name="p63739472356"></a><a name="p63739472356"></a>HTTP</p>
    </td>
    </tr>
    <tr id="row13870025165211"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p20436447616"><a name="p20436447616"></a><a name="p20436447616"></a>前端端口</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.72%" headers="mcps1.2.4.1.2 "><p id="p943124410613"><a name="p943124410613"></a><a name="p943124410613"></a>客户端与负载均衡监听器建立流量分发连接的端口。</p>
    <p id="p14313441668"><a name="p14313441668"></a><a name="p14313441668"></a>取值范围为：[1-65535]。</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.86%" headers="mcps1.2.4.1.3 "><p id="p7870122520524"><a name="p7870122520524"></a><a name="p7870122520524"></a>80</p>
    </td>
    </tr>
    <tr id="row14321151212517"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p149412188913"><a name="p149412188913"></a><a name="p149412188913"></a>重定向</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.72%" headers="mcps1.2.4.1.2 "><p id="p2941018999"><a name="p2941018999"></a><a name="p2941018999"></a>重定向开关是否开启。</p>
    <p id="p19947187915"><a name="p19947187915"></a><a name="p19947187915"></a>协议类型为HTTP时，可根据需要设置该项。需要保证业务建立安全连接时，若同时创建了HTTPS监听器和HTTP监听器，可以通过重定向功能，将HTTP监听器访问重定向至HTTPS监听器。</p>
    <p id="p6941018290"><a name="p6941018290"></a><a name="p6941018290"></a><span id="ph119431817915"><a name="ph119431817915"></a><a name="ph119431817915"></a>HTTP监听器被重定向后，会返回301返回码。</span></p>
    </td>
    <td class="cellrowborder" valign="top" width="29.86%" headers="mcps1.2.4.1.3 "><p id="p59419181893"><a name="p59419181893"></a><a name="p59419181893"></a>-</p>
    </td>
    </tr>
    <tr id="row109201311695"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p109451816910"><a name="p109451816910"></a><a name="p109451816910"></a>重定向至</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.72%" headers="mcps1.2.4.1.2 "><p id="p89419186916"><a name="p89419186916"></a><a name="p89419186916"></a>选择需要重定向HTTPS监听器的名称。</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.86%" headers="mcps1.2.4.1.3 "><p id="p49417183912"><a name="p49417183912"></a><a name="p49417183912"></a>-listener-9ecd（HTTPS/443）</p>
    </td>
    </tr>
    <tr id="row2375164733519"><td class="cellrowborder" colspan="3" valign="top" headers="mcps1.2.4.1.1 mcps1.2.4.1.2 mcps1.2.4.1.3 "><p id="p337544716354"><a name="p337544716354"></a><a name="p337544716354"></a><strong id="b25661342132015"><a name="b25661342132015"></a><a name="b25661342132015"></a>高级配置</strong></p>
    </td>
    </tr>
    <tr id="row147733330354"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p4619133542414"><a name="p4619133542414"></a><a name="p4619133542414"></a>访问策略</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.72%" headers="mcps1.2.4.1.2 "><p id="p16195358244"><a name="p16195358244"></a><a name="p16195358244"></a>支持通过白名单和黑名单进行访问控制，更多信息请参见<a href="访问控制策略.md">访问控制策略</a>：</p>
    <a name="ul161301312102917"></a><a name="ul161301312102917"></a><ul id="ul161301312102917"><li>允许所有IP访问</li><li>黑名单</li><li>白名单</li></ul>
    </td>
    <td class="cellrowborder" valign="top" width="29.86%" headers="mcps1.2.4.1.3 "><p id="p861993572415"><a name="p861993572415"></a><a name="p861993572415"></a>白名单</p>
    </td>
    </tr>
    <tr id="row134742317358"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p840321417258"><a name="p840321417258"></a><a name="p840321417258"></a>IP地址组</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.72%" headers="mcps1.2.4.1.2 "><p id="p1484541812184"><a name="p1484541812184"></a><a name="p1484541812184"></a>设置白名单或者黑名单时，必须选择一个IP地址组。如果还未创建IP地址组，需要先创建IP地址组，更多关于IP地址组的信息请参见<a href="IP地址组（黑名单-白名单）.md">IP地址组（黑名单/白名单）</a>。</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.86%" headers="mcps1.2.4.1.3 "><p id="p11574181042917"><a name="p11574181042917"></a><a name="p11574181042917"></a>ipGroup-b2</p>
    </td>
    </tr>
    <tr id="row1780834016918"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p1715512711018"><a name="p1715512711018"></a><a name="p1715512711018"></a>获取弹性公网IP</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.72%" headers="mcps1.2.4.1.2 "><p id="p41552276106"><a name="p41552276106"></a><a name="p41552276106"></a>通过X-Forwarded-ELB-IP头字段获取ELB实例公网IP地址。</p>
    <p id="p18155227171010"><a name="p18155227171010"></a><a name="p18155227171010"></a>若您需要将ELB公网IP透传到后端，只需在创建HTTP监听器时，打开该开关。</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.86%" headers="mcps1.2.4.1.3 "><p id="p191551827131014"><a name="p191551827131014"></a><a name="p191551827131014"></a>-</p>
    </td>
    </tr>
    <tr id="row102731948169"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p888716515119"><a name="p888716515119"></a><a name="p888716515119"></a>空闲超时时间（秒）</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.72%" headers="mcps1.2.4.1.2 "><p id="p388712512115"><a name="p388712512115"></a><a name="p388712512115"></a>如果在超时时间内一直没有访问请求，负载均衡会中断当前连接，直到下一次请求到来时再重新建立新的连接。</p>
    <p id="p38874512119"><a name="p38874512119"></a><a name="p38874512119"></a>时间取值范围[0-4000]。</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.86%" headers="mcps1.2.4.1.3 "><p id="p688775161114"><a name="p688775161114"></a><a name="p688775161114"></a>60</p>
    </td>
    </tr>
    <tr id="row1486019538912"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p1888719561115"><a name="p1888719561115"></a><a name="p1888719561115"></a>请求超时时间（秒）</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.72%" headers="mcps1.2.4.1.2 "><p id="p48876551111"><a name="p48876551111"></a><a name="p48876551111"></a>客户端向负载均衡发起请求，如果在超时时间内客户端没有完成整个请求的传输，负载均衡将放弃等待关闭连接。</p>
    <p id="p888710510119"><a name="p888710510119"></a><a name="p888710510119"></a>时间取值范围[1-300]。</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.86%" headers="mcps1.2.4.1.3 "><p id="p588765161116"><a name="p588765161116"></a><a name="p588765161116"></a>60</p>
    </td>
    </tr>
    <tr id="row2867195716918"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p19888657117"><a name="p19888657117"></a><a name="p19888657117"></a>响应超时时间（秒）</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.72%" headers="mcps1.2.4.1.2 "><p id="p08881254111"><a name="p08881254111"></a><a name="p08881254111"></a>负载均衡向后端服务器发起请求，如果超时时间内接收请求的后端服务器无响应，负载均衡会向其他后端服务器重试请求。如果重试期间后端服务器一直没有响应，则负载均衡会给客户端返回HTTP 504错误码。</p>
    <p id="p178881759114"><a name="p178881759114"></a><a name="p178881759114"></a>时间取值范围[1-300]。</p>
    <div class="note" id="note9888205101115"><a name="note9888205101115"></a><a name="note9888205101115"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p158885515119"><a name="p158885515119"></a><a name="p158885515119"></a>当开启了会话保持功能时，响应超时时间内如果对应的后端服务器无响应，则直接会返回HTTP 504错误码。</p>
    </div></div>
    </td>
    <td class="cellrowborder" valign="top" width="29.86%" headers="mcps1.2.4.1.3 "><p id="p11888551113"><a name="p11888551113"></a><a name="p11888551113"></a>60</p>
    </td>
    </tr>
    <tr id="row143761647163518"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p237634710356"><a name="p237634710356"></a><a name="p237634710356"></a>描述</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.72%" headers="mcps1.2.4.1.2 "><p id="p23761447103512"><a name="p23761447103512"></a><a name="p23761447103512"></a>对于监听器描述。</p>
    <p id="p475022217118"><a name="p475022217118"></a><a name="p475022217118"></a>字数范围：0/255。</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.86%" headers="mcps1.2.4.1.3 "><p id="p437644773515"><a name="p437644773515"></a><a name="p437644773515"></a>-</p>
    </td>
    </tr>
    </tbody>
    </table>

6.  单击“下一步：配置后端分配策略”。配置后端服务器组参数请参见[表5](#table3561446373)。

    **表 5** 共享型负载均衡配置后端服务器组参数说明

    <a name="table3561446373"></a>
    <table><thead align="left"><tr id="row11555104193715"><th class="cellrowborder" valign="top" width="23.419999999999998%" id="mcps1.2.4.1.1"><p id="p85551445373"><a name="p85551445373"></a><a name="p85551445373"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="50.43%" id="mcps1.2.4.1.2"><p id="p185555413375"><a name="p185555413375"></a><a name="p185555413375"></a>说明</p>
    </th>
    <th class="cellrowborder" valign="top" width="26.150000000000002%" id="mcps1.2.4.1.3"><p id="p755524163717"><a name="p755524163717"></a><a name="p755524163717"></a>示例</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row95561142372"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p1255518414378"><a name="p1255518414378"></a><a name="p1255518414378"></a>后端<span id="text594285384914"><a name="text594285384914"></a><a name="text594285384914"></a>服务器</span>组</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.43%" headers="mcps1.2.4.1.2 "><p id="p1155517417374"><a name="p1155517417374"></a><a name="p1155517417374"></a>把具有相同特性的后端<span id="text23731024185018"><a name="text23731024185018"></a><a name="text23731024185018"></a>服务器</span>放在一个组。</p>
    <a name="ul35562047371"></a><a name="ul35562047371"></a><ul id="ul35562047371"><li>新创建</li><li>使用已有<div class="note" id="note1507185012389"><a name="note1507185012389"></a><a name="note1507185012389"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="zh-cn_topic_0242751126_p1494711463437_1"><a name="zh-cn_topic_0242751126_p1494711463437_1"></a><a name="zh-cn_topic_0242751126_p1494711463437_1"></a><span id="zh-cn_topic_0242751126_ph157831728154313_1"><a name="zh-cn_topic_0242751126_ph157831728154313_1"></a><a name="zh-cn_topic_0242751126_ph157831728154313_1"></a>使用已有后端<span id="zh-cn_topic_0242751126_ph177241201433_1"><a name="zh-cn_topic_0242751126_ph177241201433_1"></a><a name="zh-cn_topic_0242751126_ph177241201433_1"></a>服务器</span>组时，请确保此后端<span id="zh-cn_topic_0242751126_ph10299216174319_1"><a name="zh-cn_topic_0242751126_ph10299216174319_1"></a><a name="zh-cn_topic_0242751126_ph10299216174319_1"></a>服务器</span>组未被使用。并且只能选择前端协议匹配的后端<span id="zh-cn_topic_0242751126_ph16724182224314_1"><a name="zh-cn_topic_0242751126_ph16724182224314_1"></a><a name="zh-cn_topic_0242751126_ph16724182224314_1"></a>服务器</span>组。例如前端协议是TCP时，后端协议只能是TCP。</span></p>
    </div></div>
    </li></ul>
    </td>
    <td class="cellrowborder" valign="top" width="26.150000000000002%" headers="mcps1.2.4.1.3 "><p id="p18556194173710"><a name="p18556194173710"></a><a name="p18556194173710"></a>新创建</p>
    </td>
    </tr>
    <tr id="row1955634173711"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p195565417375"><a name="p195565417375"></a><a name="p195565417375"></a>名称</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.43%" headers="mcps1.2.4.1.2 "><p id="p155569413712"><a name="p155569413712"></a><a name="p155569413712"></a>后端<span id="text153723316504"><a name="text153723316504"></a><a name="text153723316504"></a>服务器</span>组名称。</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.150000000000002%" headers="mcps1.2.4.1.3 "><p id="p655618416379"><a name="p655618416379"></a><a name="p655618416379"></a>server_group-sq4v</p>
    </td>
    </tr>
    <tr id="row3556114153716"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p1655616416379"><a name="p1655616416379"></a><a name="p1655616416379"></a>后端协议</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.43%" headers="mcps1.2.4.1.2 "><p id="p9556184133715"><a name="p9556184133715"></a><a name="p9556184133715"></a>云服务器开通的协议。</p>
    <p id="p12212624143913"><a name="p12212624143913"></a><a name="p12212624143913"></a>前端协议为HTTP时，后端协议默认为HTTP，不支持修改。</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.150000000000002%" headers="mcps1.2.4.1.3 "><p id="p3556348372"><a name="p3556348372"></a><a name="p3556348372"></a>HTTP</p>
    </td>
    </tr>
    <tr id="row555915403715"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p1755654113720"><a name="p1755654113720"></a><a name="p1755654113720"></a>分配策略类型</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.43%" headers="mcps1.2.4.1.2 "><p id="p175561746372"><a name="p175561746372"></a><a name="p175561746372"></a>负载均衡采用的算法。</p>
    <a name="ul95599453720"></a><a name="ul95599453720"></a><ul id="ul95599453720"><li>加权轮询算法：根据后端服务器的权重，按顺序依次将请求分发给不同的服务器。它用相应的权重表示服务器的处理性能，按照权重的高低以及轮询方式将请求分配给各服务器，相同权重的服务器处理相同数目的连接数。</li><li>加权最少连接：最少连接是通过当前活跃的连接数来估计服务器负载情况的一种动态调度算法。加权最少连接就是在最少连接数的基础上，根据服务器的不同处理能力，给每个服务器分配不同的权重，使其能够接受相应权值数的服务请求。</li><li>源IP算法：将请求的源IP地址进行一致性Hash运算，得到一个具体的数值，同时对后端服务器进行编号，按照运算结果将请求分发到对应编号的服务器上。这可以使得对不同源IP的访问进行负载分发，同时使得同一个客户端IP的请求始终被派发至某特定的服务器。</li></ul>
    <div class="note" id="note7559845371"><a name="note7559845371"></a><a name="note7559845371"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="ul77115484370"></a><a name="ul77115484370"></a><ul id="ul77115484370"><li>用户可以根据自身需求选择相应的算法来分配用户访问流量，提升负载均衡能力。</li><li>对于加权轮询算法和加权最少连接，当服务器的权重为“0”时，将不会被分发访问请求。</li></ul>
    </div></div>
    </td>
    <td class="cellrowborder" valign="top" width="26.150000000000002%" headers="mcps1.2.4.1.3 "><p id="p105591463716"><a name="p105591463716"></a><a name="p105591463716"></a>加权轮询算法</p>
    </td>
    </tr>
    <tr id="row25605412371"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p15559104143712"><a name="p15559104143712"></a><a name="p15559104143712"></a>会话保持</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.43%" headers="mcps1.2.4.1.2 "><p id="p75601413375"><a name="p75601413375"></a><a name="p75601413375"></a>开启会话保持后，弹性负载均衡将属于同一个会话的请求都转发到同一个<span id="text7245255105020"><a name="text7245255105020"></a><a name="text7245255105020"></a>服务器</span>进行处理。</p>
    <div class="note" id="note169761956101212"><a name="note169761956101212"></a><a name="note169761956101212"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p15976856191215"><a name="p15976856191215"></a><a name="p15976856191215"></a>当分配策略类型为“加权轮询算法”或"加权最少连接”时，可配置会话保持。</p>
    </div></div>
    </td>
    <td class="cellrowborder" valign="top" width="26.150000000000002%" headers="mcps1.2.4.1.3 "><p id="p256011415372"><a name="p256011415372"></a><a name="p256011415372"></a>-</p>
    </td>
    </tr>
    <tr id="row8560204133710"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p17560144143718"><a name="p17560144143718"></a><a name="p17560144143718"></a>会话保持类型</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.43%" headers="mcps1.2.4.1.2 "><p id="p125601473720"><a name="p125601473720"></a><a name="p125601473720"></a>共享型负载均衡，HTTP和HTTPS协议支持负载均衡器cookie、应用程序cookie类型。</p>
    <a name="ul1232481161411"></a><a name="ul1232481161411"></a><ul id="ul1232481161411"><li><strong id="elb_ug_jt_0004_b253964721712_1"><a name="elb_ug_jt_0004_b253964721712_1"></a><a name="elb_ug_jt_0004_b253964721712_1"></a>负载均衡器cookie：</strong>负载均衡器会根据客户端第一个请求生成一个cookie，后续所有包含这个cookie值的请求都会由同一个后端<span id="elb_ug_jt_0004_ph197863419101_1"><a name="elb_ug_jt_0004_ph197863419101_1"></a><a name="elb_ug_jt_0004_ph197863419101_1"></a>服务器</span>处理。</li><li><strong id="elb_ug_jt_0004_b151925118179"><a name="elb_ug_jt_0004_b151925118179"></a><a name="elb_ug_jt_0004_b151925118179"></a>应用程序cookie</strong>：该选项依赖于后端应用。后端应用生成一个cookie值，后续所有包含这个cookie值的请求都会由同一个后端<span id="elb_ug_jt_0004_ph1897221011106"><a name="elb_ug_jt_0004_ph1897221011106"></a><a name="elb_ug_jt_0004_ph1897221011106"></a>服务器</span>处理。</li></ul>
    </td>
    <td class="cellrowborder" valign="top" width="26.150000000000002%" headers="mcps1.2.4.1.3 "><p id="p1156044163717"><a name="p1156044163717"></a><a name="p1156044163717"></a>负载均衡cookie</p>
    </td>
    </tr>
    <tr id="row12622812151614"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0237163437_zh-cn_topic_0052569729_zh-cn_topic_0091131437_zh-cn_topic_0015479923_p14147913531"><a name="zh-cn_topic_0237163437_zh-cn_topic_0052569729_zh-cn_topic_0091131437_zh-cn_topic_0015479923_p14147913531"></a><a name="zh-cn_topic_0237163437_zh-cn_topic_0052569729_zh-cn_topic_0091131437_zh-cn_topic_0015479923_p14147913531"></a>cookie名称</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.43%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0237163437_zh-cn_topic_0052569729_zh-cn_topic_0091131437_zh-cn_topic_0015479923_p10414159125310"><a name="zh-cn_topic_0237163437_zh-cn_topic_0052569729_zh-cn_topic_0091131437_zh-cn_topic_0015479923_p10414159125310"></a><a name="zh-cn_topic_0237163437_zh-cn_topic_0052569729_zh-cn_topic_0091131437_zh-cn_topic_0015479923_p10414159125310"></a>当会话保持选择应用程序cookie时，需要填写cookie名称。</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.150000000000002%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0237163437_zh-cn_topic_0052569729_zh-cn_topic_0091131437_zh-cn_topic_0015479923_p194143935314"><a name="zh-cn_topic_0237163437_zh-cn_topic_0052569729_zh-cn_topic_0091131437_zh-cn_topic_0015479923_p194143935314"></a><a name="zh-cn_topic_0237163437_zh-cn_topic_0052569729_zh-cn_topic_0091131437_zh-cn_topic_0015479923_p194143935314"></a>cookieName-qsps</p>
    </td>
    </tr>
    <tr id="row16561745372"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p1856111415375"><a name="p1856111415375"></a><a name="p1856111415375"></a>会话保持时间（分钟）</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.43%" headers="mcps1.2.4.1.2 "><p id="p6269182364414"><a name="p6269182364414"></a><a name="p6269182364414"></a>当分配策略类型选择“加权轮询算法”或“加权最少连接”，会话保持开启后，需添加会话保持时间。</p>
    <a name="ul1386252534410"></a><a name="ul1386252534410"></a><ul id="ul1386252534410"><li>四层会话保持的会话保持时间取值范围为[1，60]。</li><li>七层会话保持的会话保持时间取值范围为[1，1440]。</li></ul>
    </td>
    <td class="cellrowborder" valign="top" width="26.150000000000002%" headers="mcps1.2.4.1.3 "><p id="p205618423715"><a name="p205618423715"></a><a name="p205618423715"></a>20</p>
    </td>
    </tr>
    <tr id="row656113463715"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p1656119416373"><a name="p1656119416373"></a><a name="p1656119416373"></a>描述</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.43%" headers="mcps1.2.4.1.2 "><p id="p9561204183712"><a name="p9561204183712"></a><a name="p9561204183712"></a>后端<span id="text12251834518"><a name="text12251834518"></a><a name="text12251834518"></a>服务器</span>组的描述。</p>
    <p id="p10181124063217"><a name="p10181124063217"></a><a name="p10181124063217"></a>字数范围：0/255。</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.150000000000002%" headers="mcps1.2.4.1.3 "><p id="p155619417372"><a name="p155619417372"></a><a name="p155619417372"></a>-</p>
    </td>
    </tr>
    </tbody>
    </table>

7.  单击“下一步：添加后端服务器”。添加后端服务器并配置健康检查。添加后端服务器详见[添加或移除后端服务器（共享型）](添加或移除后端服务器（共享型）.md)，配置健康检查参数请参见[表6](#table95680412371)。

    **表 6** 共享型负载均衡配置健康检查参数说明

    <a name="table95680412371"></a>
    <table><thead align="left"><tr id="row1256210411378"><th class="cellrowborder" valign="top" width="23.419999999999998%" id="mcps1.2.4.1.1"><p id="p156218414377"><a name="p156218414377"></a><a name="p156218414377"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="46.7%" id="mcps1.2.4.1.2"><p id="p45620443711"><a name="p45620443711"></a><a name="p45620443711"></a>说明</p>
    </th>
    <th class="cellrowborder" valign="top" width="29.880000000000003%" id="mcps1.2.4.1.3"><p id="p185622433710"><a name="p185622433710"></a><a name="p185622433710"></a>示例</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row456214163715"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p105621646371"><a name="p105621646371"></a><a name="p105621646371"></a>是否开启</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.7%" headers="mcps1.2.4.1.2 "><p id="p175623416377"><a name="p175623416377"></a><a name="p175623416377"></a>开启或者关闭健康检查。</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.880000000000003%" headers="mcps1.2.4.1.3 "><p id="p1756213415373"><a name="p1756213415373"></a><a name="p1756213415373"></a>-</p>
    </td>
    </tr>
    <tr id="row1556318453710"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p175624417375"><a name="p175624417375"></a><a name="p175624417375"></a>协议</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.7%" headers="mcps1.2.4.1.2 "><p id="p1939517507163"><a name="p1939517507163"></a><a name="p1939517507163"></a>健康检查支持TCP、HTTP协议，设置后不可修改。</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.880000000000003%" headers="mcps1.2.4.1.3 "><p id="p65626414372"><a name="p65626414372"></a><a name="p65626414372"></a>HTTP</p>
    </td>
    </tr>
    <tr id="row1756314153720"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p195631416374"><a name="p195631416374"></a><a name="p195631416374"></a>端口</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.7%" headers="mcps1.2.4.1.2 "><p id="p1956313417375"><a name="p1956313417375"></a><a name="p1956313417375"></a>健康检查端口号，取值范围[1，65535]，为可选参数。</p>
    <div class="note" id="note35631403712"><a name="note35631403712"></a><a name="note35631403712"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p1056315493716"><a name="p1056315493716"></a><a name="p1056315493716"></a>未配置健康检查端口时，默认使用后端云服务器端口进行健康检查。配置后，使用配置的健康检查端口进行健康检查。</p>
    </div></div>
    </td>
    <td class="cellrowborder" valign="top" width="29.880000000000003%" headers="mcps1.2.4.1.3 "><p id="p19563940375"><a name="p19563940375"></a><a name="p19563940375"></a>80</p>
    </td>
    </tr>
    <tr id="row9363110881"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p1563841377"><a name="p1563841377"></a><a name="p1563841377"></a>域名</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.7%" headers="mcps1.2.4.1.2 "><p id="p126107501713"><a name="p126107501713"></a><a name="p126107501713"></a>健康检查的请求域名。</p>
    <p id="p16303138161710"><a name="p16303138161710"></a><a name="p16303138161710"></a>默认值为空，由数字、字母、‘-’、‘.’组成的字符串，只能以数字或字符开头。</p>
    <p id="p175631947374"><a name="p175631947374"></a><a name="p175631947374"></a>只有健康检查协议为HTTP时，需要设置。</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.880000000000003%" headers="mcps1.2.4.1.3 "><p id="p256311403714"><a name="p256311403714"></a><a name="p256311403714"></a>www.elb.com</p>
    </td>
    </tr>
    <tr id="row3365201011337"><td class="cellrowborder" colspan="3" valign="top" headers="mcps1.2.4.1.1 mcps1.2.4.1.2 mcps1.2.4.1.3 "><p id="p2366191073319"><a name="p2366191073319"></a><a name="p2366191073319"></a><strong id="b842691814334"><a name="b842691814334"></a><a name="b842691814334"></a>健康检查配置</strong></p>
    </td>
    </tr>
    <tr id="row456394163714"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p195635417372"><a name="p195635417372"></a><a name="p195635417372"></a>检查间隔（秒）</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.7%" headers="mcps1.2.4.1.2 "><p id="p10563104203711"><a name="p10563104203711"></a><a name="p10563104203711"></a>每次健康检查响应的最大间隔时间。</p>
    <p id="p15639419374"><a name="p15639419374"></a><a name="p15639419374"></a>取值范围[1-50]。</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.880000000000003%" headers="mcps1.2.4.1.3 "><p id="p5563148375"><a name="p5563148375"></a><a name="p5563148375"></a>5</p>
    </td>
    </tr>
    <tr id="row205644443718"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p25631040376"><a name="p25631040376"></a><a name="p25631040376"></a>超时时间（秒）</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.7%" headers="mcps1.2.4.1.2 "><p id="p75641743371"><a name="p75641743371"></a><a name="p75641743371"></a>每次健康检查响应的最大超时时间。取值范围[1-50]。</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.880000000000003%" headers="mcps1.2.4.1.3 "><p id="p175641747374"><a name="p175641747374"></a><a name="p175641747374"></a>3</p>
    </td>
    </tr>
    <tr id="row7791163020103"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p181111841128"><a name="p181111841128"></a><a name="p181111841128"></a>检查路径</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.7%" headers="mcps1.2.4.1.2 "><p id="p18111164111217"><a name="p18111164111217"></a><a name="p18111164111217"></a>指定健康检查的URL地址。当“协议”为HTTP时生效。检查路径只能以/开头，长度范围[1-80]。</p>
    <p id="p1252312932013"><a name="p1252312932013"></a><a name="p1252312932013"></a>支持使用英文字母、数字和‘-’、‘/’、‘.’、‘%’、‘&amp;’以及特殊字符_~';@$*+,=!:()。</p>
    <div class="note" id="note01115461218"><a name="note01115461218"></a><a name="note01115461218"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p121125411125"><a name="p121125411125"></a><a name="p121125411125"></a>例如：</p>
    <p id="p1811210411215"><a name="p1811210411215"></a><a name="p1811210411215"></a>访问链接为：http://www.example.com/chat/try/，则检查路径填写“/chat/try/”。</p>
    <p id="p311264121213"><a name="p311264121213"></a><a name="p311264121213"></a>访问链接为：http://192.168.63.187:9096/chat/index.html，则检查路径填写“/chat/index.html”。</p>
    </div></div>
    </td>
    <td class="cellrowborder" valign="top" width="29.880000000000003%" headers="mcps1.2.4.1.3 "><p id="p1112145120"><a name="p1112145120"></a><a name="p1112145120"></a>/index.html</p>
    </td>
    </tr>
    <tr id="row16567144143718"><td class="cellrowborder" valign="top" width="23.419999999999998%" headers="mcps1.2.4.1.1 "><p id="p356411463720"><a name="p356411463720"></a><a name="p356411463720"></a>最大重试次数</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.7%" headers="mcps1.2.4.1.2 "><p id="p3567184103716"><a name="p3567184103716"></a><a name="p3567184103716"></a>健康检查最大的重试次数，取值范围[1-10]。</p>
    </td>
    <td class="cellrowborder" valign="top" width="29.880000000000003%" headers="mcps1.2.4.1.3 "><p id="p11567194133711"><a name="p11567194133711"></a><a name="p11567194133711"></a>3</p>
    </td>
    </tr>
    </tbody>
    </table>

8.  单击“下一步：确认配置”。
9.  确认配置无误后，单击“提交”。

