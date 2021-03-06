# 配置SNI<a name="elb_ug_jt_0021"></a>

## 操作场景<a name="section740719161315"></a>

如果用户的后台应用对外提供多个域名的访问，并且每个域名都使用独立的证书，则需要在创建HTTPS监听器时开启SNI功能。SNI（Server Name Indication）是为了解决一个服务器使用多个域名和证书的TLS扩展，主要解决一台服务器只能使用一个证书的缺点。开启SNI后，允许客户端在发起SSL握手请求时就提交请求的域名信息，负载均衡收到SSL请求后，会根据域名去查找证书，如果找到域名对应的证书，则返回该证书；如果没有找到域名对应的证书，则返回缺省证书。负载均衡在配置HTTPS 监听器支持此功能， 即支持绑定多个证书。

目前只有增强型负载均衡支持此功能，经典型负载均衡不支持。

## 前提条件<a name="section1392112210718"></a>

已经创建证书，具体步骤可参照[创建证书](创建证书.md)。

>![](public_sys-resources/icon-note.gif) **说明：**   
>用于SNI的证书，需要指定域名，每个证书只能指定一个域名。  

## 操作步骤<a name="section61198541679"></a>

1.  登录管理控制台。
2.  在管理控制台左上角单击![](figures/zh-cn_image_0161931717.png)图标，选择区域和项目。
3.  选择“服务列表 \> 网络 \> 弹性负载均衡”。

1.  在“负载均衡器”界面，单击负载均衡名称。
2.  切换到“监听器”页签：
    -   增强型负载均衡器，在需要添加SNI的监听器的基本信息页面，单击SNI右侧“配置”。
    -   经典型负载均衡器，在需要添加SNI的监听器所在行，单击“修改 ”。

3.  开启SNI的开关，选择需要配置的SNI证书。
4.  单击“确定”。

