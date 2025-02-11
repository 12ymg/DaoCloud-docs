# 功能总览

此处介绍服务网格支持的功能。

## 服务管理

- 服务注册与发现

    支持服务注册与发现，支持服务实例的动态注册和注销。

- VM 服务注册

    支持 VM 服务注册，支持一行命令完成 VM 服务的注册与纳管。

- 服务智能诊断

    支持根据网格服务使用最佳实践，自动检查接入网格服务的配置情况，提供一键修复和手工修复等多种策略。

## 流量治理

- 七层连接池管理

    支持配置 HTTP 最大请求数、最大重试次数、最大等待请求数、每次连接最大请求数以及连接最长空闲时间。

- 四层连接池管理

    支持配置 TCP 最大连接数、连接超时时间、最大无响应次数、最短空闲时间以及健康检查间隔。

- 离群检测

    支持配置服务离群检测规则，包括实例被驱逐前的连续错误数、检查周期、基础隔离时间以及最大隔离实例比例。

- 重试

    支持配置 HTTP 重试次数、重试超时时间以及重试条件。

- 超时

    支持配置 HTTP 请求超时时间。

- 负载均衡

    支持配置随机调度、轮询调度、最少连接和一致性哈希多种负载均衡算法。

- HTTP Header

    可以灵活添加、修改和删除指定 HTTP Header，包括将 HTTP 请求转发到目标服务之前对 Header 的操作，以及将 HTTP 响应回复给客户端前对 Header 的操作。

- 故障注入

    支持配置延时故障和中断故障。

## 安全治理

- 透明双向认证

    支持界面配置服务间的双向认证，包括对等身份认证、请求身份认证。

- 细粒度访问授权

    支持通过界面配置服务间的访问授权（后台 API 可以配置 Namespace 级别授权，授权将会给一个特定的接口）。

## 边车管理

- 边车注入

    支持通过界面配置服务的边车注入策略，支持多重维度的边车默认注入策略。

- 边车热升级

    支持边车热升级，在控制面升级后，自动检测边车版本并给出升级建议，支持无缝热升级，业务不中断。

- 边车服务发现范围

    支持通过自定义配置边车服务发现范围，根据不同业务场景，极大减少的边车资源消耗的压力。

## 可观测性

- 流量拓扑

    支持查看网格应用流量拓扑，了解服务间依赖关系。

- 服务运行监控

    支持查看服务访问信息，包括服务和服务各个版本的 QPS 和延时等指标。

- 访问日志

    支持收集和检索服务的访问日志。

- 调用链

    支持非侵入调用链埋点，并可以通过检索调用链数据进行问题定界定位。

## 多集群模式

- 多集群配置统一管理

    支持多集群网格的网格全局配置、工作集群配置管理等；支持对不同集群进行不同粒度的边车注入策略，同时支持对数据面统一管理跨集群流量策略等。

- 可扩展性

    支持一键接入、移除集群，支持接入集群时进行集群的接入检查，预防接入集群时的错误。

## 网格数据面微服务框架

- Spring Cloud

    支持 Spring Cloud SDK 开发的服务无侵入式的接入网格，并统一管理。

- Dubbo 协议

    支持 Dubbo SDK 开发的服务无侵入式的接入网格，并统一管理。

## 兼容性和扩展

- 版本兼容

    API 完全兼容通用服务网格。

- 插件支持

    支持 Tracing、Prometheus、Kiali、Grafana。
