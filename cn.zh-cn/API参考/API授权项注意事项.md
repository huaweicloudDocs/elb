# API授权项注意事项<a name="elb_sq_lb_0012"></a>

配额显示细粒度权限控制action为elb:quotas:list。

云日志创建、查列表、查详情、更新和删除的细粒度权限控制action为elb:logtanks:create，elb:logtanks:list，elb:logtanks:get，elb:logtanks:put和elb:logtanks:delete。

云日志使用会依赖LTS服务，请在项目（Project）级别赋予lts:\*:get\*和lts:\*:list\*权限。

弹性负载均衡的监控功能依赖云监控CES的权限。

