# 获取ELB实例弹性公网IP<a name="zh-cn_topic_0118147668"></a>

## 操作场景<a name="section191131646081"></a>

对于需要将ELB的弹性公网IP透传到后端服务器的用户，在创建HTTPS监听器和HTTP监听器时，可以开启获取弹性公网IP开关，传输到后端服务器的报文中，HTTPS或HTTP报文头会包含ELB的弹性公网IP。

ELB的弹性公网IP会被放在HTTPS或HTTP报文头的X-Forwarded-ELB-IP字段，格式如下\(XX.XXX.XX.XXX代表ELB的弹性公网IP\)：

```
X-Forwarded-ELB-IP：XX.XXX.XX.XXX
```

## 添加获取弹性公网IP<a name="section923919121192"></a>

1.  登录管理控制台。
2.  在管理控制台左上角单击![](figures/icon-region.png)图标，选择区域和项目。
3.  单击页面左上角的![](figures/icon-position.png)，选择“网络 \> 弹性负载均衡”。
4.  在“负载均衡器”界面，单击需要创建ELB公网IP透传到后端服务器的监听器的负载均衡器名称。
5.  在该负载均衡界面的“监听器”页签，单击“添加监听器”。
6.  在“添加监听器”界面，展开高级配置，打开获取弹性公网IP开关。
7.  配置完成，单击“确定”。

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >“获取弹性公网IP”仅在创建HTTPS监听器和HTTP监听器时可配置。


## 修改获取弹性公网IP<a name="section20472544101120"></a>

1.  登录管理控制台。
2.  在管理控制台左上角单击![](figures/icon-region.png)图标，选择区域和项目。
3.  单击页面左上角的![](figures/icon-position.png)，选择“网络 \> 弹性负载均衡”。
4.  在“负载均衡器”界面，单击含有需要修改透传ELB公网IP到后端服务器的监听器的负载均衡器名称。
5.  单击需要修改透传ELB公网IP到后端开关的监听器名称右侧的![](figures/icon-edit-7.png)。
6.  在“修改监听器”界面，展开高级配置，打开或关闭获取弹性公网IP开关。
7.  确认正确，单击“确认”。

