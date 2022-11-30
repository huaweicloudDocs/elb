# 重写客户端X-Forwarded-Host<a name="elb_ug_jt_0020"></a>

重写客户端X-Forwarded-Host，即ELB将客户端请求头中的Host（主机信息）添加进X-Forwarded-Host，传输至后端服务器。

## 操作场景<a name="section1010186125812"></a>

在添加HTTPS/HTTP监听器时，重写X-Forwarded-Host默认开启。

开关开启，表示ELB以客户端请求头的Host重写X-Forwarded-Host向后端传输；开关关闭表示ELB透传客户端的X-Forwarded-Host。

目前独享型负载均衡和共享型负载均衡均默认开启此功能，独享型负载均衡支持通过**管理控制台**方式和**[调用API](https://support.huaweicloud.com/api-elb/UpdateListener.html)**的方式关闭此功能，共享型负载均衡仅支持通过**[调用API](https://support.huaweicloud.com/api-elb/elb_qy_jt_0004.html)**的方式关闭此功能。

本章节针对独享型负载均衡，介绍如何通过管理控制台方式关闭此功能。

>![](public_sys-resources/icon-note.gif) **说明：** 
>-   只有HTTPS监听器和HTTP监听器支持此功能。
>-   该功能目前所支持的区域有：华东-上海一、华北-北京四、拉美-圣地亚哥。

## 关闭重写X-Forwarded-Host<a name="section131086155812"></a>

1.  登录管理控制台。
2.  在管理控制台左上角单击![](figures/icon-region.png)图标，选择区域和项目。
3.  单击页面左上角的![](figures/icon-position.png)，选择“网络 \> 弹性负载均衡”。
4.  在“负载均衡器”界面，单击需要关闭重写X-Forwarded-Host开关的负载均衡器名称。
5.  切换到“监听器”页签，单击需要关闭重写X-Forwarded-Host开关的监听器名称右侧的![](figures/zh-cn_image_0000001170790116.png)按钮，选择“修改监听器”。
6.  单击“高级配置”，关闭重写X-Forwarded-Host开关。

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >-   也可以在添加HTTPS/HTTP监听器时，关闭重写X-Forwarded-Host功能。详见[添加HTTP监听器](添加HTTP监听器.md)和[添加HTTPS监听器](添加HTTPS监听器.md)。
    >-   如果需要开启重写X-Forwarded-Host功能，请参考上述步骤开启。


