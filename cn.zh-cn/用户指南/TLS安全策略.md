# TLS安全策略<a name="elb_ug_jt_0022"></a>

## 操作场景<a name="section15451157527"></a>

对于银行，金融类加密传输的应用 ，在创建和配置HTTPS监听器时，您可以选择使用安全策略，可以提高您的业务安全性。安全策略包含TLS协议版本和配套的加密算法套件。您可以选择默认安全策略，或创建自定义安全策略。

>![](public_sys-resources/icon-note.gif) **说明：** 
>如果您要创建/使用“自定义安全策略”，请进入至ELB服务控制台后，单击页面左下角的“体验新版”。目前新版控制台在公测中，待公测结束后即可正常使用。

## 添加安全策略<a name="section76346198117"></a>

1.  登录管理控制台。
2.  在管理控制台左上角单击![](figures/icon-region.png)图标，选择区域和项目。
3.  单击页面左上角的![](figures/icon-position.png)，选择“网络 \> 弹性负载均衡”。
4.  在“负载均衡器”界面，单击需要创建安全策略的监听器的负载均衡器名称。
5.  在该负载均衡界面的“监听器”区域，单击“添加监听器”。
6.  在“添加监听器”界面，前端协议选择“HTTPS”。
7.  在“添加监听器”界面，选择“高级配置 \> 安全策略”。支持选择默认策略或自定义策略。如果列表中无自定义策略，您可以选择[创建自定义策略](#section9832162313111)。默认策略如[表1](#table1247813103533)所示。

    **表 1**  默认安全策略参数说明

    <a name="table1247813103533"></a>
    <table><thead align="left"><tr id="row204784101539"><th class="cellrowborder" valign="top" width="19.259999999999998%" id="mcps1.2.5.1.1"><p id="p147851075312"><a name="p147851075312"></a><a name="p147851075312"></a>名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="13.950000000000001%" id="mcps1.2.5.1.2"><p id="p175102389132"><a name="p175102389132"></a><a name="p175102389132"></a>说明</p>
    </th>
    <th class="cellrowborder" valign="top" width="17.22%" id="mcps1.2.5.1.3"><p id="p2478181015313"><a name="p2478181015313"></a><a name="p2478181015313"></a>支持的TLS版本类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="49.57%" id="mcps1.2.5.1.4"><p id="p5478131085310"><a name="p5478131085310"></a><a name="p5478131085310"></a>使用的加密套件列表</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row125843182408"><td class="cellrowborder" valign="top" width="19.259999999999998%" headers="mcps1.2.5.1.1 "><p id="p12584131812401"><a name="p12584131812401"></a><a name="p12584131812401"></a>TLS-1-0</p>
    </td>
    <td class="cellrowborder" valign="top" width="13.950000000000001%" headers="mcps1.2.5.1.2 "><p id="p030111715443"><a name="p030111715443"></a><a name="p030111715443"></a>支持TLS 1.0、TLS 1.1、TLS 1.2版本与相关加密套件，兼容性好，安全性低。</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.22%" headers="mcps1.2.5.1.3 "><p id="p44847408439"><a name="p44847408439"></a><a name="p44847408439"></a>TLS 1.2</p>
    <p id="p2086324219439"><a name="p2086324219439"></a><a name="p2086324219439"></a>TLS 1.1</p>
    <p id="p1358411811405"><a name="p1358411811405"></a><a name="p1358411811405"></a>TLS 1.0</p>
    </td>
    <td class="cellrowborder" rowspan="3" valign="top" width="49.57%" headers="mcps1.2.5.1.4 "><a name="ul141564120364"></a><a name="ul141564120364"></a><ul id="ul141564120364"><li>ECDHE-RSA-AES256-GCM-SHA384</li><li>ECDHE-RSA-AES128-GCM-SHA256</li><li>ECDHE-ECDSA-AES256-GCM-SHA384</li><li>ECDHE-ECDSA-AES128-GCM-SHA256</li><li>AES128-GCM-SHA256</li><li>AES256-GCM-SHA384</li><li>ECDHE-ECDSA-AES128-SHA256</li><li>ECDHE-RSA-AES128-SHA256</li><li>AES128-SHA256</li><li>AES256-SHA256</li><li>ECDHE-ECDSA-AES256-SHA384</li><li>ECDHE-RSA-AES256-SHA384</li><li>ECDHE-ECDSA-AES128-SHA</li><li>ECDHE-RSA-AES128-SHA</li><li>ECDHE-RSA-AES256-SHA</li><li>ECDHE-ECDSA-AES256-SHA</li><li>AES128-SHA</li><li>AES256-SHA</li></ul>
    </td>
    </tr>
    <tr id="row586052216444"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p050232216409"><a name="p050232216409"></a><a name="p050232216409"></a>TLS-1-1</p>
    </td>
    <td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p13015716444"><a name="p13015716444"></a><a name="p13015716444"></a>支持TLS 1.1、TLS 1.2版本与相关加密套件，兼容性较好，安全性中。</p>
    </td>
    <td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p4920104413437"><a name="p4920104413437"></a><a name="p4920104413437"></a>TLS 1.2</p>
    <p id="p185021822194019"><a name="p185021822194019"></a><a name="p185021822194019"></a>TLS 1.1</p>
    </td>
    </tr>
    <tr id="row178061419194420"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p31598266400"><a name="p31598266400"></a><a name="p31598266400"></a>TLS-1-2</p>
    </td>
    <td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p830177164415"><a name="p830177164415"></a><a name="p830177164415"></a>支持TLS 1.2版本与相关加密套件，兼容性较好，安全性高。</p>
    </td>
    <td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p315914265406"><a name="p315914265406"></a><a name="p315914265406"></a>TLS 1.2</p>
    </td>
    </tr>
    <tr id="row935255214374"><td class="cellrowborder" valign="top" width="19.259999999999998%" headers="mcps1.2.5.1.1 "><p id="p735375213712"><a name="p735375213712"></a><a name="p735375213712"></a>tls-1-0-inherit</p>
    </td>
    <td class="cellrowborder" valign="top" width="13.950000000000001%" headers="mcps1.2.5.1.2 "><p id="p3353105211371"><a name="p3353105211371"></a><a name="p3353105211371"></a>支持TLS 1.0、TLS 1.1、TLS 1.2版本与相关加密套件，兼容性好，安全性低。</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.22%" headers="mcps1.2.5.1.3 "><p id="p51183222383"><a name="p51183222383"></a><a name="p51183222383"></a>TLS 1.2</p>
    <p id="p1411832293810"><a name="p1411832293810"></a><a name="p1411832293810"></a>TLS 1.1</p>
    <p id="p511922217382"><a name="p511922217382"></a><a name="p511922217382"></a>TLS 1.0</p>
    </td>
    <td class="cellrowborder" valign="top" width="49.57%" headers="mcps1.2.5.1.4 "><a name="ul8954152513919"></a><a name="ul8954152513919"></a><ul id="ul8954152513919"><li>ECDHE-RSA-AES256-GCM-SHA384</li><li>ECDHE-RSA-AES128-GCM-SHA256</li><li>ECDHE-ECDSA-AES256-GCM-SHA384</li><li>ECDHE-ECDSA-AES128-GCM-SHA256</li><li>AES128-GCM-SHA256</li><li>AES256-GCM-SHA384</li><li>ECDHE-ECDSA-AES128-SHA256</li><li>ECDHE-RSA-AES128-SHA256</li><li>AES128-SHA256</li><li>AES256-SHA256</li><li>ECDHE-ECDSA-AES256-SHA384</li><li>ECDHE-RSA-AES256-SHA384</li><li>ECDHE-ECDSA-AES128-SHA</li><li>ECDHE-RSA-AES128-SHA</li><li>DHE-RSA-AES128-SHA</li><li>ECDHE-RSA-AES256-SHA</li><li>ECDHE-ECDSA-AES256-SHA</li><li>AES128-SHA</li><li>AES256-SHA</li><li>DHE-DSS-AES128-SHA</li><li>CAMELLIA128-SHA</li><li>EDH-RSA-DES-CBC3-SHA</li><li>DES-CBC3-SHA</li><li>ECDHE-RSA-RC4-SHA</li><li>RC4-SHA</li><li>DHE-RSA-AES256-SHA</li><li>DHE-DSS-AES256-SHA</li><li>DHE-RSA-CAMELLIA256-SHA</li></ul>
    </td>
    </tr>
    <tr id="row148501331204010"><td class="cellrowborder" valign="top" width="19.259999999999998%" headers="mcps1.2.5.1.1 "><p id="p18850153164010"><a name="p18850153164010"></a><a name="p18850153164010"></a>TLS-1-2-Strict</p>
    </td>
    <td class="cellrowborder" valign="top" width="13.950000000000001%" headers="mcps1.2.5.1.2 "><p id="p1130114715442"><a name="p1130114715442"></a><a name="p1130114715442"></a>支持TLS 1.2版本与相关加密套件，兼容性一般，安全性高。</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.22%" headers="mcps1.2.5.1.3 "><p id="p3850531104014"><a name="p3850531104014"></a><a name="p3850531104014"></a>TLS 1.2</p>
    </td>
    <td class="cellrowborder" valign="top" width="49.57%" headers="mcps1.2.5.1.4 "><a name="ul12064436486"></a><a name="ul12064436486"></a><ul id="ul12064436486"><li>ECDHE-RSA-AES256-GCM-SHA384</li><li>ECDHE-RSA-AES128-GCM-SHA256</li><li>ECDHE-ECDSA-AES256-GCM-SHA384</li><li>ECDHE-ECDSA-AES128-GCM-SHA256</li><li>AES128-GCM-SHA256</li><li>AES256-GCM-SHA384</li><li>ECDHE-ECDSA-AES128-SHA256</li><li>ECDHE-RSA-AES128-SHA256</li><li>AES128-SHA256</li><li>AES256-SHA256</li><li>ECDHE-ECDSA-AES256-SHA384</li><li>ECDHE-RSA-AES256-SHA384</li></ul>
    </td>
    </tr>
    <tr id="row993705044213"><td class="cellrowborder" valign="top" width="19.259999999999998%" headers="mcps1.2.5.1.1 "><p id="p1893901244316"><a name="p1893901244316"></a><a name="p1893901244316"></a>TLS-1-0-WITH-1-3（独享型实例）</p>
    </td>
    <td class="cellrowborder" valign="top" width="13.950000000000001%" headers="mcps1.2.5.1.2 "><p id="p29391412184312"><a name="p29391412184312"></a><a name="p29391412184312"></a>支持TLS 1.0及以上版本与相关加密套件，兼容性最好，安全性低。</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.22%" headers="mcps1.2.5.1.3 "><p id="p20940151234315"><a name="p20940151234315"></a><a name="p20940151234315"></a>TLS 1.3</p>
    <p id="p5940512134318"><a name="p5940512134318"></a><a name="p5940512134318"></a>TLS 1.2</p>
    <p id="p29401112114317"><a name="p29401112114317"></a><a name="p29401112114317"></a>TLS 1.1</p>
    <p id="p199401712144317"><a name="p199401712144317"></a><a name="p199401712144317"></a>TLS 1.0</p>
    </td>
    <td class="cellrowborder" valign="top" width="49.57%" headers="mcps1.2.5.1.4 "><a name="ul612718945414"></a><a name="ul612718945414"></a><ul id="ul612718945414"><li>ECDHE-RSA-AES256-GCM-SHA384</li><li>ECDHE-RSA-AES128-GCM-SHA256</li><li>ECDHE-ECDSA-AES256-GCM-SHA384</li><li>ECDHE-ECDSA-AES128-GCM-SHA256</li><li>AES128-GCM-SHA256</li><li>AES256-GCM-SHA384</li><li>ECDHE-ECDSA-AES128-SHA256</li><li>ECDHE-RSA-AES128-SHA256</li><li>AES128-SHA256</li><li>AES256-SHA256</li><li>ECDHE-ECDSA-AES256-SHA384</li><li>ECDHE-RSA-AES256-SHA384</li><li>ECDHE-ECDSA-AES128-SHA</li><li>ECDHE-RSA-AES128-SHA</li><li>ECDHE-RSA-AES256-SHA</li><li>ECDHE-ECDSA-AES256-SHA</li><li>AES128-SHA</li><li>AES256-SHA</li><li>TLS_AES_128_GCM_SHA256</li><li>TLS_AES_256_GCM_SHA384</li><li>TLS_CHACHA20_POLY1305_SHA256</li><li>TLS_AES_128_CCM_SHA256</li><li>TLS_AES_128_CCM_8_SHA256</li></ul>
    </td>
    </tr>
    <tr id="row1155514411417"><td class="cellrowborder" valign="top" width="19.259999999999998%" headers="mcps1.2.5.1.1 "><p id="p994161234315"><a name="p994161234315"></a><a name="p994161234315"></a>TLS-1-2-FS-WITH-1-3（独享型实例）</p>
    </td>
    <td class="cellrowborder" valign="top" width="13.950000000000001%" headers="mcps1.2.5.1.2 "><p id="p69411124432"><a name="p69411124432"></a><a name="p69411124432"></a>支持TLS 1.2及以上版本与前向安全相关的加密套件，兼容性较好，安全性最高。</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.22%" headers="mcps1.2.5.1.3 "><p id="p1094117127431"><a name="p1094117127431"></a><a name="p1094117127431"></a>TLS 1.3</p>
    <p id="p1894141284314"><a name="p1894141284314"></a><a name="p1894141284314"></a>TLS 1.2</p>
    </td>
    <td class="cellrowborder" valign="top" width="49.57%" headers="mcps1.2.5.1.4 "><a name="ul2680103510552"></a><a name="ul2680103510552"></a><ul id="ul2680103510552"><li>ECDHE-RSA-AES256-GCM-SHA384</li><li>ECDHE-RSA-AES128-GCM-SHA256</li><li>ECDHE-ECDSA-AES256-GCM-SHA384</li><li>ECDHE-ECDSA-AES128-GCM-SHA256</li><li>ECDHE-ECDSA-AES128-SHA256</li><li>ECDHE-RSA-AES128-SHA256</li><li>ECDHE-ECDSA-AES256-SHA384</li><li>ECDHE-RSA-AES256-SHA384</li><li>TLS_AES_128_GCM_SHA256</li><li>TLS_AES_256_GCM_SHA384</li><li>TLS_CHACHA20_POLY1305_SHA256</li><li>TLS_AES_128_CCM_SHA256</li><li>TLS_AES_128_CCM_8_SHA256</li></ul>
    </td>
    </tr>
    <tr id="row129382050194218"><td class="cellrowborder" valign="top" width="19.259999999999998%" headers="mcps1.2.5.1.1 "><p id="p1394091218430"><a name="p1394091218430"></a><a name="p1394091218430"></a>TLS-1-2-FS（独享型实例）</p>
    </td>
    <td class="cellrowborder" valign="top" width="13.950000000000001%" headers="mcps1.2.5.1.2 "><p id="p109403125439"><a name="p109403125439"></a><a name="p109403125439"></a>支持TLS 1.2版本与前向安全相关的加密套件，兼容性一般，安全性最高。</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.22%" headers="mcps1.2.5.1.3 "><p id="p12941101215430"><a name="p12941101215430"></a><a name="p12941101215430"></a>TLS 1.2</p>
    </td>
    <td class="cellrowborder" valign="top" width="49.57%" headers="mcps1.2.5.1.4 "><a name="ul229445419519"></a><a name="ul229445419519"></a><ul id="ul229445419519"><li>ECDHE-RSA-AES256-GCM-SHA384</li><li>ECDHE-RSA-AES128-GCM-SHA256</li><li>ECDHE-ECDSA-AES256-GCM-SHA384</li><li>ECDHE-ECDSA-AES128-GCM-SHA256</li><li>ECDHE-ECDSA-AES128-SHA256</li><li>ECDHE-RSA-AES128-SHA256</li><li>ECDHE-ECDSA-AES256-SHA384</li><li>ECDHE-RSA-AES256-SHA384</li></ul>
    </td>
    </tr>
    <tr id="row159881250105511"><td class="cellrowborder" valign="top" width="19.259999999999998%" headers="mcps1.2.5.1.1 "><p id="p1498815065520"><a name="p1498815065520"></a><a name="p1498815065520"></a>hybrid-policy-1-0</p>
    </td>
    <td class="cellrowborder" valign="top" width="13.950000000000001%" headers="mcps1.2.5.1.2 "><p id="p11988195045513"><a name="p11988195045513"></a><a name="p11988195045513"></a>支持TLS 1.1、TLS 1.2版本与相关加密套件，兼容性较好，安全性中。</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.22%" headers="mcps1.2.5.1.3 "><p id="p16988205065516"><a name="p16988205065516"></a><a name="p16988205065516"></a>TLS 1.2</p>
    <p id="p2821190135710"><a name="p2821190135710"></a><a name="p2821190135710"></a>TLS 1.1</p>
    </td>
    <td class="cellrowborder" valign="top" width="49.57%" headers="mcps1.2.5.1.4 "><a name="ul948217775918"></a><a name="ul948217775918"></a><ul id="ul948217775918"><li>ECDHE-RSA-AES256-GCM-SHA384</li><li>ECDHE-RSA-AES128-GCM-SHA256</li><li>ECDHE-ECDSA-AES256-GCM-SHA384</li><li>ECDHE-ECDSA-AES128-GCM-SHA256</li><li>AES128-GCM-SHA256</li><li>AES256-GCM-SHA384</li><li>ECDHE-ECDSA-AES128-SHA256</li><li>ECDHE-RSA-AES128-SHA256</li><li>AES128-SHA256</li><li>AES256-SHA256</li><li>ECDHE-ECDSA-AES256-SHA384</li><li>ECDHE-RSA-AES256-SHA384</li><li>ECDHE-ECDSA-AES128-SHA</li><li>ECDHE-RSA-AES128-SHA</li><li>ECDHE-RSA-AES256-SHA</li><li>ECDHE-ECDSA-AES256-SHA</li><li>AES128-SHA</li><li>AES256-SHA</li><li>ECC-SM4-SM3</li><li>ECDHE-SM4-SM3</li></ul>
    </td>
    </tr>
    </tbody>
    </table>

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >-   安全策略“TLS-1-0-WITH-1-3”、“TLS-1-2-FS-WITH-1-3”、“TLS-1-2-FS”目前仅支持独享型实例。
    >-   目前，独享型负载均衡安全策略最高支持TLS 1.3协议，共享型负载均衡安全策略最高支持TLS 1.2协议。
    >-   上述列表为ELB支持的加密套件，同时客户端也支持多个加密套件，这样在实际使用时，加密套件的选择范围为：ELB和客户端支持的加密套件的交集，加密套件的选择顺序为：ELB支持的加密套件顺序。

8.  配置完成，单击“确定”。

## 安全策略差异说明<a name="section20639534152813"></a>

**表 2**  安全策略差异说明

<a name="table165866510169"></a>
<table><thead align="left"><tr id="row1458720515167"><th class="cellrowborder" valign="top" width="20.453863840847745%" id="mcps1.2.11.1.1"><p id="p8587151191610"><a name="p8587151191610"></a><a name="p8587151191610"></a>安全策略</p>
</th>
<th class="cellrowborder" valign="top" width="8.187543736878936%" id="mcps1.2.11.1.2"><p id="p12587751101614"><a name="p12587751101614"></a><a name="p12587751101614"></a>tls-1-0</p>
</th>
<th class="cellrowborder" valign="top" width="7.807657702689194%" id="mcps1.2.11.1.3"><p id="p12587175114164"><a name="p12587175114164"></a><a name="p12587175114164"></a>tls-1-1</p>
</th>
<th class="cellrowborder" valign="top" width="8.367489753074079%" id="mcps1.2.11.1.4"><p id="p958745121610"><a name="p958745121610"></a><a name="p958745121610"></a>tls-1-2</p>
</th>
<th class="cellrowborder" valign="top" width="8.007597720683796%" id="mcps1.2.11.1.5"><p id="p16766214133415"><a name="p16766214133415"></a><a name="p16766214133415"></a>tls-1-0-inherit</p>
</th>
<th class="cellrowborder" valign="top" width="8.257522743177049%" id="mcps1.2.11.1.6"><p id="p105871751121610"><a name="p105871751121610"></a><a name="p105871751121610"></a>tls-1-2-strict</p>
</th>
<th class="cellrowborder" valign="top" width="9.617114865540339%" id="mcps1.2.11.1.7"><p id="p7587115117166"><a name="p7587115117166"></a><a name="p7587115117166"></a>tls-1-0-with-1-3</p>
</th>
<th class="cellrowborder" valign="top" width="9.89703089073278%" id="mcps1.2.11.1.8"><p id="p1358710518168"><a name="p1358710518168"></a><a name="p1358710518168"></a>tls-1-2-fs-with-1-3</p>
</th>
<th class="cellrowborder" valign="top" width="8.107567729681096%" id="mcps1.2.11.1.9"><p id="p185888514167"><a name="p185888514167"></a><a name="p185888514167"></a>tls-1-2-fs</p>
</th>
<th class="cellrowborder" valign="top" width="11.296611016694992%" id="mcps1.2.11.1.10"><p id="p19840191865418"><a name="p19840191865418"></a><a name="p19840191865418"></a>hybrid-policy-1-0</p>
</th>
</tr>
</thead>
<tbody><tr id="row11588165131620"><td class="cellrowborder" colspan="10" valign="top" headers="mcps1.2.11.1.1 mcps1.2.11.1.2 mcps1.2.11.1.3 mcps1.2.11.1.4 mcps1.2.11.1.5 mcps1.2.11.1.6 mcps1.2.11.1.7 mcps1.2.11.1.8 mcps1.2.11.1.9 mcps1.2.11.1.10 "><p id="p75886517166"><a name="p75886517166"></a><a name="p75886517166"></a>TLS 协议</p>
</td>
</tr>
<tr id="row1358895111614"><td class="cellrowborder" valign="top" width="20.453863840847745%" headers="mcps1.2.11.1.1 "><p id="p7588145101618"><a name="p7588145101618"></a><a name="p7588145101618"></a>Protocol-TLS 1.3</p>
</td>
<td class="cellrowborder" valign="top" width="8.187543736878936%" headers="mcps1.2.11.1.2 "><p id="p758895110169"><a name="p758895110169"></a><a name="p758895110169"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="7.807657702689194%" headers="mcps1.2.11.1.3 "><p id="p358825117166"><a name="p358825117166"></a><a name="p358825117166"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.367489753074079%" headers="mcps1.2.11.1.4 "><p id="p2588551161611"><a name="p2588551161611"></a><a name="p2588551161611"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.007597720683796%" headers="mcps1.2.11.1.5 "><p id="p376771416343"><a name="p376771416343"></a><a name="p376771416343"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.257522743177049%" headers="mcps1.2.11.1.6 "><p id="p9588165111617"><a name="p9588165111617"></a><a name="p9588165111617"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.617114865540339%" headers="mcps1.2.11.1.7 "><p id="p2588135114169"><a name="p2588135114169"></a><a name="p2588135114169"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.89703089073278%" headers="mcps1.2.11.1.8 "><p id="p175884511164"><a name="p175884511164"></a><a name="p175884511164"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.107567729681096%" headers="mcps1.2.11.1.9 "><p id="p14588451111616"><a name="p14588451111616"></a><a name="p14588451111616"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="11.296611016694992%" headers="mcps1.2.11.1.10 "><p id="p15840718165416"><a name="p15840718165416"></a><a name="p15840718165416"></a>-</p>
</td>
</tr>
<tr id="row05885511164"><td class="cellrowborder" valign="top" width="20.453863840847745%" headers="mcps1.2.11.1.1 "><p id="p45881051171616"><a name="p45881051171616"></a><a name="p45881051171616"></a>Protocol-TLS 1.2</p>
</td>
<td class="cellrowborder" valign="top" width="8.187543736878936%" headers="mcps1.2.11.1.2 "><p id="p175881551111619"><a name="p175881551111619"></a><a name="p175881551111619"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="7.807657702689194%" headers="mcps1.2.11.1.3 "><p id="p0588251181614"><a name="p0588251181614"></a><a name="p0588251181614"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.367489753074079%" headers="mcps1.2.11.1.4 "><p id="p8589205113164"><a name="p8589205113164"></a><a name="p8589205113164"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.007597720683796%" headers="mcps1.2.11.1.5 "><p id="p14549194418347"><a name="p14549194418347"></a><a name="p14549194418347"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.257522743177049%" headers="mcps1.2.11.1.6 "><p id="p558945110169"><a name="p558945110169"></a><a name="p558945110169"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.617114865540339%" headers="mcps1.2.11.1.7 "><p id="p85892051131613"><a name="p85892051131613"></a><a name="p85892051131613"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.89703089073278%" headers="mcps1.2.11.1.8 "><p id="p17589175114168"><a name="p17589175114168"></a><a name="p17589175114168"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.107567729681096%" headers="mcps1.2.11.1.9 "><p id="p14589551141617"><a name="p14589551141617"></a><a name="p14589551141617"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="11.296611016694992%" headers="mcps1.2.11.1.10 "><p id="p134445919112"><a name="p134445919112"></a><a name="p134445919112"></a>√</p>
</td>
</tr>
<tr id="row16589165119168"><td class="cellrowborder" valign="top" width="20.453863840847745%" headers="mcps1.2.11.1.1 "><p id="p1658919519163"><a name="p1658919519163"></a><a name="p1658919519163"></a>Protocol-TLS 1.1</p>
</td>
<td class="cellrowborder" valign="top" width="8.187543736878936%" headers="mcps1.2.11.1.2 "><p id="p75891951131615"><a name="p75891951131615"></a><a name="p75891951131615"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="7.807657702689194%" headers="mcps1.2.11.1.3 "><p id="p95891951121618"><a name="p95891951121618"></a><a name="p95891951121618"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.367489753074079%" headers="mcps1.2.11.1.4 "><p id="p258919516169"><a name="p258919516169"></a><a name="p258919516169"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.007597720683796%" headers="mcps1.2.11.1.5 "><p id="p1354915440345"><a name="p1354915440345"></a><a name="p1354915440345"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.257522743177049%" headers="mcps1.2.11.1.6 "><p id="p1058916519165"><a name="p1058916519165"></a><a name="p1058916519165"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.617114865540339%" headers="mcps1.2.11.1.7 "><p id="p1258935141611"><a name="p1258935141611"></a><a name="p1258935141611"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.89703089073278%" headers="mcps1.2.11.1.8 "><p id="p8589551191615"><a name="p8589551191615"></a><a name="p8589551191615"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.107567729681096%" headers="mcps1.2.11.1.9 "><p id="p1358995191616"><a name="p1358995191616"></a><a name="p1358995191616"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="11.296611016694992%" headers="mcps1.2.11.1.10 "><p id="p4441959311"><a name="p4441959311"></a><a name="p4441959311"></a>√</p>
</td>
</tr>
<tr id="row75896516165"><td class="cellrowborder" valign="top" width="20.453863840847745%" headers="mcps1.2.11.1.1 "><p id="p858985171610"><a name="p858985171610"></a><a name="p858985171610"></a>Protocol-TLS 1.0</p>
</td>
<td class="cellrowborder" valign="top" width="8.187543736878936%" headers="mcps1.2.11.1.2 "><p id="p1659055191619"><a name="p1659055191619"></a><a name="p1659055191619"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="7.807657702689194%" headers="mcps1.2.11.1.3 "><p id="p1359075115169"><a name="p1359075115169"></a><a name="p1359075115169"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.367489753074079%" headers="mcps1.2.11.1.4 "><p id="p15590105111162"><a name="p15590105111162"></a><a name="p15590105111162"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.007597720683796%" headers="mcps1.2.11.1.5 "><p id="p115491744103420"><a name="p115491744103420"></a><a name="p115491744103420"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.257522743177049%" headers="mcps1.2.11.1.6 "><p id="p1759085121619"><a name="p1759085121619"></a><a name="p1759085121619"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.617114865540339%" headers="mcps1.2.11.1.7 "><p id="p1159055116163"><a name="p1159055116163"></a><a name="p1159055116163"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.89703089073278%" headers="mcps1.2.11.1.8 "><p id="p19590551111612"><a name="p19590551111612"></a><a name="p19590551111612"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.107567729681096%" headers="mcps1.2.11.1.9 "><p id="p20590451101614"><a name="p20590451101614"></a><a name="p20590451101614"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="11.296611016694992%" headers="mcps1.2.11.1.10 "><p id="p138411518125413"><a name="p138411518125413"></a><a name="p138411518125413"></a>-</p>
</td>
</tr>
<tr id="row14590155117161"><td class="cellrowborder" colspan="10" valign="top" headers="mcps1.2.11.1.1 mcps1.2.11.1.2 mcps1.2.11.1.3 mcps1.2.11.1.4 mcps1.2.11.1.5 mcps1.2.11.1.6 mcps1.2.11.1.7 mcps1.2.11.1.8 mcps1.2.11.1.9 mcps1.2.11.1.10 "><p id="p205901351171610"><a name="p205901351171610"></a><a name="p205901351171610"></a>加密套件</p>
</td>
</tr>
<tr id="row15901351171614"><td class="cellrowborder" valign="top" width="20.453863840847745%" headers="mcps1.2.11.1.1 "><p id="p35901851111610"><a name="p35901851111610"></a><a name="p35901851111610"></a>EDHE-RSA-AES128-GCM-SHA256</p>
</td>
<td class="cellrowborder" valign="top" width="8.187543736878936%" headers="mcps1.2.11.1.2 "><p id="p759012512161"><a name="p759012512161"></a><a name="p759012512161"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="7.807657702689194%" headers="mcps1.2.11.1.3 "><p id="p959016517168"><a name="p959016517168"></a><a name="p959016517168"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.367489753074079%" headers="mcps1.2.11.1.4 "><p id="p359015191614"><a name="p359015191614"></a><a name="p359015191614"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.007597720683796%" headers="mcps1.2.11.1.5 "><p id="p3767101411349"><a name="p3767101411349"></a><a name="p3767101411349"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.257522743177049%" headers="mcps1.2.11.1.6 "><p id="p559085131610"><a name="p559085131610"></a><a name="p559085131610"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.617114865540339%" headers="mcps1.2.11.1.7 "><p id="p175903510164"><a name="p175903510164"></a><a name="p175903510164"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.89703089073278%" headers="mcps1.2.11.1.8 "><p id="p1159135110167"><a name="p1159135110167"></a><a name="p1159135110167"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.107567729681096%" headers="mcps1.2.11.1.9 "><p id="p5591165118165"><a name="p5591165118165"></a><a name="p5591165118165"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="11.296611016694992%" headers="mcps1.2.11.1.10 "><p id="p16841191815410"><a name="p16841191815410"></a><a name="p16841191815410"></a>-</p>
</td>
</tr>
<tr id="row9591165161611"><td class="cellrowborder" valign="top" width="20.453863840847745%" headers="mcps1.2.11.1.1 "><p id="p1591251161616"><a name="p1591251161616"></a><a name="p1591251161616"></a>ECDHE-RSA-AES256-GCM-SHA384</p>
</td>
<td class="cellrowborder" valign="top" width="8.187543736878936%" headers="mcps1.2.11.1.2 "><p id="p15916517169"><a name="p15916517169"></a><a name="p15916517169"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="7.807657702689194%" headers="mcps1.2.11.1.3 "><p id="p859195171613"><a name="p859195171613"></a><a name="p859195171613"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.367489753074079%" headers="mcps1.2.11.1.4 "><p id="p55911551151611"><a name="p55911551151611"></a><a name="p55911551151611"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.007597720683796%" headers="mcps1.2.11.1.5 "><p id="p1153191795214"><a name="p1153191795214"></a><a name="p1153191795214"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.257522743177049%" headers="mcps1.2.11.1.6 "><p id="p959135121615"><a name="p959135121615"></a><a name="p959135121615"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.617114865540339%" headers="mcps1.2.11.1.7 "><p id="p10591351121616"><a name="p10591351121616"></a><a name="p10591351121616"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.89703089073278%" headers="mcps1.2.11.1.8 "><p id="p95919519161"><a name="p95919519161"></a><a name="p95919519161"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.107567729681096%" headers="mcps1.2.11.1.9 "><p id="p959117510168"><a name="p959117510168"></a><a name="p959117510168"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="11.296611016694992%" headers="mcps1.2.11.1.10 "><p id="p102541942015"><a name="p102541942015"></a><a name="p102541942015"></a>√</p>
</td>
</tr>
<tr id="row459175115168"><td class="cellrowborder" valign="top" width="20.453863840847745%" headers="mcps1.2.11.1.1 "><p id="p1359165121612"><a name="p1359165121612"></a><a name="p1359165121612"></a>ECDHE-RSA-AES128-SHA256</p>
</td>
<td class="cellrowborder" valign="top" width="8.187543736878936%" headers="mcps1.2.11.1.2 "><p id="p45914513167"><a name="p45914513167"></a><a name="p45914513167"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="7.807657702689194%" headers="mcps1.2.11.1.3 "><p id="p6591851181610"><a name="p6591851181610"></a><a name="p6591851181610"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.367489753074079%" headers="mcps1.2.11.1.4 "><p id="p115911451161619"><a name="p115911451161619"></a><a name="p115911451161619"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.007597720683796%" headers="mcps1.2.11.1.5 "><p id="p4217141710521"><a name="p4217141710521"></a><a name="p4217141710521"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.257522743177049%" headers="mcps1.2.11.1.6 "><p id="p1059245111619"><a name="p1059245111619"></a><a name="p1059245111619"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.617114865540339%" headers="mcps1.2.11.1.7 "><p id="p105923519165"><a name="p105923519165"></a><a name="p105923519165"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.89703089073278%" headers="mcps1.2.11.1.8 "><p id="p175921851171613"><a name="p175921851171613"></a><a name="p175921851171613"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.107567729681096%" headers="mcps1.2.11.1.9 "><p id="p45921051101620"><a name="p45921051101620"></a><a name="p45921051101620"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="11.296611016694992%" headers="mcps1.2.11.1.10 "><p id="p14341645114"><a name="p14341645114"></a><a name="p14341645114"></a>√</p>
</td>
</tr>
<tr id="row17592751161614"><td class="cellrowborder" valign="top" width="20.453863840847745%" headers="mcps1.2.11.1.1 "><p id="p059205151616"><a name="p059205151616"></a><a name="p059205151616"></a>ECDHE-RSA-AES256-SHA384</p>
</td>
<td class="cellrowborder" valign="top" width="8.187543736878936%" headers="mcps1.2.11.1.2 "><p id="p8592145161618"><a name="p8592145161618"></a><a name="p8592145161618"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="7.807657702689194%" headers="mcps1.2.11.1.3 "><p id="p1859245101613"><a name="p1859245101613"></a><a name="p1859245101613"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.367489753074079%" headers="mcps1.2.11.1.4 "><p id="p1559216515168"><a name="p1559216515168"></a><a name="p1559216515168"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.007597720683796%" headers="mcps1.2.11.1.5 "><p id="p113711017145214"><a name="p113711017145214"></a><a name="p113711017145214"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.257522743177049%" headers="mcps1.2.11.1.6 "><p id="p115921751111618"><a name="p115921751111618"></a><a name="p115921751111618"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.617114865540339%" headers="mcps1.2.11.1.7 "><p id="p359216515165"><a name="p359216515165"></a><a name="p359216515165"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.89703089073278%" headers="mcps1.2.11.1.8 "><p id="p159213518166"><a name="p159213518166"></a><a name="p159213518166"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.107567729681096%" headers="mcps1.2.11.1.9 "><p id="p18592125141619"><a name="p18592125141619"></a><a name="p18592125141619"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="11.296611016694992%" headers="mcps1.2.11.1.10 "><p id="p11611184515"><a name="p11611184515"></a><a name="p11611184515"></a>√</p>
</td>
</tr>
<tr id="row05921251101616"><td class="cellrowborder" valign="top" width="20.453863840847745%" headers="mcps1.2.11.1.1 "><p id="p45934514164"><a name="p45934514164"></a><a name="p45934514164"></a>AES128-GCM-SHA256</p>
</td>
<td class="cellrowborder" valign="top" width="8.187543736878936%" headers="mcps1.2.11.1.2 "><p id="p13593155114164"><a name="p13593155114164"></a><a name="p13593155114164"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="7.807657702689194%" headers="mcps1.2.11.1.3 "><p id="p16593195116165"><a name="p16593195116165"></a><a name="p16593195116165"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.367489753074079%" headers="mcps1.2.11.1.4 "><p id="p1559365113168"><a name="p1559365113168"></a><a name="p1559365113168"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.007597720683796%" headers="mcps1.2.11.1.5 "><p id="p1553371755211"><a name="p1553371755211"></a><a name="p1553371755211"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.257522743177049%" headers="mcps1.2.11.1.6 "><p id="p7593205121610"><a name="p7593205121610"></a><a name="p7593205121610"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.617114865540339%" headers="mcps1.2.11.1.7 "><p id="p259375141616"><a name="p259375141616"></a><a name="p259375141616"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.89703089073278%" headers="mcps1.2.11.1.8 "><p id="p195936515161"><a name="p195936515161"></a><a name="p195936515161"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.107567729681096%" headers="mcps1.2.11.1.9 "><p id="p559355111163"><a name="p559355111163"></a><a name="p559355111163"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="11.296611016694992%" headers="mcps1.2.11.1.10 "><p id="p13775154916"><a name="p13775154916"></a><a name="p13775154916"></a>√</p>
</td>
</tr>
<tr id="row15933513167"><td class="cellrowborder" valign="top" width="20.453863840847745%" headers="mcps1.2.11.1.1 "><p id="p18593175113161"><a name="p18593175113161"></a><a name="p18593175113161"></a>AES256-GCM-SHA384</p>
</td>
<td class="cellrowborder" valign="top" width="8.187543736878936%" headers="mcps1.2.11.1.2 "><p id="p1059310511161"><a name="p1059310511161"></a><a name="p1059310511161"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="7.807657702689194%" headers="mcps1.2.11.1.3 "><p id="p45945519163"><a name="p45945519163"></a><a name="p45945519163"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.367489753074079%" headers="mcps1.2.11.1.4 "><p id="p185942516161"><a name="p185942516161"></a><a name="p185942516161"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.007597720683796%" headers="mcps1.2.11.1.5 "><p id="p36901717125216"><a name="p36901717125216"></a><a name="p36901717125216"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.257522743177049%" headers="mcps1.2.11.1.6 "><p id="p2594751171619"><a name="p2594751171619"></a><a name="p2594751171619"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.617114865540339%" headers="mcps1.2.11.1.7 "><p id="p559495119162"><a name="p559495119162"></a><a name="p559495119162"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.89703089073278%" headers="mcps1.2.11.1.8 "><p id="p55951451101610"><a name="p55951451101610"></a><a name="p55951451101610"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.107567729681096%" headers="mcps1.2.11.1.9 "><p id="p159535181619"><a name="p159535181619"></a><a name="p159535181619"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="11.296611016694992%" headers="mcps1.2.11.1.10 "><p id="p11945141118"><a name="p11945141118"></a><a name="p11945141118"></a>√</p>
</td>
</tr>
<tr id="row3595135112163"><td class="cellrowborder" valign="top" width="20.453863840847745%" headers="mcps1.2.11.1.1 "><p id="p1859505113169"><a name="p1859505113169"></a><a name="p1859505113169"></a>AES128-SHA256</p>
</td>
<td class="cellrowborder" valign="top" width="8.187543736878936%" headers="mcps1.2.11.1.2 "><p id="p35954513161"><a name="p35954513161"></a><a name="p35954513161"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="7.807657702689194%" headers="mcps1.2.11.1.3 "><p id="p105951951171611"><a name="p105951951171611"></a><a name="p105951951171611"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.367489753074079%" headers="mcps1.2.11.1.4 "><p id="p11595351111619"><a name="p11595351111619"></a><a name="p11595351111619"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.007597720683796%" headers="mcps1.2.11.1.5 "><p id="p68541417175211"><a name="p68541417175211"></a><a name="p68541417175211"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.257522743177049%" headers="mcps1.2.11.1.6 "><p id="p1259525114169"><a name="p1259525114169"></a><a name="p1259525114169"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.617114865540339%" headers="mcps1.2.11.1.7 "><p id="p14596125131612"><a name="p14596125131612"></a><a name="p14596125131612"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.89703089073278%" headers="mcps1.2.11.1.8 "><p id="p17596135114166"><a name="p17596135114166"></a><a name="p17596135114166"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.107567729681096%" headers="mcps1.2.11.1.9 "><p id="p10597751151619"><a name="p10597751151619"></a><a name="p10597751151619"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="11.296611016694992%" headers="mcps1.2.11.1.10 "><p id="p910935913"><a name="p910935913"></a><a name="p910935913"></a>√</p>
</td>
</tr>
<tr id="row5597185110163"><td class="cellrowborder" valign="top" width="20.453863840847745%" headers="mcps1.2.11.1.1 "><p id="p6597151151618"><a name="p6597151151618"></a><a name="p6597151151618"></a>AES256-SHA256</p>
</td>
<td class="cellrowborder" valign="top" width="8.187543736878936%" headers="mcps1.2.11.1.2 "><p id="p13598165119164"><a name="p13598165119164"></a><a name="p13598165119164"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="7.807657702689194%" headers="mcps1.2.11.1.3 "><p id="p459895119162"><a name="p459895119162"></a><a name="p459895119162"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.367489753074079%" headers="mcps1.2.11.1.4 "><p id="p1359816511166"><a name="p1359816511166"></a><a name="p1359816511166"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.007597720683796%" headers="mcps1.2.11.1.5 "><p id="p2018191815529"><a name="p2018191815529"></a><a name="p2018191815529"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.257522743177049%" headers="mcps1.2.11.1.6 "><p id="p9599351191614"><a name="p9599351191614"></a><a name="p9599351191614"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.617114865540339%" headers="mcps1.2.11.1.7 "><p id="p2599185181611"><a name="p2599185181611"></a><a name="p2599185181611"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.89703089073278%" headers="mcps1.2.11.1.8 "><p id="p959945111166"><a name="p959945111166"></a><a name="p959945111166"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.107567729681096%" headers="mcps1.2.11.1.9 "><p id="p75991751101617"><a name="p75991751101617"></a><a name="p75991751101617"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="11.296611016694992%" headers="mcps1.2.11.1.10 "><p id="p112711552114"><a name="p112711552114"></a><a name="p112711552114"></a>√</p>
</td>
</tr>
<tr id="row859975116161"><td class="cellrowborder" valign="top" width="20.453863840847745%" headers="mcps1.2.11.1.1 "><p id="p17600151171617"><a name="p17600151171617"></a><a name="p17600151171617"></a>ECDHE-RSA-AES128-SHA</p>
</td>
<td class="cellrowborder" valign="top" width="8.187543736878936%" headers="mcps1.2.11.1.2 "><p id="p1160095191617"><a name="p1160095191617"></a><a name="p1160095191617"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="7.807657702689194%" headers="mcps1.2.11.1.3 "><p id="p46001551141610"><a name="p46001551141610"></a><a name="p46001551141610"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.367489753074079%" headers="mcps1.2.11.1.4 "><p id="p1560011519167"><a name="p1560011519167"></a><a name="p1560011519167"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.007597720683796%" headers="mcps1.2.11.1.5 "><p id="p15182618135212"><a name="p15182618135212"></a><a name="p15182618135212"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.257522743177049%" headers="mcps1.2.11.1.6 "><p id="p17600145191613"><a name="p17600145191613"></a><a name="p17600145191613"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.617114865540339%" headers="mcps1.2.11.1.7 "><p id="p0600651121618"><a name="p0600651121618"></a><a name="p0600651121618"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.89703089073278%" headers="mcps1.2.11.1.8 "><p id="p15600155101617"><a name="p15600155101617"></a><a name="p15600155101617"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.107567729681096%" headers="mcps1.2.11.1.9 "><p id="p860015516165"><a name="p860015516165"></a><a name="p860015516165"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="11.296611016694992%" headers="mcps1.2.11.1.10 "><p id="p174314518115"><a name="p174314518115"></a><a name="p174314518115"></a>√</p>
</td>
</tr>
<tr id="row8600155191610"><td class="cellrowborder" valign="top" width="20.453863840847745%" headers="mcps1.2.11.1.1 "><p id="p160025111166"><a name="p160025111166"></a><a name="p160025111166"></a>ECDHE-RSA-AES256-SHA</p>
</td>
<td class="cellrowborder" valign="top" width="8.187543736878936%" headers="mcps1.2.11.1.2 "><p id="p760118515167"><a name="p760118515167"></a><a name="p760118515167"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="7.807657702689194%" headers="mcps1.2.11.1.3 "><p id="p060115513163"><a name="p060115513163"></a><a name="p060115513163"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.367489753074079%" headers="mcps1.2.11.1.4 "><p id="p186011851131619"><a name="p186011851131619"></a><a name="p186011851131619"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.007597720683796%" headers="mcps1.2.11.1.5 "><p id="p15350181845220"><a name="p15350181845220"></a><a name="p15350181845220"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.257522743177049%" headers="mcps1.2.11.1.6 "><p id="p18601205113166"><a name="p18601205113166"></a><a name="p18601205113166"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.617114865540339%" headers="mcps1.2.11.1.7 "><p id="p1360116517167"><a name="p1360116517167"></a><a name="p1360116517167"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.89703089073278%" headers="mcps1.2.11.1.8 "><p id="p16601195110162"><a name="p16601195110162"></a><a name="p16601195110162"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.107567729681096%" headers="mcps1.2.11.1.9 "><p id="p16601155111165"><a name="p16601155111165"></a><a name="p16601155111165"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="11.296611016694992%" headers="mcps1.2.11.1.10 "><p id="p76021252120"><a name="p76021252120"></a><a name="p76021252120"></a>√</p>
</td>
</tr>
<tr id="row4601125115169"><td class="cellrowborder" valign="top" width="20.453863840847745%" headers="mcps1.2.11.1.1 "><p id="p160111515167"><a name="p160111515167"></a><a name="p160111515167"></a>AES128-SHA</p>
</td>
<td class="cellrowborder" valign="top" width="8.187543736878936%" headers="mcps1.2.11.1.2 "><p id="p36011751131614"><a name="p36011751131614"></a><a name="p36011751131614"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="7.807657702689194%" headers="mcps1.2.11.1.3 "><p id="p060105161618"><a name="p060105161618"></a><a name="p060105161618"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.367489753074079%" headers="mcps1.2.11.1.4 "><p id="p12601145131610"><a name="p12601145131610"></a><a name="p12601145131610"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.007597720683796%" headers="mcps1.2.11.1.5 "><p id="p1051621815213"><a name="p1051621815213"></a><a name="p1051621815213"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.257522743177049%" headers="mcps1.2.11.1.6 "><p id="p860285112163"><a name="p860285112163"></a><a name="p860285112163"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.617114865540339%" headers="mcps1.2.11.1.7 "><p id="p6602951141610"><a name="p6602951141610"></a><a name="p6602951141610"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.89703089073278%" headers="mcps1.2.11.1.8 "><p id="p1160225151614"><a name="p1160225151614"></a><a name="p1160225151614"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.107567729681096%" headers="mcps1.2.11.1.9 "><p id="p9602105191613"><a name="p9602105191613"></a><a name="p9602105191613"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="11.296611016694992%" headers="mcps1.2.11.1.10 "><p id="p978235212"><a name="p978235212"></a><a name="p978235212"></a>√</p>
</td>
</tr>
<tr id="row12602135118160"><td class="cellrowborder" valign="top" width="20.453863840847745%" headers="mcps1.2.11.1.1 "><p id="p186027511162"><a name="p186027511162"></a><a name="p186027511162"></a>AES256-SHA</p>
</td>
<td class="cellrowborder" valign="top" width="8.187543736878936%" headers="mcps1.2.11.1.2 "><p id="p1602185117167"><a name="p1602185117167"></a><a name="p1602185117167"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="7.807657702689194%" headers="mcps1.2.11.1.3 "><p id="p2060245112165"><a name="p2060245112165"></a><a name="p2060245112165"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.367489753074079%" headers="mcps1.2.11.1.4 "><p id="p1960375114169"><a name="p1960375114169"></a><a name="p1960375114169"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.007597720683796%" headers="mcps1.2.11.1.5 "><p id="p667114189523"><a name="p667114189523"></a><a name="p667114189523"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.257522743177049%" headers="mcps1.2.11.1.6 "><p id="p11603145111161"><a name="p11603145111161"></a><a name="p11603145111161"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.617114865540339%" headers="mcps1.2.11.1.7 "><p id="p76034513160"><a name="p76034513160"></a><a name="p76034513160"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.89703089073278%" headers="mcps1.2.11.1.8 "><p id="p19603451161619"><a name="p19603451161619"></a><a name="p19603451161619"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.107567729681096%" headers="mcps1.2.11.1.9 "><p id="p96031951131617"><a name="p96031951131617"></a><a name="p96031951131617"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="11.296611016694992%" headers="mcps1.2.11.1.10 "><p id="p11949451013"><a name="p11949451013"></a><a name="p11949451013"></a>√</p>
</td>
</tr>
<tr id="row760317515167"><td class="cellrowborder" valign="top" width="20.453863840847745%" headers="mcps1.2.11.1.1 "><p id="p7603135111163"><a name="p7603135111163"></a><a name="p7603135111163"></a>ECDHE-ECDSA-AES128-GCM-SHA256</p>
</td>
<td class="cellrowborder" valign="top" width="8.187543736878936%" headers="mcps1.2.11.1.2 "><p id="p96031051101613"><a name="p96031051101613"></a><a name="p96031051101613"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="7.807657702689194%" headers="mcps1.2.11.1.3 "><p id="p6603195131612"><a name="p6603195131612"></a><a name="p6603195131612"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.367489753074079%" headers="mcps1.2.11.1.4 "><p id="p156032513169"><a name="p156032513169"></a><a name="p156032513169"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.007597720683796%" headers="mcps1.2.11.1.5 "><p id="p12846418185213"><a name="p12846418185213"></a><a name="p12846418185213"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.257522743177049%" headers="mcps1.2.11.1.6 "><p id="p76031151191612"><a name="p76031151191612"></a><a name="p76031151191612"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.617114865540339%" headers="mcps1.2.11.1.7 "><p id="p560411517167"><a name="p560411517167"></a><a name="p560411517167"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.89703089073278%" headers="mcps1.2.11.1.8 "><p id="p1960425114169"><a name="p1960425114169"></a><a name="p1960425114169"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.107567729681096%" headers="mcps1.2.11.1.9 "><p id="p16604135111168"><a name="p16604135111168"></a><a name="p16604135111168"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="11.296611016694992%" headers="mcps1.2.11.1.10 "><p id="p1116116319"><a name="p1116116319"></a><a name="p1116116319"></a>√</p>
</td>
</tr>
<tr id="row1160425171612"><td class="cellrowborder" valign="top" width="20.453863840847745%" headers="mcps1.2.11.1.1 "><p id="p96041151111619"><a name="p96041151111619"></a><a name="p96041151111619"></a>ECDHE-ECDSA-AES128-SHA256</p>
</td>
<td class="cellrowborder" valign="top" width="8.187543736878936%" headers="mcps1.2.11.1.2 "><p id="p26041512161"><a name="p26041512161"></a><a name="p26041512161"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="7.807657702689194%" headers="mcps1.2.11.1.3 "><p id="p0604551201618"><a name="p0604551201618"></a><a name="p0604551201618"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.367489753074079%" headers="mcps1.2.11.1.4 "><p id="p106047516168"><a name="p106047516168"></a><a name="p106047516168"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.007597720683796%" headers="mcps1.2.11.1.5 "><p id="p0115193529"><a name="p0115193529"></a><a name="p0115193529"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.257522743177049%" headers="mcps1.2.11.1.6 "><p id="p16604145131616"><a name="p16604145131616"></a><a name="p16604145131616"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.617114865540339%" headers="mcps1.2.11.1.7 "><p id="p4604105119169"><a name="p4604105119169"></a><a name="p4604105119169"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.89703089073278%" headers="mcps1.2.11.1.8 "><p id="p1360475117163"><a name="p1360475117163"></a><a name="p1360475117163"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.107567729681096%" headers="mcps1.2.11.1.9 "><p id="p196042513161"><a name="p196042513161"></a><a name="p196042513161"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="11.296611016694992%" headers="mcps1.2.11.1.10 "><p id="p192811161415"><a name="p192811161415"></a><a name="p192811161415"></a>√</p>
</td>
</tr>
<tr id="row1560413513165"><td class="cellrowborder" valign="top" width="20.453863840847745%" headers="mcps1.2.11.1.1 "><p id="p26041051161620"><a name="p26041051161620"></a><a name="p26041051161620"></a>ECDHE-ECDSA-AES128-SHA</p>
</td>
<td class="cellrowborder" valign="top" width="8.187543736878936%" headers="mcps1.2.11.1.2 "><p id="p126041051161617"><a name="p126041051161617"></a><a name="p126041051161617"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="7.807657702689194%" headers="mcps1.2.11.1.3 "><p id="p13604651161610"><a name="p13604651161610"></a><a name="p13604651161610"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.367489753074079%" headers="mcps1.2.11.1.4 "><p id="p260513510165"><a name="p260513510165"></a><a name="p260513510165"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.007597720683796%" headers="mcps1.2.11.1.5 "><p id="p817331905210"><a name="p817331905210"></a><a name="p817331905210"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.257522743177049%" headers="mcps1.2.11.1.6 "><p id="p86051951111618"><a name="p86051951111618"></a><a name="p86051951111618"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.617114865540339%" headers="mcps1.2.11.1.7 "><p id="p11605195118168"><a name="p11605195118168"></a><a name="p11605195118168"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.89703089073278%" headers="mcps1.2.11.1.8 "><p id="p4605115191617"><a name="p4605115191617"></a><a name="p4605115191617"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.107567729681096%" headers="mcps1.2.11.1.9 "><p id="p860519519162"><a name="p860519519162"></a><a name="p860519519162"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="11.296611016694992%" headers="mcps1.2.11.1.10 "><p id="p19901114414"><a name="p19901114414"></a><a name="p19901114414"></a>√</p>
</td>
</tr>
<tr id="row36052512169"><td class="cellrowborder" valign="top" width="20.453863840847745%" headers="mcps1.2.11.1.1 "><p id="p3605115113169"><a name="p3605115113169"></a><a name="p3605115113169"></a>ECDHE-ECDSA-AES256-GCM-SHA384</p>
</td>
<td class="cellrowborder" valign="top" width="8.187543736878936%" headers="mcps1.2.11.1.2 "><p id="p1560518519162"><a name="p1560518519162"></a><a name="p1560518519162"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="7.807657702689194%" headers="mcps1.2.11.1.3 "><p id="p11605185115162"><a name="p11605185115162"></a><a name="p11605185115162"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.367489753074079%" headers="mcps1.2.11.1.4 "><p id="p11605145111612"><a name="p11605145111612"></a><a name="p11605145111612"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.007597720683796%" headers="mcps1.2.11.1.5 "><p id="p18366619155216"><a name="p18366619155216"></a><a name="p18366619155216"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.257522743177049%" headers="mcps1.2.11.1.6 "><p id="p66066513164"><a name="p66066513164"></a><a name="p66066513164"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.617114865540339%" headers="mcps1.2.11.1.7 "><p id="p1660695131610"><a name="p1660695131610"></a><a name="p1660695131610"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.89703089073278%" headers="mcps1.2.11.1.8 "><p id="p106067517162"><a name="p106067517162"></a><a name="p106067517162"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.107567729681096%" headers="mcps1.2.11.1.9 "><p id="p14606551151613"><a name="p14606551151613"></a><a name="p14606551151613"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="11.296611016694992%" headers="mcps1.2.11.1.10 "><p id="p018391516113"><a name="p018391516113"></a><a name="p018391516113"></a>√</p>
</td>
</tr>
<tr id="row1160675191619"><td class="cellrowborder" valign="top" width="20.453863840847745%" headers="mcps1.2.11.1.1 "><p id="p19606251101612"><a name="p19606251101612"></a><a name="p19606251101612"></a>ECDHE-ECDSA-AES256-SHA384</p>
</td>
<td class="cellrowborder" valign="top" width="8.187543736878936%" headers="mcps1.2.11.1.2 "><p id="p46061851101617"><a name="p46061851101617"></a><a name="p46061851101617"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="7.807657702689194%" headers="mcps1.2.11.1.3 "><p id="p860613513167"><a name="p860613513167"></a><a name="p860613513167"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.367489753074079%" headers="mcps1.2.11.1.4 "><p id="p66061751111618"><a name="p66061751111618"></a><a name="p66061751111618"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.007597720683796%" headers="mcps1.2.11.1.5 "><p id="p1553781913520"><a name="p1553781913520"></a><a name="p1553781913520"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.257522743177049%" headers="mcps1.2.11.1.6 "><p id="p86061151151615"><a name="p86061151151615"></a><a name="p86061151151615"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.617114865540339%" headers="mcps1.2.11.1.7 "><p id="p1960755111612"><a name="p1960755111612"></a><a name="p1960755111612"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.89703089073278%" headers="mcps1.2.11.1.8 "><p id="p76071351101617"><a name="p76071351101617"></a><a name="p76071351101617"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.107567729681096%" headers="mcps1.2.11.1.9 "><p id="p14607175116165"><a name="p14607175116165"></a><a name="p14607175116165"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="11.296611016694992%" headers="mcps1.2.11.1.10 "><p id="p83721715110"><a name="p83721715110"></a><a name="p83721715110"></a>√</p>
</td>
</tr>
<tr id="row1960714519161"><td class="cellrowborder" valign="top" width="20.453863840847745%" headers="mcps1.2.11.1.1 "><p id="p1560715517163"><a name="p1560715517163"></a><a name="p1560715517163"></a>ECDHE-ECDSA-AES256-SHA</p>
</td>
<td class="cellrowborder" valign="top" width="8.187543736878936%" headers="mcps1.2.11.1.2 "><p id="p2060795117161"><a name="p2060795117161"></a><a name="p2060795117161"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="7.807657702689194%" headers="mcps1.2.11.1.3 "><p id="p19607151131619"><a name="p19607151131619"></a><a name="p19607151131619"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.367489753074079%" headers="mcps1.2.11.1.4 "><p id="p360765121616"><a name="p360765121616"></a><a name="p360765121616"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.007597720683796%" headers="mcps1.2.11.1.5 "><p id="p1672514199526"><a name="p1672514199526"></a><a name="p1672514199526"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.257522743177049%" headers="mcps1.2.11.1.6 "><p id="p86081251201610"><a name="p86081251201610"></a><a name="p86081251201610"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.617114865540339%" headers="mcps1.2.11.1.7 "><p id="p1960814517166"><a name="p1960814517166"></a><a name="p1960814517166"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.89703089073278%" headers="mcps1.2.11.1.8 "><p id="p196081551131610"><a name="p196081551131610"></a><a name="p196081551131610"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.107567729681096%" headers="mcps1.2.11.1.9 "><p id="p196084514166"><a name="p196084514166"></a><a name="p196084514166"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="11.296611016694992%" headers="mcps1.2.11.1.10 "><p id="p18561121517113"><a name="p18561121517113"></a><a name="p18561121517113"></a>√</p>
</td>
</tr>
<tr id="row166081551141619"><td class="cellrowborder" valign="top" width="20.453863840847745%" headers="mcps1.2.11.1.1 "><p id="p1160895111619"><a name="p1160895111619"></a><a name="p1160895111619"></a>ECDHE-RSA-AES128-GCM-SHA256</p>
</td>
<td class="cellrowborder" valign="top" width="8.187543736878936%" headers="mcps1.2.11.1.2 "><p id="p7609851131613"><a name="p7609851131613"></a><a name="p7609851131613"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="7.807657702689194%" headers="mcps1.2.11.1.3 "><p id="p106091951141616"><a name="p106091951141616"></a><a name="p106091951141616"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.367489753074079%" headers="mcps1.2.11.1.4 "><p id="p1760955118164"><a name="p1760955118164"></a><a name="p1760955118164"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.007597720683796%" headers="mcps1.2.11.1.5 "><p id="p390817194523"><a name="p390817194523"></a><a name="p390817194523"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.257522743177049%" headers="mcps1.2.11.1.6 "><p id="p360945116168"><a name="p360945116168"></a><a name="p360945116168"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.617114865540339%" headers="mcps1.2.11.1.7 "><p id="p760918512164"><a name="p760918512164"></a><a name="p760918512164"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.89703089073278%" headers="mcps1.2.11.1.8 "><p id="p2609145115168"><a name="p2609145115168"></a><a name="p2609145115168"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.107567729681096%" headers="mcps1.2.11.1.9 "><p id="p126095512167"><a name="p126095512167"></a><a name="p126095512167"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="11.296611016694992%" headers="mcps1.2.11.1.10 "><p id="p167601215016"><a name="p167601215016"></a><a name="p167601215016"></a>√</p>
</td>
</tr>
<tr id="row96091651161614"><td class="cellrowborder" valign="top" width="20.453863840847745%" headers="mcps1.2.11.1.1 "><p id="p661025117167"><a name="p661025117167"></a><a name="p661025117167"></a>TLS_AES_256_GCM_SHA384</p>
</td>
<td class="cellrowborder" valign="top" width="8.187543736878936%" headers="mcps1.2.11.1.2 "><p id="p4610145101619"><a name="p4610145101619"></a><a name="p4610145101619"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="7.807657702689194%" headers="mcps1.2.11.1.3 "><p id="p156109512163"><a name="p156109512163"></a><a name="p156109512163"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.367489753074079%" headers="mcps1.2.11.1.4 "><p id="p1161025181618"><a name="p1161025181618"></a><a name="p1161025181618"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.007597720683796%" headers="mcps1.2.11.1.5 "><p id="p1989162019528"><a name="p1989162019528"></a><a name="p1989162019528"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.257522743177049%" headers="mcps1.2.11.1.6 "><p id="p66104510162"><a name="p66104510162"></a><a name="p66104510162"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.617114865540339%" headers="mcps1.2.11.1.7 "><p id="p11610751101616"><a name="p11610751101616"></a><a name="p11610751101616"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.89703089073278%" headers="mcps1.2.11.1.8 "><p id="p1610651101615"><a name="p1610651101615"></a><a name="p1610651101615"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.107567729681096%" headers="mcps1.2.11.1.9 "><p id="p1961165119161"><a name="p1961165119161"></a><a name="p1961165119161"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="11.296611016694992%" headers="mcps1.2.11.1.10 "><p id="p12960132602"><a name="p12960132602"></a><a name="p12960132602"></a>-</p>
</td>
</tr>
<tr id="row166111651191611"><td class="cellrowborder" valign="top" width="20.453863840847745%" headers="mcps1.2.11.1.1 "><p id="p161120512169"><a name="p161120512169"></a><a name="p161120512169"></a>TLS_CHACHA20_POLY1305_SHA256</p>
</td>
<td class="cellrowborder" valign="top" width="8.187543736878936%" headers="mcps1.2.11.1.2 "><p id="p26119512163"><a name="p26119512163"></a><a name="p26119512163"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="7.807657702689194%" headers="mcps1.2.11.1.3 "><p id="p1061105119165"><a name="p1061105119165"></a><a name="p1061105119165"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.367489753074079%" headers="mcps1.2.11.1.4 "><p id="p1361125112160"><a name="p1361125112160"></a><a name="p1361125112160"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.007597720683796%" headers="mcps1.2.11.1.5 "><p id="p1525412015529"><a name="p1525412015529"></a><a name="p1525412015529"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.257522743177049%" headers="mcps1.2.11.1.6 "><p id="p12611105117166"><a name="p12611105117166"></a><a name="p12611105117166"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.617114865540339%" headers="mcps1.2.11.1.7 "><p id="p14611185110166"><a name="p14611185110166"></a><a name="p14611185110166"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.89703089073278%" headers="mcps1.2.11.1.8 "><p id="p18612115151617"><a name="p18612115151617"></a><a name="p18612115151617"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.107567729681096%" headers="mcps1.2.11.1.9 "><p id="p36121251191619"><a name="p36121251191619"></a><a name="p36121251191619"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="11.296611016694992%" headers="mcps1.2.11.1.10 "><p id="p9152133319017"><a name="p9152133319017"></a><a name="p9152133319017"></a>-</p>
</td>
</tr>
<tr id="row261245181613"><td class="cellrowborder" valign="top" width="20.453863840847745%" headers="mcps1.2.11.1.1 "><p id="p66138518169"><a name="p66138518169"></a><a name="p66138518169"></a>TLS_AES_128_GCM_SHA256</p>
</td>
<td class="cellrowborder" valign="top" width="8.187543736878936%" headers="mcps1.2.11.1.2 "><p id="p06131651161610"><a name="p06131651161610"></a><a name="p06131651161610"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="7.807657702689194%" headers="mcps1.2.11.1.3 "><p id="p1961317513161"><a name="p1961317513161"></a><a name="p1961317513161"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.367489753074079%" headers="mcps1.2.11.1.4 "><p id="p10613145121614"><a name="p10613145121614"></a><a name="p10613145121614"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.007597720683796%" headers="mcps1.2.11.1.5 "><p id="p18434172017525"><a name="p18434172017525"></a><a name="p18434172017525"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.257522743177049%" headers="mcps1.2.11.1.6 "><p id="p861455115167"><a name="p861455115167"></a><a name="p861455115167"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.617114865540339%" headers="mcps1.2.11.1.7 "><p id="p18614135151619"><a name="p18614135151619"></a><a name="p18614135151619"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.89703089073278%" headers="mcps1.2.11.1.8 "><p id="p1861475116162"><a name="p1861475116162"></a><a name="p1861475116162"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.107567729681096%" headers="mcps1.2.11.1.9 "><p id="p661495151612"><a name="p661495151612"></a><a name="p661495151612"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="11.296611016694992%" headers="mcps1.2.11.1.10 "><p id="p173365338018"><a name="p173365338018"></a><a name="p173365338018"></a>-</p>
</td>
</tr>
<tr id="row12614165111164"><td class="cellrowborder" valign="top" width="20.453863840847745%" headers="mcps1.2.11.1.1 "><p id="p0614751121613"><a name="p0614751121613"></a><a name="p0614751121613"></a>TLS_AES_128_CCM_8_SHA256</p>
</td>
<td class="cellrowborder" valign="top" width="8.187543736878936%" headers="mcps1.2.11.1.2 "><p id="p1261445151620"><a name="p1261445151620"></a><a name="p1261445151620"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="7.807657702689194%" headers="mcps1.2.11.1.3 "><p id="p116141851101616"><a name="p116141851101616"></a><a name="p116141851101616"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.367489753074079%" headers="mcps1.2.11.1.4 "><p id="p12614185151620"><a name="p12614185151620"></a><a name="p12614185151620"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.007597720683796%" headers="mcps1.2.11.1.5 "><p id="p1610132020528"><a name="p1610132020528"></a><a name="p1610132020528"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.257522743177049%" headers="mcps1.2.11.1.6 "><p id="p15614145111163"><a name="p15614145111163"></a><a name="p15614145111163"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.617114865540339%" headers="mcps1.2.11.1.7 "><p id="p10615105131617"><a name="p10615105131617"></a><a name="p10615105131617"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.89703089073278%" headers="mcps1.2.11.1.8 "><p id="p1961513515168"><a name="p1961513515168"></a><a name="p1961513515168"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.107567729681096%" headers="mcps1.2.11.1.9 "><p id="p19615185117162"><a name="p19615185117162"></a><a name="p19615185117162"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="11.296611016694992%" headers="mcps1.2.11.1.10 "><p id="p0523123315013"><a name="p0523123315013"></a><a name="p0523123315013"></a>-</p>
</td>
</tr>
<tr id="row1961555117166"><td class="cellrowborder" valign="top" width="20.453863840847745%" headers="mcps1.2.11.1.1 "><p id="p96151519160"><a name="p96151519160"></a><a name="p96151519160"></a>TLS_AES_128_CCM_SHA256</p>
</td>
<td class="cellrowborder" valign="top" width="8.187543736878936%" headers="mcps1.2.11.1.2 "><p id="p1761518510161"><a name="p1761518510161"></a><a name="p1761518510161"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="7.807657702689194%" headers="mcps1.2.11.1.3 "><p id="p861525141618"><a name="p861525141618"></a><a name="p861525141618"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.367489753074079%" headers="mcps1.2.11.1.4 "><p id="p1861525117167"><a name="p1861525117167"></a><a name="p1861525117167"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.007597720683796%" headers="mcps1.2.11.1.5 "><p id="p1579318203523"><a name="p1579318203523"></a><a name="p1579318203523"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.257522743177049%" headers="mcps1.2.11.1.6 "><p id="p10615155111616"><a name="p10615155111616"></a><a name="p10615155111616"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.617114865540339%" headers="mcps1.2.11.1.7 "><p id="p3615185161618"><a name="p3615185161618"></a><a name="p3615185161618"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.89703089073278%" headers="mcps1.2.11.1.8 "><p id="p10615651141619"><a name="p10615651141619"></a><a name="p10615651141619"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.107567729681096%" headers="mcps1.2.11.1.9 "><p id="p1861514513162"><a name="p1861514513162"></a><a name="p1861514513162"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="11.296611016694992%" headers="mcps1.2.11.1.10 "><p id="p12707133314014"><a name="p12707133314014"></a><a name="p12707133314014"></a>-</p>
</td>
</tr>
<tr id="row12560684420"><td class="cellrowborder" valign="top" width="20.453863840847745%" headers="mcps1.2.11.1.1 "><p id="p95611386422"><a name="p95611386422"></a><a name="p95611386422"></a>DHE-RSA-AES128-SHA</p>
</td>
<td class="cellrowborder" valign="top" width="8.187543736878936%" headers="mcps1.2.11.1.2 "><p id="p1956114864218"><a name="p1956114864218"></a><a name="p1956114864218"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="7.807657702689194%" headers="mcps1.2.11.1.3 "><p id="p6561118194212"><a name="p6561118194212"></a><a name="p6561118194212"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.367489753074079%" headers="mcps1.2.11.1.4 "><p id="p19561483426"><a name="p19561483426"></a><a name="p19561483426"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.007597720683796%" headers="mcps1.2.11.1.5 "><p id="p45614820428"><a name="p45614820428"></a><a name="p45614820428"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.257522743177049%" headers="mcps1.2.11.1.6 "><p id="p20561108194219"><a name="p20561108194219"></a><a name="p20561108194219"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.617114865540339%" headers="mcps1.2.11.1.7 "><p id="p1726933714216"><a name="p1726933714216"></a><a name="p1726933714216"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.89703089073278%" headers="mcps1.2.11.1.8 "><p id="p940815374429"><a name="p940815374429"></a><a name="p940815374429"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.107567729681096%" headers="mcps1.2.11.1.9 "><p id="p15533163734215"><a name="p15533163734215"></a><a name="p15533163734215"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="11.296611016694992%" headers="mcps1.2.11.1.10 "><p id="p1589310331016"><a name="p1589310331016"></a><a name="p1589310331016"></a>-</p>
</td>
</tr>
<tr id="row996801610434"><td class="cellrowborder" valign="top" width="20.453863840847745%" headers="mcps1.2.11.1.1 "><p id="p310193744314"><a name="p310193744314"></a><a name="p310193744314"></a>DHE-DSS-AES128-SHA</p>
</td>
<td class="cellrowborder" valign="top" width="8.187543736878936%" headers="mcps1.2.11.1.2 "><p id="p1950555074314"><a name="p1950555074314"></a><a name="p1950555074314"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="7.807657702689194%" headers="mcps1.2.11.1.3 "><p id="p65063506430"><a name="p65063506430"></a><a name="p65063506430"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.367489753074079%" headers="mcps1.2.11.1.4 "><p id="p050618506434"><a name="p050618506434"></a><a name="p050618506434"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.007597720683796%" headers="mcps1.2.11.1.5 "><p id="p150685011434"><a name="p150685011434"></a><a name="p150685011434"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.257522743177049%" headers="mcps1.2.11.1.6 "><p id="p950635011431"><a name="p950635011431"></a><a name="p950635011431"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.617114865540339%" headers="mcps1.2.11.1.7 "><p id="p2506250174310"><a name="p2506250174310"></a><a name="p2506250174310"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.89703089073278%" headers="mcps1.2.11.1.8 "><p id="p1150613509437"><a name="p1150613509437"></a><a name="p1150613509437"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.107567729681096%" headers="mcps1.2.11.1.9 "><p id="p6506175018432"><a name="p6506175018432"></a><a name="p6506175018432"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="11.296611016694992%" headers="mcps1.2.11.1.10 "><p id="p155920343015"><a name="p155920343015"></a><a name="p155920343015"></a>-</p>
</td>
</tr>
<tr id="row696919161431"><td class="cellrowborder" valign="top" width="20.453863840847745%" headers="mcps1.2.11.1.1 "><p id="p7102113715433"><a name="p7102113715433"></a><a name="p7102113715433"></a>CAMELLIA128-SHA</p>
</td>
<td class="cellrowborder" valign="top" width="8.187543736878936%" headers="mcps1.2.11.1.2 "><p id="p98201354174319"><a name="p98201354174319"></a><a name="p98201354174319"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="7.807657702689194%" headers="mcps1.2.11.1.3 "><p id="p582185494310"><a name="p582185494310"></a><a name="p582185494310"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.367489753074079%" headers="mcps1.2.11.1.4 "><p id="p28211454154314"><a name="p28211454154314"></a><a name="p28211454154314"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.007597720683796%" headers="mcps1.2.11.1.5 "><p id="p482125415436"><a name="p482125415436"></a><a name="p482125415436"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.257522743177049%" headers="mcps1.2.11.1.6 "><p id="p8821115412433"><a name="p8821115412433"></a><a name="p8821115412433"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.617114865540339%" headers="mcps1.2.11.1.7 "><p id="p16821145474313"><a name="p16821145474313"></a><a name="p16821145474313"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.89703089073278%" headers="mcps1.2.11.1.8 "><p id="p1282155411438"><a name="p1282155411438"></a><a name="p1282155411438"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.107567729681096%" headers="mcps1.2.11.1.9 "><p id="p118211154154312"><a name="p118211154154312"></a><a name="p118211154154312"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="11.296611016694992%" headers="mcps1.2.11.1.10 "><p id="p1923343420016"><a name="p1923343420016"></a><a name="p1923343420016"></a>-</p>
</td>
</tr>
<tr id="row1296941610434"><td class="cellrowborder" valign="top" width="20.453863840847745%" headers="mcps1.2.11.1.1 "><p id="p161021137154315"><a name="p161021137154315"></a><a name="p161021137154315"></a>EDH-RSA-DES-CBC3-SHA</p>
</td>
<td class="cellrowborder" valign="top" width="8.187543736878936%" headers="mcps1.2.11.1.2 "><p id="p341635764316"><a name="p341635764316"></a><a name="p341635764316"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="7.807657702689194%" headers="mcps1.2.11.1.3 "><p id="p19416165718435"><a name="p19416165718435"></a><a name="p19416165718435"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.367489753074079%" headers="mcps1.2.11.1.4 "><p id="p144166578433"><a name="p144166578433"></a><a name="p144166578433"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.007597720683796%" headers="mcps1.2.11.1.5 "><p id="p0416357184317"><a name="p0416357184317"></a><a name="p0416357184317"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.257522743177049%" headers="mcps1.2.11.1.6 "><p id="p341635711435"><a name="p341635711435"></a><a name="p341635711435"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.617114865540339%" headers="mcps1.2.11.1.7 "><p id="p18417135794318"><a name="p18417135794318"></a><a name="p18417135794318"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.89703089073278%" headers="mcps1.2.11.1.8 "><p id="p204171657204315"><a name="p204171657204315"></a><a name="p204171657204315"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.107567729681096%" headers="mcps1.2.11.1.9 "><p id="p1741716579436"><a name="p1741716579436"></a><a name="p1741716579436"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="11.296611016694992%" headers="mcps1.2.11.1.10 "><p id="p15410934705"><a name="p15410934705"></a><a name="p15410934705"></a>-</p>
</td>
</tr>
<tr id="row1597031614313"><td class="cellrowborder" valign="top" width="20.453863840847745%" headers="mcps1.2.11.1.1 "><p id="p16102133710432"><a name="p16102133710432"></a><a name="p16102133710432"></a>DES-CBC3-SHA</p>
</td>
<td class="cellrowborder" valign="top" width="8.187543736878936%" headers="mcps1.2.11.1.2 "><p id="p19186165919433"><a name="p19186165919433"></a><a name="p19186165919433"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="7.807657702689194%" headers="mcps1.2.11.1.3 "><p id="p818612595438"><a name="p818612595438"></a><a name="p818612595438"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.367489753074079%" headers="mcps1.2.11.1.4 "><p id="p2018618596436"><a name="p2018618596436"></a><a name="p2018618596436"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.007597720683796%" headers="mcps1.2.11.1.5 "><p id="p12186145911433"><a name="p12186145911433"></a><a name="p12186145911433"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.257522743177049%" headers="mcps1.2.11.1.6 "><p id="p7186125911433"><a name="p7186125911433"></a><a name="p7186125911433"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.617114865540339%" headers="mcps1.2.11.1.7 "><p id="p31879599439"><a name="p31879599439"></a><a name="p31879599439"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.89703089073278%" headers="mcps1.2.11.1.8 "><p id="p0187359144310"><a name="p0187359144310"></a><a name="p0187359144310"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.107567729681096%" headers="mcps1.2.11.1.9 "><p id="p7187185913436"><a name="p7187185913436"></a><a name="p7187185913436"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="11.296611016694992%" headers="mcps1.2.11.1.10 "><p id="p2584133412011"><a name="p2584133412011"></a><a name="p2584133412011"></a>-</p>
</td>
</tr>
<tr id="row4970121624311"><td class="cellrowborder" valign="top" width="20.453863840847745%" headers="mcps1.2.11.1.1 "><p id="p1410243774316"><a name="p1410243774316"></a><a name="p1410243774316"></a>ECDHE-RSA-RC4-SHA</p>
</td>
<td class="cellrowborder" valign="top" width="8.187543736878936%" headers="mcps1.2.11.1.2 "><p id="p67543044411"><a name="p67543044411"></a><a name="p67543044411"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="7.807657702689194%" headers="mcps1.2.11.1.3 "><p id="p1275440134415"><a name="p1275440134415"></a><a name="p1275440134415"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.367489753074079%" headers="mcps1.2.11.1.4 "><p id="p1175416018440"><a name="p1175416018440"></a><a name="p1175416018440"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.007597720683796%" headers="mcps1.2.11.1.5 "><p id="p12754170184420"><a name="p12754170184420"></a><a name="p12754170184420"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.257522743177049%" headers="mcps1.2.11.1.6 "><p id="p27541014444"><a name="p27541014444"></a><a name="p27541014444"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.617114865540339%" headers="mcps1.2.11.1.7 "><p id="p875412013446"><a name="p875412013446"></a><a name="p875412013446"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.89703089073278%" headers="mcps1.2.11.1.8 "><p id="p4754120144416"><a name="p4754120144416"></a><a name="p4754120144416"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.107567729681096%" headers="mcps1.2.11.1.9 "><p id="p187549004413"><a name="p187549004413"></a><a name="p187549004413"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="11.296611016694992%" headers="mcps1.2.11.1.10 "><p id="p1275514344016"><a name="p1275514344016"></a><a name="p1275514344016"></a>-</p>
</td>
</tr>
<tr id="row159701316134317"><td class="cellrowborder" valign="top" width="20.453863840847745%" headers="mcps1.2.11.1.1 "><p id="p2102143724313"><a name="p2102143724313"></a><a name="p2102143724313"></a>RC4-SHA</p>
</td>
<td class="cellrowborder" valign="top" width="8.187543736878936%" headers="mcps1.2.11.1.2 "><p id="p2128152184413"><a name="p2128152184413"></a><a name="p2128152184413"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="7.807657702689194%" headers="mcps1.2.11.1.3 "><p id="p131284204414"><a name="p131284204414"></a><a name="p131284204414"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.367489753074079%" headers="mcps1.2.11.1.4 "><p id="p2012812164414"><a name="p2012812164414"></a><a name="p2012812164414"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.007597720683796%" headers="mcps1.2.11.1.5 "><p id="p121286220446"><a name="p121286220446"></a><a name="p121286220446"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.257522743177049%" headers="mcps1.2.11.1.6 "><p id="p171291721444"><a name="p171291721444"></a><a name="p171291721444"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.617114865540339%" headers="mcps1.2.11.1.7 "><p id="p1212942134419"><a name="p1212942134419"></a><a name="p1212942134419"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.89703089073278%" headers="mcps1.2.11.1.8 "><p id="p131291024443"><a name="p131291024443"></a><a name="p131291024443"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.107567729681096%" headers="mcps1.2.11.1.9 "><p id="p1112914219446"><a name="p1112914219446"></a><a name="p1112914219446"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="11.296611016694992%" headers="mcps1.2.11.1.10 "><p id="p6926153411018"><a name="p6926153411018"></a><a name="p6926153411018"></a>-</p>
</td>
</tr>
<tr id="row148051324154317"><td class="cellrowborder" valign="top" width="20.453863840847745%" headers="mcps1.2.11.1.1 "><p id="p151021637174319"><a name="p151021637174319"></a><a name="p151021637174319"></a>DHE-RSA-AES256-SHA</p>
</td>
<td class="cellrowborder" valign="top" width="8.187543736878936%" headers="mcps1.2.11.1.2 "><p id="p1564793124417"><a name="p1564793124417"></a><a name="p1564793124417"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="7.807657702689194%" headers="mcps1.2.11.1.3 "><p id="p196471337443"><a name="p196471337443"></a><a name="p196471337443"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.367489753074079%" headers="mcps1.2.11.1.4 "><p id="p464719318446"><a name="p464719318446"></a><a name="p464719318446"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.007597720683796%" headers="mcps1.2.11.1.5 "><p id="p76473344416"><a name="p76473344416"></a><a name="p76473344416"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.257522743177049%" headers="mcps1.2.11.1.6 "><p id="p96473334416"><a name="p96473334416"></a><a name="p96473334416"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.617114865540339%" headers="mcps1.2.11.1.7 "><p id="p1164716314420"><a name="p1164716314420"></a><a name="p1164716314420"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.89703089073278%" headers="mcps1.2.11.1.8 "><p id="p964753184418"><a name="p964753184418"></a><a name="p964753184418"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.107567729681096%" headers="mcps1.2.11.1.9 "><p id="p1664716374417"><a name="p1664716374417"></a><a name="p1664716374417"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="11.296611016694992%" headers="mcps1.2.11.1.10 "><p id="p611453516017"><a name="p611453516017"></a><a name="p611453516017"></a>-</p>
</td>
</tr>
<tr id="row88051424114313"><td class="cellrowborder" valign="top" width="20.453863840847745%" headers="mcps1.2.11.1.1 "><p id="p13102153712433"><a name="p13102153712433"></a><a name="p13102153712433"></a>DHE-DSS-AES256-SHA</p>
</td>
<td class="cellrowborder" valign="top" width="8.187543736878936%" headers="mcps1.2.11.1.2 "><p id="p162615516447"><a name="p162615516447"></a><a name="p162615516447"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="7.807657702689194%" headers="mcps1.2.11.1.3 "><p id="p426195194410"><a name="p426195194410"></a><a name="p426195194410"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.367489753074079%" headers="mcps1.2.11.1.4 "><p id="p526155164415"><a name="p526155164415"></a><a name="p526155164415"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.007597720683796%" headers="mcps1.2.11.1.5 "><p id="p12261145144417"><a name="p12261145144417"></a><a name="p12261145144417"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.257522743177049%" headers="mcps1.2.11.1.6 "><p id="p02611054449"><a name="p02611054449"></a><a name="p02611054449"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.617114865540339%" headers="mcps1.2.11.1.7 "><p id="p726135144412"><a name="p726135144412"></a><a name="p726135144412"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.89703089073278%" headers="mcps1.2.11.1.8 "><p id="p15261125114417"><a name="p15261125114417"></a><a name="p15261125114417"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.107567729681096%" headers="mcps1.2.11.1.9 "><p id="p8262456444"><a name="p8262456444"></a><a name="p8262456444"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="11.296611016694992%" headers="mcps1.2.11.1.10 "><p id="p429193519017"><a name="p429193519017"></a><a name="p429193519017"></a>-</p>
</td>
</tr>
<tr id="row1480612419434"><td class="cellrowborder" valign="top" width="20.453863840847745%" headers="mcps1.2.11.1.1 "><p id="p51028378436"><a name="p51028378436"></a><a name="p51028378436"></a>DHE-RSA-CAMELLIA256-SHA</p>
</td>
<td class="cellrowborder" valign="top" width="8.187543736878936%" headers="mcps1.2.11.1.2 "><p id="p18587410194411"><a name="p18587410194411"></a><a name="p18587410194411"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="7.807657702689194%" headers="mcps1.2.11.1.3 "><p id="p11587181018445"><a name="p11587181018445"></a><a name="p11587181018445"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.367489753074079%" headers="mcps1.2.11.1.4 "><p id="p2058711103445"><a name="p2058711103445"></a><a name="p2058711103445"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.007597720683796%" headers="mcps1.2.11.1.5 "><p id="p25878106448"><a name="p25878106448"></a><a name="p25878106448"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.257522743177049%" headers="mcps1.2.11.1.6 "><p id="p6588110124419"><a name="p6588110124419"></a><a name="p6588110124419"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.617114865540339%" headers="mcps1.2.11.1.7 "><p id="p158881084417"><a name="p158881084417"></a><a name="p158881084417"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.89703089073278%" headers="mcps1.2.11.1.8 "><p id="p1458819100446"><a name="p1458819100446"></a><a name="p1458819100446"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.107567729681096%" headers="mcps1.2.11.1.9 "><p id="p1358891044420"><a name="p1358891044420"></a><a name="p1358891044420"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="11.296611016694992%" headers="mcps1.2.11.1.10 "><p id="p10479173511012"><a name="p10479173511012"></a><a name="p10479173511012"></a>-</p>
</td>
</tr>
<tr id="row139801623125720"><td class="cellrowborder" valign="top" width="20.453863840847745%" headers="mcps1.2.11.1.1 "><p id="p1574811315574"><a name="p1574811315574"></a><a name="p1574811315574"></a>ECC-SM4-SM3</p>
</td>
<td class="cellrowborder" valign="top" width="8.187543736878936%" headers="mcps1.2.11.1.2 "><p id="p18981623165712"><a name="p18981623165712"></a><a name="p18981623165712"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="7.807657702689194%" headers="mcps1.2.11.1.3 "><p id="p12248457205715"><a name="p12248457205715"></a><a name="p12248457205715"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.367489753074079%" headers="mcps1.2.11.1.4 "><p id="p164281657125714"><a name="p164281657125714"></a><a name="p164281657125714"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.007597720683796%" headers="mcps1.2.11.1.5 "><p id="p196034573577"><a name="p196034573577"></a><a name="p196034573577"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.257522743177049%" headers="mcps1.2.11.1.6 "><p id="p15793657165714"><a name="p15793657165714"></a><a name="p15793657165714"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.617114865540339%" headers="mcps1.2.11.1.7 "><p id="p1198015571571"><a name="p1198015571571"></a><a name="p1198015571571"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.89703089073278%" headers="mcps1.2.11.1.8 "><p id="p115219583574"><a name="p115219583574"></a><a name="p115219583574"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.107567729681096%" headers="mcps1.2.11.1.9 "><p id="p03301058135710"><a name="p03301058135710"></a><a name="p03301058135710"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="11.296611016694992%" headers="mcps1.2.11.1.10 "><p id="p1987524415579"><a name="p1987524415579"></a><a name="p1987524415579"></a>√</p>
</td>
</tr>
<tr id="row0978182745712"><td class="cellrowborder" valign="top" width="20.453863840847745%" headers="mcps1.2.11.1.1 "><p id="p074803110576"><a name="p074803110576"></a><a name="p074803110576"></a>ECDHE-SM4-SM3</p>
</td>
<td class="cellrowborder" valign="top" width="8.187543736878936%" headers="mcps1.2.11.1.2 "><p id="p16979162795715"><a name="p16979162795715"></a><a name="p16979162795715"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="7.807657702689194%" headers="mcps1.2.11.1.3 "><p id="p16505358195712"><a name="p16505358195712"></a><a name="p16505358195712"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.367489753074079%" headers="mcps1.2.11.1.4 "><p id="p14680155825714"><a name="p14680155825714"></a><a name="p14680155825714"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.007597720683796%" headers="mcps1.2.11.1.5 "><p id="p4866758145715"><a name="p4866758145715"></a><a name="p4866758145715"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.257522743177049%" headers="mcps1.2.11.1.6 "><p id="p43945965710"><a name="p43945965710"></a><a name="p43945965710"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.617114865540339%" headers="mcps1.2.11.1.7 "><p id="p15219185918577"><a name="p15219185918577"></a><a name="p15219185918577"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.89703089073278%" headers="mcps1.2.11.1.8 "><p id="p15389659185715"><a name="p15389659185715"></a><a name="p15389659185715"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.107567729681096%" headers="mcps1.2.11.1.9 "><p id="p256235916578"><a name="p256235916578"></a><a name="p256235916578"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="11.296611016694992%" headers="mcps1.2.11.1.10 "><p id="p166164515575"><a name="p166164515575"></a><a name="p166164515575"></a>√</p>
</td>
</tr>
</tbody>
</table>

## 创建自定义策略<a name="section9832162313111"></a>

1.  登录管理控制台。
2.  在管理控制台左上角单击![](figures/icon-region.png)图标，选择区域和项目。
3.  单击页面左上角的![](figures/icon-position.png)，选择“网络 \> 弹性负载均衡”。
4.  单击页面左边的“TLS安全策略”。
5.  在TLS安全策略页面，单击页面右上角的“创建自定义策略”。
6.  配置自定义策略参数，参数说明参见[表3](#table3263104318541)。

    **表 3**  自定义策略参数说明

    <a name="table3263104318541"></a>
    <table><thead align="left"><tr id="row6556870018541"><th class="cellrowborder" valign="top" width="18.25182518251825%" id="mcps1.2.4.1.1"><p id="p60775331862"><a name="p60775331862"></a><a name="p60775331862"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="62.04620462046204%" id="mcps1.2.4.1.2"><p id="p5449227018541"><a name="p5449227018541"></a><a name="p5449227018541"></a>说明</p>
    </th>
    <th class="cellrowborder" valign="top" width="19.7019701970197%" id="mcps1.2.4.1.3"><p id="p5179777918541"><a name="p5179777918541"></a><a name="p5179777918541"></a>样例</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row6352683318541"><td class="cellrowborder" valign="top" width="18.25182518251825%" headers="mcps1.2.4.1.1 "><p id="p4539988218541"><a name="p4539988218541"></a><a name="p4539988218541"></a>名称</p>
    </td>
    <td class="cellrowborder" valign="top" width="62.04620462046204%" headers="mcps1.2.4.1.2 "><p id="p4599141863"><a name="p4599141863"></a><a name="p4599141863"></a>自定义策略的名称。</p>
    </td>
    <td class="cellrowborder" valign="top" width="19.7019701970197%" headers="mcps1.2.4.1.3 "><p id="p1526418399126"><a name="p1526418399126"></a><a name="p1526418399126"></a>tls-test</p>
    </td>
    </tr>
    <tr id="row104691922173916"><td class="cellrowborder" valign="top" width="18.25182518251825%" headers="mcps1.2.4.1.1 "><p id="p54691222163911"><a name="p54691222163911"></a><a name="p54691222163911"></a>选择协议版本</p>
    </td>
    <td class="cellrowborder" valign="top" width="62.04620462046204%" headers="mcps1.2.4.1.2 "><p id="p154694224394"><a name="p154694224394"></a><a name="p154694224394"></a>自定义策略支持的TLS协议版本类型。支持选择多个协议版本。</p>
    <p id="p11838154971310"><a name="p11838154971310"></a><a name="p11838154971310"></a>包含：</p>
    <a name="ul13290181201519"></a><a name="ul13290181201519"></a><ul id="ul13290181201519"><li>TLS 1.0</li><li>TLS 1.1</li><li>TLS 1.2</li><li>TLS 1.3</li></ul>
    </td>
    <td class="cellrowborder" valign="top" width="19.7019701970197%" headers="mcps1.2.4.1.3 "><p id="p2469162213910"><a name="p2469162213910"></a><a name="p2469162213910"></a>-</p>
    </td>
    </tr>
    <tr id="row1987534018541"><td class="cellrowborder" valign="top" width="18.25182518251825%" headers="mcps1.2.4.1.1 "><p id="p6639869918541"><a name="p6639869918541"></a><a name="p6639869918541"></a>选择加密算法套件</p>
    </td>
    <td class="cellrowborder" valign="top" width="62.04620462046204%" headers="mcps1.2.4.1.2 "><p id="p1356618389348"><a name="p1356618389348"></a><a name="p1356618389348"></a>选择与协议版本配套的加密算法套件。支持选择多个加密算法套件。</p>
    </td>
    <td class="cellrowborder" valign="top" width="19.7019701970197%" headers="mcps1.2.4.1.3 "><p id="p3823315618541"><a name="p3823315618541"></a><a name="p3823315618541"></a>-</p>
    </td>
    </tr>
    <tr id="row11711619316"><td class="cellrowborder" valign="top" width="18.25182518251825%" headers="mcps1.2.4.1.1 "><p id="p187216203118"><a name="p187216203118"></a><a name="p187216203118"></a>描述</p>
    </td>
    <td class="cellrowborder" valign="top" width="62.04620462046204%" headers="mcps1.2.4.1.2 "><p id="p1673161317"><a name="p1673161317"></a><a name="p1673161317"></a>自定义策略相关信息的描述说明。</p>
    </td>
    <td class="cellrowborder" valign="top" width="19.7019701970197%" headers="mcps1.2.4.1.3 "><p id="p177151616319"><a name="p177151616319"></a><a name="p177151616319"></a>-</p>
    </td>
    </tr>
    </tbody>
    </table>

7.  确认参数配置，单击“确定”。

## 修改安全策略<a name="section1783252193616"></a>

修改安全策略时，后端服务器需要放通安全组，放开对ELB健康检查的限制（100.125IP的限制，UDP健康检查icmp报文的限制等），否则后端健康检查没上线，会影响业务。

1.  登录管理控制台。
2.  在管理控制台左上角单击![](figures/icon-region.png)图标，选择区域和项目。
3.  单击页面左上角的![](figures/icon-position.png)，选择“网络 \> 弹性负载均衡”。
4.  在“负载均衡器”界面，单击需要修改安全策略的监听器的负载均衡器名称。
5.  切换至“监听器”页签：
    -   独享型负载均衡器，单击需要修改安全策略的监听器名称右侧的![](figures/zh-cn_image_0000001309631721.png)按钮，选择“修改监听器”。
    -   共享型负载均衡器，单击需要修改安全策略的监听器名称右侧的![](figures/icon-edit-8.png)。

6.  在“修改监听器”界面，展开高级配置，选择安全策略参数。
7.  单击“确认”。

