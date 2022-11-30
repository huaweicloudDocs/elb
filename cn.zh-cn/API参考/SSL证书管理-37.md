# SSL证书管理<a name="elb_sq_lb_0009"></a>

<a name="table1877125992216"></a>
<table><thead align="left"><tr id="row17825205902212"><th class="cellrowborder" valign="top" width="9.800000000000002%" id="mcps1.1.6.1.1"><p id="p1541914062018"><a name="p1541914062018"></a><a name="p1541914062018"></a>权限</p>
</th>
<th class="cellrowborder" valign="top" width="38.2%" id="mcps1.1.6.1.2"><p id="p14419180102011"><a name="p14419180102011"></a><a name="p14419180102011"></a>对应API接口</p>
</th>
<th class="cellrowborder" valign="top" width="16.980000000000004%" id="mcps1.1.6.1.3"><p id="p54192004206"><a name="p54192004206"></a><a name="p54192004206"></a>授权项（Action）</p>
</th>
<th class="cellrowborder" valign="top" width="14.450000000000001%" id="mcps1.1.6.1.4"><p id="p541940122019"><a name="p541940122019"></a><a name="p541940122019"></a>IAM项目（Project）</p>
</th>
<th class="cellrowborder" valign="top" width="20.570000000000004%" id="mcps1.1.6.1.5"><p id="p1598614261743"><a name="p1598614261743"></a><a name="p1598614261743"></a>企业项目（Enterprise Project）</p>
</th>
</tr>
</thead>
<tbody><tr id="row2825105916227"><td class="cellrowborder" valign="top" width="9.800000000000002%" headers="mcps1.1.6.1.1 "><p id="p5825185914224"><a name="p5825185914224"></a><a name="p5825185914224"></a>创建证书</p>
</td>
<td class="cellrowborder" valign="top" width="38.2%" headers="mcps1.1.6.1.2 "><p id="p4825159192214"><a name="p4825159192214"></a><a name="p4825159192214"></a>POST /v2/{project_id}/elb/certificates</p>
</td>
<td class="cellrowborder" valign="top" width="16.980000000000004%" headers="mcps1.1.6.1.3 "><p id="p16825165917229"><a name="p16825165917229"></a><a name="p16825165917229"></a>elb:certificates:create</p>
</td>
<td class="cellrowborder" valign="top" width="14.450000000000001%" headers="mcps1.1.6.1.4 "><p id="p15497936122214"><a name="p15497936122214"></a><a name="p15497936122214"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="20.570000000000004%" headers="mcps1.1.6.1.5 "><p id="p2507193622212"><a name="p2507193622212"></a><a name="p2507193622212"></a>√</p>
</td>
</tr>
<tr id="row16825155942211"><td class="cellrowborder" valign="top" width="9.800000000000002%" headers="mcps1.1.6.1.1 "><p id="p2082510599227"><a name="p2082510599227"></a><a name="p2082510599227"></a>查询证书</p>
</td>
<td class="cellrowborder" valign="top" width="38.2%" headers="mcps1.1.6.1.2 "><p id="p10825145910224"><a name="p10825145910224"></a><a name="p10825145910224"></a>GET /v2/{project_id}/elb/ certificates/{certificate_id}</p>
</td>
<td class="cellrowborder" valign="top" width="16.980000000000004%" headers="mcps1.1.6.1.3 "><p id="p1882545932220"><a name="p1882545932220"></a><a name="p1882545932220"></a>elb:certificates:get</p>
</td>
<td class="cellrowborder" valign="top" width="14.450000000000001%" headers="mcps1.1.6.1.4 "><p id="p175201367226"><a name="p175201367226"></a><a name="p175201367226"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="20.570000000000004%" headers="mcps1.1.6.1.5 "><p id="p052143622212"><a name="p052143622212"></a><a name="p052143622212"></a>√</p>
</td>
</tr>
<tr id="row2825195922215"><td class="cellrowborder" valign="top" width="9.800000000000002%" headers="mcps1.1.6.1.1 "><p id="p18826125911228"><a name="p18826125911228"></a><a name="p18826125911228"></a>查询证书列表</p>
</td>
<td class="cellrowborder" valign="top" width="38.2%" headers="mcps1.1.6.1.2 "><p id="p1182575913225"><a name="p1182575913225"></a><a name="p1182575913225"></a>GET /v2/{project_id}/elb/certificates</p>
</td>
<td class="cellrowborder" valign="top" width="16.980000000000004%" headers="mcps1.1.6.1.3 "><p id="p2826105962212"><a name="p2826105962212"></a><a name="p2826105962212"></a>elb:certificates:list</p>
</td>
<td class="cellrowborder" valign="top" width="14.450000000000001%" headers="mcps1.1.6.1.4 "><p id="p95221036192215"><a name="p95221036192215"></a><a name="p95221036192215"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="20.570000000000004%" headers="mcps1.1.6.1.5 "><p id="p11523636122219"><a name="p11523636122219"></a><a name="p11523636122219"></a>√</p>
</td>
</tr>
<tr id="row1682695911223"><td class="cellrowborder" valign="top" width="9.800000000000002%" headers="mcps1.1.6.1.1 "><p id="p78261859142215"><a name="p78261859142215"></a><a name="p78261859142215"></a>更新证书</p>
</td>
<td class="cellrowborder" valign="top" width="38.2%" headers="mcps1.1.6.1.2 "><p id="p4826135913222"><a name="p4826135913222"></a><a name="p4826135913222"></a>PUT /v2/{project_id}/elb/ certificates/{certificate_id}</p>
</td>
<td class="cellrowborder" valign="top" width="16.980000000000004%" headers="mcps1.1.6.1.3 "><p id="p1382610596221"><a name="p1382610596221"></a><a name="p1382610596221"></a>elb:certificates:put</p>
</td>
<td class="cellrowborder" valign="top" width="14.450000000000001%" headers="mcps1.1.6.1.4 "><p id="p65240365228"><a name="p65240365228"></a><a name="p65240365228"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="20.570000000000004%" headers="mcps1.1.6.1.5 "><p id="p155251436182214"><a name="p155251436182214"></a><a name="p155251436182214"></a>√</p>
</td>
</tr>
<tr id="row1682625918226"><td class="cellrowborder" valign="top" width="9.800000000000002%" headers="mcps1.1.6.1.1 "><p id="p782615962214"><a name="p782615962214"></a><a name="p782615962214"></a>删除证书</p>
</td>
<td class="cellrowborder" valign="top" width="38.2%" headers="mcps1.1.6.1.2 "><p id="p482675914223"><a name="p482675914223"></a><a name="p482675914223"></a>DELETE /v2/{project_id}/elb/ certificates/{certificate_id}</p>
</td>
<td class="cellrowborder" valign="top" width="16.980000000000004%" headers="mcps1.1.6.1.3 "><p id="p1282620593223"><a name="p1282620593223"></a><a name="p1282620593223"></a>elb:certificates:delete</p>
</td>
<td class="cellrowborder" valign="top" width="14.450000000000001%" headers="mcps1.1.6.1.4 "><p id="p12526336142216"><a name="p12526336142216"></a><a name="p12526336142216"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="20.570000000000004%" headers="mcps1.1.6.1.5 "><p id="p14527153618223"><a name="p14527153618223"></a><a name="p14527153618223"></a>√</p>
</td>
</tr>
</tbody>
</table>

