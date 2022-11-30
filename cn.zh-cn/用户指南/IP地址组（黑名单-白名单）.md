# IP地址组（黑名单/白名单）<a name="elb_ug_ip_0000"></a>

## 操作场景<a name="section1143912015382"></a>

对于需要使用**黑名单**和**白名单**，在监听器上设置**[访问控制](访问控制策略.md)**的用户，开启白名单或黑名单时必须选择一个IP地址组，从而实现允许或者限制IP地址组中的IP访问负载均衡的监听器。

同一个IP地址组，最多可以关联50个监听器。目前IP地址组既支持IPv4地址又支持IPv6地址。

## 创建IP地址组<a name="section1163718452455"></a>

1.  登录管理控制台。
2.  在管理控制台左上角单击![](figures/icon-region.png)图标，选择区域和项目。
3.  单击页面左上角的![](figures/icon-position.png)，选择“网络 \> 弹性负载均衡”。
4.  在“IP地址组”界面，单击“创建IP地址组”。
5.  配置IP地址组参数，参数说明参见[表1](#table3263104318541)。

    **表 1**  IP地址组参数说明

    <a name="table3263104318541"></a>
    <table><thead align="left"><tr id="row6556870018541"><th class="cellrowborder" valign="top" width="18.23182318231823%" id="mcps1.2.4.1.1"><p id="p60775331862"><a name="p60775331862"></a><a name="p60775331862"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="48.434843484348434%" id="mcps1.2.4.1.2"><p id="p5449227018541"><a name="p5449227018541"></a><a name="p5449227018541"></a>说明</p>
    </th>
    <th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.3"><p id="p5179777918541"><a name="p5179777918541"></a><a name="p5179777918541"></a>样例</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row6352683318541"><td class="cellrowborder" valign="top" width="18.23182318231823%" headers="mcps1.2.4.1.1 "><p id="p4539988218541"><a name="p4539988218541"></a><a name="p4539988218541"></a>名称</p>
    </td>
    <td class="cellrowborder" valign="top" width="48.434843484348434%" headers="mcps1.2.4.1.2 "><p id="p4599141863"><a name="p4599141863"></a><a name="p4599141863"></a>IP地址组的名称。</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p3949107318541"><a name="p3949107318541"></a><a name="p3949107318541"></a>ipGroup-01</p>
    </td>
    </tr>
    <tr id="row104691922173916"><td class="cellrowborder" valign="top" width="18.23182318231823%" headers="mcps1.2.4.1.1 "><p id="p54691222163911"><a name="p54691222163911"></a><a name="p54691222163911"></a>企业项目</p>
    </td>
    <td class="cellrowborder" valign="top" width="48.434843484348434%" headers="mcps1.2.4.1.2 "><p id="p154694224394"><a name="p154694224394"></a><a name="p154694224394"></a>企业项目是一种云资源管理方式，企业项目管理服务提供统一的云资源按项目管理，以及项目内的资源管理、成员管理。详见<a href="https://support.huaweicloud.com/usermanual-em/em_eps_01_0000.html" target="_blank" rel="noopener noreferrer">《企业管理用户指南》</a>。</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p2469162213910"><a name="p2469162213910"></a><a name="p2469162213910"></a>-</p>
    </td>
    </tr>
    <tr id="row1987534018541"><td class="cellrowborder" valign="top" width="18.23182318231823%" headers="mcps1.2.4.1.1 "><p id="p6639869918541"><a name="p6639869918541"></a><a name="p6639869918541"></a>IP地址</p>
    </td>
    <td class="cellrowborder" valign="top" width="48.434843484348434%" headers="mcps1.2.4.1.2 "><p id="p39771091184017"><a name="p39771091184017"></a><a name="p39771091184017"></a>需要通过白名单或黑名单进行访问控制的IP地址。</p>
    <a name="ul332864552210"></a><a name="ul332864552210"></a><ul id="ul332864552210"><li>每行一个IP地址或一个网段，以回车结束；</li><li>每个IP地址或者网段都可以用“|”分隔添加备注，如“192.168.10.10丨ECS01”，备注长度范围是0到255字符，不能包含&lt;&gt;；</li><li>每个IP地址组最多可添加300个IP地址和网段。</li></ul>
    <div class="note" id="note93361548104420"><a name="note93361548104420"></a><a name="note93361548104420"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p1534024817448"><a name="p1534024817448"></a><a name="p1534024817448"></a>如果IP地址组未包含任何IP地址，当访问控制选择白名单时，则对应的负载均衡监听器禁止任何IP地址访问。</p>
    </div></div>
    </td>
    <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p53931056122017"><a name="p53931056122017"></a><a name="p53931056122017"></a>10.168.2.24</p>
    <p id="p3823315618541"><a name="p3823315618541"></a><a name="p3823315618541"></a>10.168.16.0/24</p>
    </td>
    </tr>
    <tr id="row11711619316"><td class="cellrowborder" valign="top" width="18.23182318231823%" headers="mcps1.2.4.1.1 "><p id="p187216203118"><a name="p187216203118"></a><a name="p187216203118"></a>描述</p>
    </td>
    <td class="cellrowborder" valign="top" width="48.434843484348434%" headers="mcps1.2.4.1.2 "><p id="p1673161317"><a name="p1673161317"></a><a name="p1673161317"></a>IP地址组相关信息的描述说明。</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p177151616319"><a name="p177151616319"></a><a name="p177151616319"></a>-</p>
    </td>
    </tr>
    </tbody>
    </table>

6.  确认参数配置，单击“确定”。

## 修改IP地址组<a name="section1432939104616"></a>

1.  登录管理控制台。
2.  在管理控制台左上角单击![](figures/icon-region.png)图标，选择区域和项目。
3.  单击页面左上角的![](figures/icon-position.png)，选择“网络 \> 弹性负载均衡”。
4.  在“IP地址组”界面，需要修改的IP地址组所在行，单击“修改”。
5.  修改IP地址组参数，参数说明参见[表2](#table20185132813358)。

    **表 2**  IP地址组参数说明

    <a name="table20185132813358"></a>
    <table><thead align="left"><tr id="elb_ug_ip_0000_row6556870018541"><th class="cellrowborder" valign="top" width="18.25182518251825%" id="mcps1.2.4.1.1"><p id="elb_ug_ip_0000_p60775331862"><a name="elb_ug_ip_0000_p60775331862"></a><a name="elb_ug_ip_0000_p60775331862"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="48.41484148414841%" id="mcps1.2.4.1.2"><p id="elb_ug_ip_0000_p5449227018541"><a name="elb_ug_ip_0000_p5449227018541"></a><a name="elb_ug_ip_0000_p5449227018541"></a>说明</p>
    </th>
    <th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.3"><p id="elb_ug_ip_0000_p5179777918541"><a name="elb_ug_ip_0000_p5179777918541"></a><a name="elb_ug_ip_0000_p5179777918541"></a>样例</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="elb_ug_ip_0000_row6352683318541"><td class="cellrowborder" valign="top" width="18.25182518251825%" headers="mcps1.2.4.1.1 "><p id="elb_ug_ip_0000_p4539988218541"><a name="elb_ug_ip_0000_p4539988218541"></a><a name="elb_ug_ip_0000_p4539988218541"></a>名称</p>
    </td>
    <td class="cellrowborder" valign="top" width="48.41484148414841%" headers="mcps1.2.4.1.2 "><p id="elb_ug_ip_0000_p4599141863"><a name="elb_ug_ip_0000_p4599141863"></a><a name="elb_ug_ip_0000_p4599141863"></a>IP地址组的名称。</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="elb_ug_ip_0000_p3949107318541"><a name="elb_ug_ip_0000_p3949107318541"></a><a name="elb_ug_ip_0000_p3949107318541"></a>ipGroup-01</p>
    </td>
    </tr>
    <tr id="elb_ug_ip_0000_row1987534018541"><td class="cellrowborder" valign="top" width="18.25182518251825%" headers="mcps1.2.4.1.1 "><p id="elb_ug_ip_0000_p6639869918541"><a name="elb_ug_ip_0000_p6639869918541"></a><a name="elb_ug_ip_0000_p6639869918541"></a>IP地址</p>
    </td>
    <td class="cellrowborder" valign="top" width="48.41484148414841%" headers="mcps1.2.4.1.2 "><p id="elb_ug_ip_0000_p39771091184017"><a name="elb_ug_ip_0000_p39771091184017"></a><a name="elb_ug_ip_0000_p39771091184017"></a>需要通过白名单或黑名单进行访问控制的IP地址。</p>
    <a name="elb_ug_ip_0000_ul332864552210"></a><a name="elb_ug_ip_0000_ul332864552210"></a><ul id="elb_ug_ip_0000_ul332864552210"><li>每行一个IP地址或一个网段，以回车结束；</li><li>每个IP地址或者网段都可以用“|”分隔添加备注，如“192.168.10.10丨ECS01”，备注长度范围是0到255字符，不能包含&lt;&gt;；</li><li>每个IP地址组最多可添加300个IP地址和网段。</li></ul>
    <div class="note" id="elb_ug_ip_0000_note93361548104420"><a name="elb_ug_ip_0000_note93361548104420"></a><a name="elb_ug_ip_0000_note93361548104420"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="elb_ug_ip_0000_p1534024817448"><a name="elb_ug_ip_0000_p1534024817448"></a><a name="elb_ug_ip_0000_p1534024817448"></a>如果IP地址组未包含任何IP地址，当访问控制选择白名单时，则对应的负载均衡监听器禁止任何IP地址访问。</p>
    </div></div>
    </td>
    <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="elb_ug_ip_0000_p53931056122017"><a name="elb_ug_ip_0000_p53931056122017"></a><a name="elb_ug_ip_0000_p53931056122017"></a>10.168.2.24</p>
    <p id="elb_ug_ip_0000_p3823315618541"><a name="elb_ug_ip_0000_p3823315618541"></a><a name="elb_ug_ip_0000_p3823315618541"></a>10.168.16.0/24</p>
    </td>
    </tr>
    <tr id="elb_ug_ip_0000_row11711619316"><td class="cellrowborder" valign="top" width="18.25182518251825%" headers="mcps1.2.4.1.1 "><p id="elb_ug_ip_0000_p187216203118"><a name="elb_ug_ip_0000_p187216203118"></a><a name="elb_ug_ip_0000_p187216203118"></a>描述</p>
    </td>
    <td class="cellrowborder" valign="top" width="48.41484148414841%" headers="mcps1.2.4.1.2 "><p id="elb_ug_ip_0000_p1673161317"><a name="elb_ug_ip_0000_p1673161317"></a><a name="elb_ug_ip_0000_p1673161317"></a>IP地址组相关信息的描述说明。</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="elb_ug_ip_0000_p177151616319"><a name="elb_ug_ip_0000_p177151616319"></a><a name="elb_ug_ip_0000_p177151616319"></a>-</p>
    </td>
    </tr>
    </tbody>
    </table>

6.  确认参数配置，单击“确定”。

## 删除IP地址组<a name="section1864818172465"></a>

如果IP地址组已经关联了监听器，则不允许删除。

1.  登录管理控制台。
2.  在管理控制台左上角单击![](figures/icon-region.png)图标，选择区域和项目。
3.  单击页面左上角的![](figures/icon-position.png)，选择“网络 \> 弹性负载均衡”。
4.  在“IP地址组”界面，需要删除的IP地址组所在行，单击“删除”。
5.  确认需要删除的IP地址组，单击“是”。

