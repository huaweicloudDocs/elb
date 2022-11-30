# 创建独享型负载均衡器并新建EIP<a name="elb_eg_0001"></a>

## 操作场景<a name="zh-cn_topic_0000001127879251_section585220122402"></a>

本章节通过示例介绍如何调用API来创建独享型负载均衡器，并同时新建与之关联的EIP。

## 前提条件<a name="zh-cn_topic_0000001127879251_section41561738174014"></a>

已创建虚拟私有云和子网。

## 操作步骤<a name="zh-cn_topic_0000001127879251_section58891233153611"></a>

1.  查询VPC子网信息。
    1.  发送“GET https://\{vpc\_endpoint\}/v1/\{project\_id\}/subnets”，project\_id为项目ID。
    2.  在Request Header中增加“X-Auth-Token”。
    3.  查看请求响应结果。
        -   请求成功时，响应参数如下：

            ```
            {
                "subnets": [
            	{
                        "id": "0535759e-8104-49d9-902c-a05185a94bdf", // 子网 ID
                        "name": "subnet-001", // 子网名称
                        "description": "",
                        "cidr": "172.16.66.0/24", // ipv4网段
                        "dnsList": [
                            "100.125.4.6"
                        ],
                        "status": "ACTIVE",
                        "vpc_id": "44789a9f-3e80-451a-ac03-0818f99b6cdd", // 所属vpc ID
                        "ipv6_enable": true,
                        "gateway_ip_v6": "2001:db8:a583:37c::1",
                        "cidr_v6": "2001:db8:a583:37c::/64",
                        "gateway_ip": "172.16.66.1",
                        "dhcp_enable": true,
                        "primary_dns": "100.125.4.6",
                        "availability_zone": "eu-de-01", // 所属可用区
                        "neutron_network_id": "0535759e-8104-49d9-902c-a05185a94bdf", // 网络ID
                        "neutron_subnet_id": "1492f0ba-cfce-4e2c-86f7-561d757dfeee", // IPv4子网ID
                        "neutron_subnet_id_v6": "3c052475-b50b-49b9-abb1-558bad45e592",
                        "extra_dhcp_opts": [
                            {
                                "opt_value": "8760h",
                                "opt_name": "addresstime"
                            }
                        ]
                    }
                ]
            }
            
            ```

        -   请求异常时，错误码请参见  [错误码](错误码.md)。

2.  创建弹性负载均衡，同时新建相关联的EIP
    1.  发送“POST https://\{elb\_endpoint\}/v3/\{project\_id\}/elb/loadbalancers”，project\_id为项目ID。
    2.  在Request Header中增加“X-Auth-Token”。
    3.  在Request Body中传入参数（包括新建EIP的参数 publicip）如下：

        ```
        {
        	"loadbalancer": {
                    "vpc_id": "e5a892ff-3c33-44ef-ada5-b713eb1f7a8b",
                    "availability_zone_list": [
                        "br-iaas-odin1a"
                    ],
                    "admin_state_up": true,
                    "vip_subnet_cidr_id": "1800b6b8-a69f-4719-813d-24d62aaf32bd",
                    "name": "elb-ipv4",
                    "publicip": {
                       "network_type": "5_bgp",
                       "bandwidth": {
                           "size": 2,
                           "share_type": "PER",
                           "charge_mode": "bandwidth",
                           "name": "elb_eip_bandwidth"
                       }
                  }
            }
        }
        
        ```

    4.  查看请求响应结果。
        -   请求成功时，响应参数如下：

            ```
            {
                "request_id": "21177eb184c52c5a4540c78dc7fdaee4",
                "loadbalancer": {
                    "id": "a2556f92-3310-4173-a6d1-0b2d0bb68478",
                    "project_id": "060576782980d5762f9ec014dd2f1148",
                    "name": "elb-ipv4",
                    "description": "",
                    "vip_port_id": "fff961a9-4514-4469-84d4-a2bc4fbdfbeb",
                    "vip_address": "192.168.0.162",
                    "admin_state_up": true,
                    "provisioning_status": "ACTIVE",
                    "operating_status": "ONLINE",
                    "listeners": [],
                    "pools": [],
                    "tags": [],
                    "provider": "vlb",
                    "created_at": "2021-02-23T08:50:19Z",
                    "updated_at": "2021-02-23T08:50:19Z",
                    "vpc_id": "e5a892ff-3c33-44ef-ada5-b713eb1f7a8b",
                    "enterprise_project_id": "0",
                    "availability_zone_list": [
                        "br-iaas-odin1a"
                    ],
                    "ipv6_vip_address": null,
                    "ipv6_vip_virsubnet_id": null,
                    "ipv6_vip_port_id": null,
                    "ipv6_bandwidth": null,
                    "publicips": [
                        {
                            "publicip_id": "12cba100-764e-476c-bf3f-8aba98782cf5",
                            "publicip_address": "10.246.173.188",
                            "ip_version": 4
                        }
                    ],
                    "elb_virsubnet_ids": [
                        "4df3e391-5ebf-4300-b614-cf5a4e793666"
                    ],
                    "elb_virsubnet_type": "dualstack",
                    "ip_target_enable": false,
                    "frozen_scene": null,
                    "eips": [
                        {
                            "eip_id": "12cba100-764e-476c-bf3f-8aba98782cf5",
                            "eip_address": "10.246.173.188",
                            "ip_version": 4
                        }
                    ],
                    "guaranteed": true,
                    "billing_info": null,
                    "l4_flavor_id": null,
                    "l4_scale_flavor_id": null,
                    "l7_flavor_id": null,
                    "l7_scale_flavor_id": null,
                    "vip_subnet_cidr_id": "1800b6b8-a69f-4719-813d-24d62aaf32bd"
                }
            }
            ```

        -   请求异常时，错误码请参见  [错误码](错误码.md)。



