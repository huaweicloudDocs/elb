# API概览<a name="elb_gl_0000"></a>

通过使用弹性负载均衡服务所提供的接口，您可以完整的使用弹性负载均衡服务的所有功能。弹性负载均衡服务所提供的接口如[表1](#table66795906)所示。

**表 1**  ELB接口说明

<a name="table66795906"></a>
<table><thead align="left"><tr id="row14670448"><th class="cellrowborder" valign="top" width="23.96%" id="mcps1.2.4.1.1"><p id="p47455645"><a name="p47455645"></a><a name="p47455645"></a><strong id="b24447627"><a name="b24447627"></a><a name="b24447627"></a>类型</strong></p>
</th>
<th class="cellrowborder" valign="top" width="16.99%" id="mcps1.2.4.1.2"><p id="p34100770"><a name="p34100770"></a><a name="p34100770"></a><strong id="b38471477"><a name="b38471477"></a><a name="b38471477"></a>子类型</strong></p>
</th>
<th class="cellrowborder" valign="top" width="59.050000000000004%" id="mcps1.2.4.1.3"><p id="p29181936"><a name="p29181936"></a><a name="p29181936"></a><strong id="b61310833"><a name="b61310833"></a><a name="b61310833"></a>说明</strong></p>
</th>
</tr>
</thead>
<tbody><tr id="row193541954112419"><td class="cellrowborder" rowspan="10" valign="top" width="23.96%" headers="mcps1.2.4.1.1 "><p id="p235417548241"><a name="p235417548241"></a><a name="p235417548241"></a>API（独享型）</p>
</td>
<td class="cellrowborder" valign="top" width="16.99%" headers="mcps1.2.4.1.2 "><p id="p2354154182414"><a name="p2354154182414"></a><a name="p2354154182414"></a>负载均衡器</p>
</td>
<td class="cellrowborder" valign="top" width="59.050000000000004%" headers="mcps1.2.4.1.3 "><p id="p14715183743520"><a name="p14715183743520"></a><a name="p14715183743520"></a>实现负载均衡器的创建、查询列表、查询详情、查询状态树、修改、删除等操作。</p>
</td>
</tr>
<tr id="row11354185412249"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p43546542241"><a name="p43546542241"></a><a name="p43546542241"></a>证书</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p3716137133513"><a name="p3716137133513"></a><a name="p3716137133513"></a>实现证书的创建、查询列表、查询详情、修改、删除等操作。</p>
</td>
</tr>
<tr id="row3355954112411"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p735575472410"><a name="p735575472410"></a><a name="p735575472410"></a>安全策略</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p89137330359"><a name="p89137330359"></a><a name="p89137330359"></a>实现安全策略的创建、查询列表、查询详情、修改、删除等操作。</p>
</td>
</tr>
<tr id="row1935565472410"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p14355195420241"><a name="p14355195420241"></a><a name="p14355195420241"></a>IP地址组</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p12913113316350"><a name="p12913113316350"></a><a name="p12913113316350"></a>实现IP地址组的创建、查询列表、查询详情、修改、删除等操作。</p>
</td>
</tr>
<tr id="row18355195420246"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p123561454132411"><a name="p123561454132411"></a><a name="p123561454132411"></a>监听器</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p1218984173519"><a name="p1218984173519"></a><a name="p1218984173519"></a>实现监听器的创建、查询列表、查询详情、修改、删除等操作。</p>
</td>
</tr>
<tr id="row253694702415"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p65373477245"><a name="p65373477245"></a><a name="p65373477245"></a>后端服务器组</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p21895413352"><a name="p21895413352"></a><a name="p21895413352"></a>实现后端服务器组的创建、查询列表、查询详情、修改、删除等操作。</p>
</td>
</tr>
<tr id="row5477154512249"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p18478645112413"><a name="p18478645112413"></a><a name="p18478645112413"></a>后端服务器</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p1595219444352"><a name="p1595219444352"></a><a name="p1595219444352"></a>实现后端服务器的创建、查询列表、查询详情、修改、删除等操作。</p>
</td>
</tr>
<tr id="row1096134310249"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p10961143152414"><a name="p10961143152414"></a><a name="p10961143152414"></a>健康检查</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p11952164413510"><a name="p11952164413510"></a><a name="p11952164413510"></a>实现健康检查的创建、查询列表、查询详情、修改、删除等操作。</p>
</td>
</tr>
<tr id="row076294015247"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p167622040202413"><a name="p167622040202413"></a><a name="p167622040202413"></a>转发策略</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p9401204712357"><a name="p9401204712357"></a><a name="p9401204712357"></a>实现安全策略的创建、查询列表、查询详情、修改、批量更新优先级、删除等操作。</p>
</td>
</tr>
<tr id="row10552173782410"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p165533376243"><a name="p165533376243"></a><a name="p165533376243"></a>转发规则</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p174011147123510"><a name="p174011147123510"></a><a name="p174011147123510"></a>实现转发规则的创建、查询列表、查询详情、修改、删除等操作。</p>
</td>
</tr>
<tr id="row71912376265"><td class="cellrowborder" rowspan="9" valign="top" width="23.96%" headers="mcps1.2.4.1.1 "><p id="p3224723192715"><a name="p3224723192715"></a><a name="p3224723192715"></a><span id="ph14224142311276"><a name="ph14224142311276"></a><a name="ph14224142311276"></a>共享型</span>ELB接口</p>
</td>
<td class="cellrowborder" valign="top" width="16.99%" headers="mcps1.2.4.1.2 "><p id="p1722511238271"><a name="p1722511238271"></a><a name="p1722511238271"></a>负载均衡器</p>
</td>
<td class="cellrowborder" valign="top" width="59.050000000000004%" headers="mcps1.2.4.1.3 "><p id="p102256237272"><a name="p102256237272"></a><a name="p102256237272"></a>实现负载均衡器创建、查询列表、查询详情、状态树查询、更新、删除等操作。</p>
</td>
</tr>
<tr id="row1190534092619"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p11225192382714"><a name="p11225192382714"></a><a name="p11225192382714"></a>监听器</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p62251232276"><a name="p62251232276"></a><a name="p62251232276"></a>实现监听器的创建、查询列表、查询详情、更新、删除等操作。</p>
</td>
</tr>
<tr id="row720613448264"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p9225152316277"><a name="p9225152316277"></a><a name="p9225152316277"></a>后端云服务器组</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p19225132315271"><a name="p19225132315271"></a><a name="p19225132315271"></a>实现后端云服务器组的创建、查询列表、查询详情、更新、删除等操作。</p>
</td>
</tr>
<tr id="row177072050162615"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p8225182315274"><a name="p8225182315274"></a><a name="p8225182315274"></a>后端云服务器</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p622562317278"><a name="p622562317278"></a><a name="p622562317278"></a>实现后端云服务器的创建、查询列表、查询详情、更新、删除等操作。</p>
</td>
</tr>
<tr id="row1570775012263"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p1022542318279"><a name="p1022542318279"></a><a name="p1022542318279"></a>健康检查</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p9225323132714"><a name="p9225323132714"></a><a name="p9225323132714"></a>实现健康检查的创建、查询列表、查询详情、更新、删除等操作。</p>
</td>
</tr>
<tr id="row1270716502267"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p15225162318272"><a name="p15225162318272"></a><a name="p15225162318272"></a>转发策略</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p18225132318279"><a name="p18225132318279"></a><a name="p18225132318279"></a>实现转发策略的创建、查询列表、查询详情、更新、删除等操作。</p>
</td>
</tr>
<tr id="row354055562620"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p1422542319277"><a name="p1422542319277"></a><a name="p1422542319277"></a>转发规则</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p10225152313275"><a name="p10225152313275"></a><a name="p10225152313275"></a>实现转发规则的创建、查询列表、查询详情、更新、删除等操作。</p>
</td>
</tr>
<tr id="row16969115992610"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p10225112312718"><a name="p10225112312718"></a><a name="p10225112312718"></a>白名单</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p202251223192710"><a name="p202251223192710"></a><a name="p202251223192710"></a>实现白名单的创建、查询列表、查询详情、更新、删除等操作。</p>
</td>
</tr>
<tr id="row1556716317273"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p122692319274"><a name="p122692319274"></a><a name="p122692319274"></a>SSL证书管理</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p722612314279"><a name="p722612314279"></a><a name="p722612314279"></a>实现证书的创建、查询列表、查询详情、更新、删除等操作。</p>
</td>
</tr>
<tr id="row121594"><td class="cellrowborder" rowspan="10" valign="top" width="23.96%" headers="mcps1.2.4.1.1 "><p id="p9849123"><a name="p9849123"></a><a name="p9849123"></a><span id="ph178014995118"><a name="ph178014995118"></a><a name="ph178014995118"></a>共享型</span>ELB OpenStack接口</p>
</td>
<td class="cellrowborder" valign="top" width="16.99%" headers="mcps1.2.4.1.2 "><p id="p59581460"><a name="p59581460"></a><a name="p59581460"></a>负载均衡器</p>
</td>
<td class="cellrowborder" valign="top" width="59.050000000000004%" headers="mcps1.2.4.1.3 "><p id="p61368950"><a name="p61368950"></a><a name="p61368950"></a>实现负载均衡器创建、查询列表、查询详情、状态树查询、更新、删除等操作。</p>
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
</tbody>
</table>

