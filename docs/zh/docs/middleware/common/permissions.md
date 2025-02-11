---
hide:
  - toc
---

# 数据中间件服务自定义角色权限说明

数据中间件服务模块允许用户自定义角色权限，用户可以在 `全局管理`中创建[自定义角色](../../ghippo/user-guide/access-control/custom-role.md)并为角色指定各中间件的权限。

创建自定义角色时可以为角色指定三种权限：创建/编辑、查看、删除。

!!! note

    部分权限选项会自动关联相关依赖权限，例如：选中`删除`权限会自动关联勾选`查看`权限，请勿取消依赖权限，避免目标权限无法正常使用。

这三种权限在数据中间件服务模块内有权执行的具体操作如下：

| 数据中间件服务          | 操作对象               | 操作         | 创建/编辑 | 查看 | 删除 |
| ------------- | ------------------ | ---------- | ----- | -- | -- |
| 配置管理          | 配置列表               | 查看列表       | ✅     | ✅  | ✅  |
|               |                    | 配置名称搜索     | ✅     | ✅  | ✅  |
|               |                    | 创建配置       | ✅     | ❌  | ❌  |
|               |                    | 更新配置       | ✅     | ❌  | ❌  |
|               |                    | 删除配置       | ❌     | ❌  | ✅  |
| MySQL         | MySQL 实例列表         | 查看列表       | ✅     | ✅  | ✅  |
|               |                    | 实例名称搜索     | ✅     | ✅  | ✅  |
|               |                    | 创建实例       | ✅     | ❌  | ❌  |
|               |                    | 更新实例配置     | ✅     | ❌  | ❌  |
|               |                    | 删除实例       | ❌     | ❌  | ✅  |
|               | MySQL 实例详情         | 实例概览       | ✅     | ✅  | ❌  |
|               |                    | 实例监控       | ✅     | ✅  | ❌  |
|               |                    | 查看实例配置参数   | ✅     | ✅  | ❌  |
|               |                    | 修改实例配置参数   | ✅     | ❌  | ❌  |
|               |                    | 查看实例访问密码   | ✅     | ✅  | ❌  |
|               |                    | 查看实例备份列表   | ✅     | ✅  | ❌  |
|               |                    | 创建实例备份     | ✅     | ❌  | ❌  |
|               |                    | 修改实例自动备份任务 | ✅     | ❌  | ❌  |
|               |                    | 使用备份创建新实例  | ✅     | ✅  | ❌  |
|               | 备份配置管理             | 备份配置列表     | ✅     | ✅  | ✅  |
|               |                    | 创建备份配置     | ✅     | ❌  | ❌  |
|               |                    | 修改备份配置     | ✅     | ❌  | ❌  |
|               |                    | 删除备份配置     | ❌     | ❌  | ✅  |
|               | 配置参数               | 查看配置参数     | ✅     | ✅  | ❌  |
|               |                    | 修改配置参数     | ✅     | ❌  | ❌  |
| RabbitMQ      | RabbitMQ 实例列表      | 查看列表       | ✅     | ✅  | ✅  |
|               |                    | 实例名称搜索     | ✅     | ✅  | ✅  |
|               |                    | 创建实例       | ✅     | ❌  | ❌  |
|               |                    | 更新实例配置     | ✅     | ❌  | ❌  |
|               |                    | 删除实例       | ❌     | ❌  | ✅  |
|               | RabbitMQ 实例详情      | 实例概览       | ✅     | ✅  | ❌  |
|               |                    | 实例监控       | ✅     | ✅  | ❌  |
|               |                    | 查看实例配置参数   | ✅     | ✅  | ❌  |
|               |                    | 修改实例配置参数   | ✅     | ❌  | ❌  |
|               |                    | 查看实例访问密码   | ✅     | ✅  | ❌  |
| Elasticsearch | Elasticsearch 实例列表 | 查看列表       | ✅     | ✅  | ✅  |
|               |                    | 实例名称搜索     | ✅     | ✅  | ✅  |
|               |                    | 创建实例       | ✅     | ❌  | ❌  |
|               |                    | 更新实例配置     | ✅     | ❌  | ❌  |
|               |                    | 删除实例       | ❌     | ❌  | ✅  |
|               | Elasticsearch 实例详情 | 实例概览       | ✅     | ✅  | ❌  |
|               |                    | 实例监控       | ✅     | ✅  | ❌  |
|               |                    | 查看实例配置参数   | ✅     | ✅  | ❌  |
|               |                    | 修改实例配置参数   | ✅     | ❌  | ❌  |
|               |                    | 查看实例访问密码   | ❌     | ✅  | ❌  |
| Redis         | Redis 实例列表         | 查看列表       | ✅     | ✅  | ✅  |
|               |                    | 实例名称搜索     | ✅     | ✅  | ✅  |
|               |                    | 创建实例       | ✅     | ❌  | ❌  |
|               |                    | 更新实例配置     | ✅     | ❌  | ❌  |
|               |                    | 删除实例       | ❌     | ❌  | ✅  |
|               | Redis 实例详情         | 实例概览       | ✅     | ✅  | ❌  |
|               |                    | 实例监控       | ✅     | ✅  | ❌  |
|               |                    | 查看实例配置参数   | ✅     | ✅  | ❌  |
|               |                    | 修改实例配置参数   | ✅     | ❌  | ❌  |
|               |                    | 查看实例访问密码   | ✅     | ✅  | ❌  |
|               |                    | 创建实例备份     | ✅     | ❌  | ❌  |
|               |                    | 修改实例自动备份任务 | ✅     | ❌  | ❌  |
|               |                    | 使用备份创建新实例  | ✅     | ✅  | ❌  |
|               | 备份配置管理             | 备份配置列表     | ✅     | ✅  | ✅  |
|               |                    | 创建备份配置     | ✅     | ❌  | ❌  |
|               |                    | 修改备份配置     | ✅     | ❌  | ❌  |
|               |                    | 删除备份配置     | ❌     | ❌  | ✅  |
|               | 配置参数               | 查看配置参数     | ✅     | ✅  | ❌  |
|               |                    | 修改配置参数     | ✅     |    | ❌  |
| Kafka         | Kafka 实例列表         | 查看列表       | ✅     | ✅  | ✅  |
|               |                    | 实例名称搜索     | ✅     | ✅  | ✅  |
|               |                    | 创建实例       | ✅     | ❌  | ❌  |
|               |                    | 更新实例配置     | ✅     | ❌  | ❌  |
|               |                    | 删除实例       | ❌     | ❌  | ✅  |
|               | Kafka 实例详情         | 实例概览       | ✅     | ✅  | ❌  |
|               |                    | 实例监控       | ✅     | ✅  | ❌  |
|               |                    | 查看实例配置参数   | ✅     | ✅  | ❌  |
|               |                    | 修改实例配置参数   | ✅     | ❌  | ❌  |
|               |                    | 查看实例访问密码   | ✅     | ✅  | ❌  |
|               | 配置参数               | 查看配置参数     | ✅     | ✅  | ❌  |
|               |                    | 修改配置参数     | ✅     | ❌  | ❌  |
| MinIO         | MinIO 实例列表         | 查看列表       | ✅     | ✅  | ✅  |
|               |                    | 实例名称搜索     | ✅     | ✅  | ✅  |
|               |                    | 创建实例       | ✅     | ❌  | ❌  |
|               |                    | 更新实例配置     | ✅     | ❌  | ❌  |
|               |                    | 删除实例       | ❌     | ❌  | ✅  |
|               | MinIO 实例详情         | 实例概览       | ✅     | ✅  | ❌  |
|               |                    | 实例监控       | ✅     | ✅  | ❌  |
|               |                    | 查看实例配置参数   | ✅     | ✅  | ❌  |
|               |                    | 修改实例配置参数   | ✅     | ❌  | ❌  |
|               |                    | 查看实例访问密码   | ✅     | ✅  | ❌  |
|               | 配置参数               | 查看配置参数     | ✅     | ✅  | ❌  |
|               |                    | 修改配置参数     | ✅     | ❌  | ❌  |
| PostgreSQL    | PostgreSQL 实例列表    | 查看列表       | ✅     | ✅  | ✅  |
|               |                    | 实例名称搜索     | ✅     | ✅  | ✅  |
|               |                    | 创建实例       | ✅     | ❌  | ❌  |
|               |                    | 更新实例配置     | ✅     | ❌  | ❌  |
|               |                    | 删除实例       | ❌     | ❌  | ✅  |
|               | PostgreSQL 实例详情    | 实例概览       | ✅     | ✅  | ❌  |
|               |                    | 实例监控       | ✅     | ✅  | ❌  |
|               |                    | 查看实例配置参数   | ✅     | ✅  | ❌  |
|               |                    | 修改实例配置参数   | ✅     | ❌  | ❌  |
|               |                    | 查看实例访问密码   | ✅     | ✅  | ❌  |
|               | 配置参数               | 查看配置参数     | ✅     | ✅  | ❌  |
|               |                    | 修改配置参数     | ✅     | ❌  | ❌  |
| MongoDB    | MongoDB 实例列表    | 查看列表       | ✅     | ✅  | ✅  |
|               |                    | 实例名称搜索     | ✅     | ✅  | ✅  |
|               |                    | 创建实例       | ✅     | ❌  | ❌  |
|               |                    | 更新实例配置     | ✅     | ❌  | ❌  |
|               |                    | 删除实例       | ❌     | ❌  | ✅  |
|               | MongoDB 实例详情    | 实例概览       | ✅     | ✅  | ❌  |
|               |                    | 实例监控       | ✅     | ✅  | ❌  |
|               |                    | 查看实例配置参数   | ✅     | ✅  | ❌  |
|               |                    | 修改实例配置参数   | ✅     | ❌  | ❌  |
|               |                    | 查看实例访问密码   | ✅     | ✅  | ❌  |
| RocketMQ    | RocketMQ 实例列表    | 查看列表       | ✅     | ✅  | ✅  |
|               |                    | 实例名称搜索     | ✅     | ✅  | ✅  |
|               |                    | 创建实例       | ✅     | ❌  | ❌  |
|               |                    | 更新实例配置     | ✅     | ❌  | ❌  |
|               |                    | 删除实例       | ❌     | ❌  | ✅  |
|               | RocketMQ 实例详情    | 实例概览       | ✅     | ✅  | ❌  |
|               |                    | 实例监控       | ✅     | ✅  | ❌  |
|               |                    | 查看实例配置参数   | ✅     | ✅  | ❌  |
|               |                    | 修改实例配置参数   | ✅     | ❌  | ❌  |
|               |                    | 查看实例访问密码   | ✅     | ✅  | ❌  |
