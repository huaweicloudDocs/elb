# HTTP重定向至HTTPS<a name="zh-cn_topic_0118840332"></a>

## 操作场景<a name="section10243515132111"></a>

HTTPS是加密数据传输协议，安全性高，如果您需要保证业务建立安全连接，可以通过负载均衡的HTTP重定向功能，将HTTP访问重定向至HTTPS。

该功能可以满足您如下需求，PC、手机浏览器等以HTTP请求访问Web服务，配置了HTTP访问重定向至HTTPS后，后端服务器返回HTTPS的响应。默认强制以HTTPS访问网页。

>![](public_sys-resources/icon-caution.gif) **注意：** 
>-   因为HTTP标准协议只支持GET和HEAD方法的重定向，所以设置了HTTP重定向至HTTPS后，POST和其他方法会被改为GET方法，这是客户端浏览器的行为，而非ELB修改的。如果您需要实现除GET和HEAD方法以外的访问方式，建议直接使用HTTPS方式进行访问。
>-   HTTP重定向至HTTPS是指所有的HTTP请求都将转给HTTPS监听器处理为HTTPS请求，但HTTPS请求是通过HTTP被发送给后端服务器的。
>-   HTTP监听器重定向至HTTPS监听器，HTTPS监听器所关联的后端服务器上不能再安装证书，否则会引起HTTPS请求不生效。

## 前提条件<a name="section87044214500"></a>

-   已经创建HTTPS监听器
-   已经创建HTTP监听器

## 约束与限制<a name="section16564101520496"></a>

-   独享型负载均衡支持在添加HTTP监听器时添加重定向，且添加重定向后不支持修改或删除重定向，如果需要删除重定向，则需删除对应的HTTP监听器。
-   独享型负载均衡在HTTP监听器创建后不支持添加重定向。

## 添加重定向<a name="section0460104412272"></a>

1.  登录管理控制台。
2.  在管理控制台左上角单击![](figures/icon-region.png)图标，选择区域和项目。
3.  单击页面左上角的![](figures/icon-position.png)，选择“网络 \> 弹性负载均衡”。
4.  在“负载均衡器”界面，单击需要重定向的HTTP监听器的负载均衡名称。
5.  在该负载均衡界面的“监听器”页签，单击需要重定向的HTTP监听器名称。
6.  选择“重定向 \> 添加”，选择需要重定向至HTTPS监听器的名称。

    **表 1**  重定向参数配置

    <a name="table5765638104311"></a>
    <table><thead align="left"><tr id="row16766173884314"><th class="cellrowborder" valign="top" width="23.94%" id="mcps1.2.4.1.1"><p id="p16337205034318"><a name="p16337205034318"></a><a name="p16337205034318"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="42.72%" id="mcps1.2.4.1.2"><p id="p2033814509436"><a name="p2033814509436"></a><a name="p2033814509436"></a>说明</p>
    </th>
    <th class="cellrowborder" valign="top" width="33.339999999999996%" id="mcps1.2.4.1.3"><p id="p9339165064318"><a name="p9339165064318"></a><a name="p9339165064318"></a>样例</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row37661383435"><td class="cellrowborder" valign="top" width="23.94%" headers="mcps1.2.4.1.1 "><p id="p133414501436"><a name="p133414501436"></a><a name="p133414501436"></a>名称</p>
    </td>
    <td class="cellrowborder" valign="top" width="42.72%" headers="mcps1.2.4.1.2 "><p id="p73421750174316"><a name="p73421750174316"></a><a name="p73421750174316"></a>重定向的名称。</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.339999999999996%" headers="mcps1.2.4.1.3 "><p id="p143171818484"><a name="p143171818484"></a><a name="p143171818484"></a>redirect-g8h9</p>
    </td>
    </tr>
    <tr id="row9766113813431"><td class="cellrowborder" valign="top" width="23.94%" headers="mcps1.2.4.1.1 "><p id="p19345250184318"><a name="p19345250184318"></a><a name="p19345250184318"></a>重定向至</p>
    </td>
    <td class="cellrowborder" valign="top" width="42.72%" headers="mcps1.2.4.1.2 "><p id="p3347150204315"><a name="p3347150204315"></a><a name="p3347150204315"></a>选择需要重定向HTTPS监听器的名称。</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.339999999999996%" headers="mcps1.2.4.1.3 "><p id="p85582571488"><a name="p85582571488"></a><a name="p85582571488"></a>-</p>
    </td>
    </tr>
    <tr id="row1176663812438"><td class="cellrowborder" valign="top" width="23.94%" headers="mcps1.2.4.1.1 "><p id="p16350450104312"><a name="p16350450104312"></a><a name="p16350450104312"></a>描述</p>
    </td>
    <td class="cellrowborder" valign="top" width="42.72%" headers="mcps1.2.4.1.2 "><p id="p935219504434"><a name="p935219504434"></a><a name="p935219504434"></a>重定向的描述。</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.339999999999996%" headers="mcps1.2.4.1.3 "><p id="p9352155014316"><a name="p9352155014316"></a><a name="p9352155014316"></a>-</p>
    </td>
    </tr>
    </tbody>
    </table>

7.  在确认对话框单击“确定”。

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >-   HTTP监听器被重定向，除访问控制以外原有监听器配置会失效。
    >-   HTTP监听器被重定向后，会返回301返回码。


## 修改重定向<a name="section143162510568"></a>

1.  登录管理控制台。
2.  在管理控制台左上角单击![](figures/icon-region.png)图标，选择区域和项目。
3.  单击页面左上角的![](figures/icon-position.png)，选择“网络 \> 弹性负载均衡”。
4.  在“负载均衡器”界面，单击需要重定向的HTTP监听器的负载均衡名称。
5.  在该负载均衡界面的“监听器”页签，单击需要重定向的HTTP监听器名称。
6.  选择“重定向 \> 修改”，选择需要重定向至HTTPS监听器的名称。
7.  在确认对话框单击“确定”。

## 删除重定向<a name="section4978153735217"></a>

1.  登录管理控制台。
2.  在管理控制台左上角单击![](figures/icon-region.png)图标，选择区域和项目。
3.  单击页面左上角的![](figures/icon-position.png)，选择“网络 \> 弹性负载均衡”。
4.  在“负载均衡器”界面，单击已经重定向的HTTP监听器的负载均衡名称。
5.  在该负载均衡界面的“监听器”页签，单击已经重定向的HTTP监听器名称。
6.  选择“重定向 \> 删除”。
7.  在确认对话框单击“是”。

