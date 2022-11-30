# 查询后端ECS的实例ID<a name="zh-cn_topic_0000001121188819"></a>

## 操作场景<a name="zh-cn_topic_0000001079802456_section585220122402"></a>

本章节通过示例演示如何调用API来获取负载均衡器下的Member对应的ECS的ID。

## 前提条件<a name="zh-cn_topic_0000001079802456_section41561738174014"></a>

已创建负载均衡器、后端服务器组和后端服务器。

## 操作步骤<a name="zh-cn_topic_0000001079802456_section15541755144011"></a>

1.  根据Member ID 获取Member的IP和子网ID。
    1.  发送“GET https://\{elb\_endpoint\}/v3/\{project\_id\}/elb/pools/\{pool\_id\}/members/\{member\_id\}”，project\_id为项目ID，pool\_id为服务器组ID，member\_id为后端服务器。
    2.  在Request Header中增加“X-Auth-Token”。
    3.  <a name="zh-cn_topic_0000001079802456_li2711141092814"></a>查看请求响应结果，获取IP和子网ID。
        -   请求成功时，响应参数如下：

            ```
            {
                "member": {
                    "name": "My member",
                    "weight": 10,
                    "admin_state_up": false,
                    "subnet_cidr_id": "c09f620e-3492-4429-ac15-445d5dd9ca74", // 子网ID
                    "project_id": "99a3fff0d03c428eac3678da6a7d0f24",
                    "address": "120.10.10.16", // IP 地址
                    "protocol_port": 89,
                    "id": "1923923e-fe8a-484f-bdbc-e11559b1f48f",
                    "operating_status": "NO_MONITOR",
                    "ip_version": "v4"
                },
                "request_id": "45688823-45f1-40cd-9d24-e51a9574a45b"
            }
            ```

        -   请求异常时，错误码请参见  [错误码](错误码.md)。

2.  根据Member的IP地址和子网ID查询对应的VPC port信息。
    1.  发送“GET https://\{vpc\_endpoint\}/v1/\{project\_id\}/ports?fixed\_ips=ip\_address=\{ip\_address\}”，project\_id为项目ID，ip\_address为步骤[1.c](#zh-cn_topic_0000001079802456_li2711141092814)取得的IP地址。
        -   请求成功时，响应参数如下：

            ```
            {
                "ports": [
                    {
                        "id": "d00f9c13-412f-4855-8af3-de5d8c24cd60",
                        "name": "test",
                        "status": "DOWN",
                        "admin_state_up": "true",
                        "fixed_ips": [
                            {
                                "subnet_id": "70f2e74b-e660-410a-b754-0ca46744348a",
                                "ip_address": "10.128.1.10"
                            }
                        ],
                        "dns_name": "",
                        "mac_address": "fa:16:3e:d7:f2:6c",
                        "network_id": "5b808927-13c9-4e60-a4f4-ed6ffe225167",
                        "tenant_id": "43f2d1cca56a40729dcb17212482f34d",
                        "device_id": "50f2e74b-e660-410a-b754-0ca43988348a",
                        "device_owner": "ELB",
                        "security_groups": [
                            "02b4e8ee-74fa-4a31-802e-5490df11245e"
                        ],
                        "extra_dhcp_opts": [],
                        "allowed_address_pairs": [],
                        "binding:vnic_type": "normal"
                ]
            }
            ```

    2.  遍历得到的port 列表，检查每一个port中的fixed\_ips是否存在subnet\_id和步骤[1.c](#zh-cn_topic_0000001079802456_li2711141092814)取得的子网ID一致的。如果存在则表明该port是需要查找的port，该port中的device\_id即后端服务器对应的ECS ID。


