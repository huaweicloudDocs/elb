# SSL证书管理<a name="zh-cn_topic_0142009639"></a>

<a name="table1877125992216"></a>
<table><thead align="left"><tr id="row17825205902212"><th class="cellrowborder" valign="top" width="35.71357135713571%" id="mcps1.1.5.1.1"><p id="p6825559152210"><a name="p6825559152210"></a><a name="p6825559152210"></a>API</p>
</th>
<th class="cellrowborder" valign="top" width="12.241224122412241%" id="mcps1.1.5.1.2"><p id="p1282535913229"><a name="p1282535913229"></a><a name="p1282535913229"></a>API功能</p>
</th>
<th class="cellrowborder" valign="top" width="25.512551255125516%" id="mcps1.1.5.1.3"><p id="p11825165932211"><a name="p11825165932211"></a><a name="p11825165932211"></a>授权项</p>
</th>
<th class="cellrowborder" valign="top" width="26.532653265326534%" id="mcps1.1.5.1.4"><p id="p1482514590227"><a name="p1482514590227"></a><a name="p1482514590227"></a>授权项作用域</p>
</th>
</tr>
</thead>
<tbody><tr id="row2825105916227"><td class="cellrowborder" valign="top" width="35.71357135713571%" headers="mcps1.1.5.1.1 "><p id="p4825159192214"><a name="p4825159192214"></a><a name="p4825159192214"></a>POST /v2/{project_id}/elb/certificates</p>
</td>
<td class="cellrowborder" valign="top" width="12.241224122412241%" headers="mcps1.1.5.1.2 "><p id="p5825185914224"><a name="p5825185914224"></a><a name="p5825185914224"></a>创建证书</p>
</td>
<td class="cellrowborder" valign="top" width="25.512551255125516%" headers="mcps1.1.5.1.3 "><p id="p16825165917229"><a name="p16825165917229"></a><a name="p16825165917229"></a>elb:certificates:create</p>
</td>
<td class="cellrowborder" valign="top" width="26.532653265326534%" headers="mcps1.1.5.1.4 "><p id="p13825259202218"><a name="p13825259202218"></a><a name="p13825259202218"></a>支持：项目（Project）、企业项目（Enterprise Project）</p>
</td>
</tr>
<tr id="row16825155942211"><td class="cellrowborder" valign="top" width="35.71357135713571%" headers="mcps1.1.5.1.1 "><p id="p10825145910224"><a name="p10825145910224"></a><a name="p10825145910224"></a>GET /v2/{project_id}/elb/ certificates/{certificate_id}</p>
</td>
<td class="cellrowborder" valign="top" width="12.241224122412241%" headers="mcps1.1.5.1.2 "><p id="p2082510599227"><a name="p2082510599227"></a><a name="p2082510599227"></a>查询证书</p>
</td>
<td class="cellrowborder" valign="top" width="25.512551255125516%" headers="mcps1.1.5.1.3 "><p id="p1882545932220"><a name="p1882545932220"></a><a name="p1882545932220"></a>elb:certificates:get</p>
</td>
<td class="cellrowborder" valign="top" width="26.532653265326534%" headers="mcps1.1.5.1.4 "><p id="p12825115914225"><a name="p12825115914225"></a><a name="p12825115914225"></a>支持：项目（Project）、企业项目（Enterprise Project）</p>
</td>
</tr>
<tr id="row2825195922215"><td class="cellrowborder" valign="top" width="35.71357135713571%" headers="mcps1.1.5.1.1 "><p id="p1182575913225"><a name="p1182575913225"></a><a name="p1182575913225"></a>GET /v2/{project_id}/elb/certificates</p>
</td>
<td class="cellrowborder" valign="top" width="12.241224122412241%" headers="mcps1.1.5.1.2 "><p id="p18826125911228"><a name="p18826125911228"></a><a name="p18826125911228"></a>查询证书列表</p>
</td>
<td class="cellrowborder" valign="top" width="25.512551255125516%" headers="mcps1.1.5.1.3 "><p id="p2826105962212"><a name="p2826105962212"></a><a name="p2826105962212"></a>elb:certificates:list</p>
</td>
<td class="cellrowborder" valign="top" width="26.532653265326534%" headers="mcps1.1.5.1.4 "><p id="p082655962212"><a name="p082655962212"></a><a name="p082655962212"></a>支持：项目（Project）、企业项目（Enterprise Project）</p>
</td>
</tr>
<tr id="row1682695911223"><td class="cellrowborder" valign="top" width="35.71357135713571%" headers="mcps1.1.5.1.1 "><p id="p4826135913222"><a name="p4826135913222"></a><a name="p4826135913222"></a>PUT /v2/{project_id}/elb/ certificates/{certificate_id}</p>
</td>
<td class="cellrowborder" valign="top" width="12.241224122412241%" headers="mcps1.1.5.1.2 "><p id="p78261859142215"><a name="p78261859142215"></a><a name="p78261859142215"></a>更新证书</p>
</td>
<td class="cellrowborder" valign="top" width="25.512551255125516%" headers="mcps1.1.5.1.3 "><p id="p1382610596221"><a name="p1382610596221"></a><a name="p1382610596221"></a>elb:certificates:put</p>
</td>
<td class="cellrowborder" valign="top" width="26.532653265326534%" headers="mcps1.1.5.1.4 "><p id="p1182625911224"><a name="p1182625911224"></a><a name="p1182625911224"></a>支持：项目（Project）、企业项目（Enterprise Project）</p>
</td>
</tr>
<tr id="row1682625918226"><td class="cellrowborder" valign="top" width="35.71357135713571%" headers="mcps1.1.5.1.1 "><p id="p482675914223"><a name="p482675914223"></a><a name="p482675914223"></a>DELETE /v2/{project_id}/elb/ certificates/{certificate_id}</p>
</td>
<td class="cellrowborder" valign="top" width="12.241224122412241%" headers="mcps1.1.5.1.2 "><p id="p782615962214"><a name="p782615962214"></a><a name="p782615962214"></a>删除证书</p>
</td>
<td class="cellrowborder" valign="top" width="25.512551255125516%" headers="mcps1.1.5.1.3 "><p id="p1282620593223"><a name="p1282620593223"></a><a name="p1282620593223"></a>elb:certificates:delete</p>
</td>
<td class="cellrowborder" valign="top" width="26.532653265326534%" headers="mcps1.1.5.1.4 "><p id="p48261259182214"><a name="p48261259182214"></a><a name="p48261259182214"></a>支持：项目（Project）、企业项目（Enterprise Project）</p>
</td>
</tr>
</tbody>
</table>

