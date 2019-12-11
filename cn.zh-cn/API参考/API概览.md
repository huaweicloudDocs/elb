# API概览<a name="zh-cn_topic_0132467675"></a>

通过使用弹性负载均衡服务所提供的接口，您可以完整的使用弹性负载均衡服务的所有功能。弹性负载均衡服务所提供的接口如[表1](#table66795906)所示。

**表 1**  ELB接口说明

<a name="table66795906"></a>
<table><thead align="left"><tr id="row14670448"><th class="cellrowborder" valign="top" width="14.000000000000002%" id="mcps1.2.4.1.1"><p id="p47455645"><a name="p47455645"></a><a name="p47455645"></a><strong id="b24447627"><a name="b24447627"></a><a name="b24447627"></a>类型</strong></p>
</th>
<th class="cellrowborder" valign="top" width="15%" id="mcps1.2.4.1.2"><p id="p34100770"><a name="p34100770"></a><a name="p34100770"></a><strong id="b38471477"><a name="b38471477"></a><a name="b38471477"></a>子类型</strong></p>
</th>
<th class="cellrowborder" valign="top" width="71%" id="mcps1.2.4.1.3"><p id="p29181936"><a name="p29181936"></a><a name="p29181936"></a><strong id="b61310833"><a name="b61310833"></a><a name="b61310833"></a>说明</strong></p>
</th>
</tr>
</thead>
<tbody><tr id="row17264416143517"><td class="cellrowborder" rowspan="8" valign="top" width="14.000000000000002%" headers="mcps1.2.4.1.1 "><p id="p42641816123511"><a name="p42641816123511"></a><a name="p42641816123511"></a>经典型ELB接口</p>
<p id="p18848135214356"><a name="p18848135214356"></a><a name="p18848135214356"></a></p>
<p id="p6826165518353"><a name="p6826165518353"></a><a name="p6826165518353"></a></p>
<p id="p1358085810359"><a name="p1358085810359"></a><a name="p1358085810359"></a></p>
<p id="p11418739365"><a name="p11418739365"></a><a name="p11418739365"></a></p>
<p id="p1665324993516"><a name="p1665324993516"></a><a name="p1665324993516"></a></p>
</td>
<td class="cellrowborder" valign="top" width="15%" headers="mcps1.2.4.1.2 "><p id="p3159181817364"><a name="p3159181817364"></a><a name="p3159181817364"></a>弹性负载均衡</p>
</td>
<td class="cellrowborder" valign="top" width="71%" headers="mcps1.2.4.1.3 "><p id="p14164618193620"><a name="p14164618193620"></a><a name="p14164618193620"></a>实现负载均衡器创建、查询列表、查询详情、修改、删除等操作。</p>
</td>
</tr>
<tr id="row1848852103515"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p12422141716"><a name="p12422141716"></a><a name="p12422141716"></a>监听器</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p10147174618615"><a name="p10147174618615"></a><a name="p10147174618615"></a>实现监听器创建、查询列表、查询详情、修改、删除等操作。</p>
</td>
</tr>
<tr id="row1482695515355"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p63322091210"><a name="p63322091210"></a><a name="p63322091210"></a>健康检查</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p1228534716613"><a name="p1228534716613"></a><a name="p1228534716613"></a>实现健康检查的创建、查询详情、修改、删除等操作。</p>
</td>
</tr>
<tr id="row25801958173516"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p1562120416212"><a name="p1562120416212"></a><a name="p1562120416212"></a>后端云服务器</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p963314481167"><a name="p963314481167"></a><a name="p963314481167"></a>实现后端云服务器添加、查询列表、移除等操作。</p>
</td>
</tr>
<tr id="row9417134360"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p822251716218"><a name="p822251716218"></a><a name="p822251716218"></a>配额</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p1475317493619"><a name="p1475317493619"></a><a name="p1475317493619"></a>实现经典型资源的配额查询操作。</p>
</td>
</tr>
<tr id="row61244611417"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p2991410641"><a name="p2991410641"></a><a name="p2991410641"></a>证书管理</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p1099191019410"><a name="p1099191019410"></a><a name="p1099191019410"></a>实现证书的创建、查询列表、修改、删除等操作。</p>
</td>
</tr>
<tr id="row16761421746"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p1767742645"><a name="p1767742645"></a><a name="p1767742645"></a>查询job状态</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p116775214419"><a name="p116775214419"></a><a name="p116775214419"></a>实现查询job状态。</p>
</td>
</tr>
<tr id="row5652549103518"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p120419397420"><a name="p120419397420"></a><a name="p120419397420"></a>查询负载均衡的监控指标</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p6898350964"><a name="p6898350964"></a><a name="p6898350964"></a>实现查询负载均衡的监控指标。</p>
</td>
</tr>
<tr id="row121594"><td class="cellrowborder" rowspan="10" valign="top" width="14.000000000000002%" headers="mcps1.2.4.1.1 "><p id="p9849123"><a name="p9849123"></a><a name="p9849123"></a>增强型ELB接口</p>
</td>
<td class="cellrowborder" valign="top" width="15%" headers="mcps1.2.4.1.2 "><p id="p59581460"><a name="p59581460"></a><a name="p59581460"></a>负载均衡器</p>
</td>
<td class="cellrowborder" valign="top" width="71%" headers="mcps1.2.4.1.3 "><p id="p61368950"><a name="p61368950"></a><a name="p61368950"></a>实现负载均衡器创建、查询列表、查询详情、状态树查询、更新、删除等操作。</p>
</td>
</tr>
<tr id="row15449640"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p43461366"><a name="p43461366"></a><a name="p43461366"></a>监听器</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p30709768"><a name="p30709768"></a><a name="p30709768"></a>实现监听器的创建、查询列表、查询详情、更新、删除等操作。</p>
</td>
</tr>
<tr id="row7952463"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p40169730"><a name="p40169730"></a><a name="p40169730"></a>后端云服务器组</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p32522735"><a name="p32522735"></a><a name="p32522735"></a>实现后端云服务器组的创建、查询列表、查询详情、更新、删除等操作。</p>
</td>
</tr>
<tr id="row24269162"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p19645086"><a name="p19645086"></a><a name="p19645086"></a>后端云服务器</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p47748127"><a name="p47748127"></a><a name="p47748127"></a>实现后端云服务器的创建、查询列表、查询详情、更新、删除等操作。</p>
</td>
</tr>
<tr id="row27079959"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p45993077"><a name="p45993077"></a><a name="p45993077"></a>健康检查</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p34451796"><a name="p34451796"></a><a name="p34451796"></a>实现健康检查的创建、查询列表、查询详情、更新、删除等操作。</p>
</td>
</tr>
<tr id="row41630716"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p16644798"><a name="p16644798"></a><a name="p16644798"></a>转发策略</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p6051413"><a name="p6051413"></a><a name="p6051413"></a>实现转发策略的创建、查询列表、查询详情、更新、删除等操作。</p>
</td>
</tr>
<tr id="row54462724"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p49404533"><a name="p49404533"></a><a name="p49404533"></a>转发规则</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p42344238"><a name="p42344238"></a><a name="p42344238"></a>实现转发规则的创建、查询列表、查询详情、更新、删除等操作。</p>
</td>
</tr>
<tr id="row75268206276"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p1152752032720"><a name="p1152752032720"></a><a name="p1152752032720"></a>白名单</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p18527162010275"><a name="p18527162010275"></a><a name="p18527162010275"></a>实现白名单的创建、查询列表、查询详情、更新、删除等操作。</p>
</td>
</tr>
<tr id="row45553830"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p65981599"><a name="p65981599"></a><a name="p65981599"></a>SSL证书管理</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p42909301"><a name="p42909301"></a><a name="p42909301"></a>实现证书的创建、查询列表、查询详情、更新、删除等操作。</p>
</td>
</tr>
<tr id="row50639390"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p8149897"><a name="p8149897"></a><a name="p8149897"></a>标签管理</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p56161925"><a name="p56161925"></a><a name="p56161925"></a>实现负载均衡器和监听器的标签的创建、批量创建、查询、删除、批量删除等操作。</p>
</td>
</tr>
<tr id="row10301192902811"><td class="cellrowborder" rowspan="9" valign="top" width="14.000000000000002%" headers="mcps1.2.4.1.1 "><p id="p10918423193020"><a name="p10918423193020"></a><a name="p10918423193020"></a>增强型企业项目接口</p>
</td>
<td class="cellrowborder" valign="top" width="15%" headers="mcps1.2.4.1.2 "><p id="p10301132962812"><a name="p10301132962812"></a><a name="p10301132962812"></a>负载均衡器</p>
</td>
<td class="cellrowborder" valign="top" width="71%" headers="mcps1.2.4.1.3 "><p id="p425585120309"><a name="p425585120309"></a><a name="p425585120309"></a>实现负载均衡器创建、查询列表、查询详情、状态树查询、更新、删除等操作。</p>
</td>
</tr>
<tr id="row132371533152814"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p2238233142810"><a name="p2238233142810"></a><a name="p2238233142810"></a>监听器</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p825575173010"><a name="p825575173010"></a><a name="p825575173010"></a>实现监听器的创建、查询列表、查询详情、更新、删除等操作。</p>
</td>
</tr>
<tr id="row191031536142816"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p610313622815"><a name="p610313622815"></a><a name="p610313622815"></a>后端云服务器组</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p1125565114307"><a name="p1125565114307"></a><a name="p1125565114307"></a>实现后端云服务器组的创建、查询列表、查询详情、更新、删除等操作。</p>
</td>
</tr>
<tr id="row1645175952818"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p3461859152819"><a name="p3461859152819"></a><a name="p3461859152819"></a>后端云服务器</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p2255205133012"><a name="p2255205133012"></a><a name="p2255205133012"></a>实现后端云服务器的创建、查询列表、查询详情、更新、删除等操作。</p>
</td>
</tr>
<tr id="row1635112016298"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p53526082910"><a name="p53526082910"></a><a name="p53526082910"></a>健康检查</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p1125535117301"><a name="p1125535117301"></a><a name="p1125535117301"></a>实现健康检查的创建、查询列表、查询详情、更新、删除等操作。</p>
</td>
</tr>
<tr id="row2447328296"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p13448192112911"><a name="p13448192112911"></a><a name="p13448192112911"></a>转发策略</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p16256151173010"><a name="p16256151173010"></a><a name="p16256151173010"></a>实现转发策略的创建、查询列表、查询详情、更新、删除等操作。</p>
</td>
</tr>
<tr id="row1213176152920"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p101327662917"><a name="p101327662917"></a><a name="p101327662917"></a>转发规则</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p525619516305"><a name="p525619516305"></a><a name="p525619516305"></a>实现转发规则的创建、查询列表、查询详情、更新、删除等操作。</p>
</td>
</tr>
<tr id="row19235115013296"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p12236185018294"><a name="p12236185018294"></a><a name="p12236185018294"></a>白名单</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p5256125110303"><a name="p5256125110303"></a><a name="p5256125110303"></a>实现白名单的创建、查询列表、查询详情、更新、删除等操作。</p>
</td>
</tr>
<tr id="row15133125432917"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p141314715301"><a name="p141314715301"></a><a name="p141314715301"></a>SSL证书管理</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p1425655113302"><a name="p1425655113302"></a><a name="p1425655113302"></a>实现证书的创建、查询列表、查询详情、更新、删除等操作。</p>
<p id="p20256175118300"><a name="p20256175118300"></a><a name="p20256175118300"></a>实现负载均衡器和监听器的标签的创建、批量创建、查询、删除、批量删除等操作。</p>
</td>
</tr>
</tbody>
</table>

