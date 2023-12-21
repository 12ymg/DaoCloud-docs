# RabbitMQ

This page allows you to download offline packages for different versions of RabbitMQ.

## Download

| Version                                                       | Architecture | File Size | Installation Package                                                                                                               | Checksum File | Update Date |
|------------------------------------------------------------| ----- |-------- |---------------------------------------------------------------------------------------------------------------------------------| ---------- |------------|
| [v0.15.0](../../../middleware/rabbitmq/release-notes.md) | AMD 64 | 165.18 MB | [:arrow_down: rabbitmq_0.15.0_amd64.tar](https://qiniu-download-public.daocloud.io/DaoCloud_Enterprise/mcamel-rabbitmq_0.15.0_amd64.tar) | [:arrow_down: rabbitmq_0.15.0_amd64_checksum.sha512sum](https://qiniu-download-public.daocloud.io/DaoCloud_Enterprise/mcamel-rabbitmq_0.15.0_amd64_checksum.sha512sum) | 2023-12-10 |
| [v0.14.0](../../../middleware/rabbitmq/release-notes.md) | AMD 64 | 162.75 MB | [:arrow_down: rabbitmq_0.14.0_amd64.tar](https://qiniu-download-public.daocloud.io/DaoCloud_Enterprise/mcamel-rabbitmq_0.14.0_amd64.tar) | [:arrow_down: rabbitmq_0.14.0_amd64_checksum.sha512sum](https://qiniu-download-public.daocloud.io/DaoCloud_Enterprise/mcamel-rabbitmq_0.14.0_amd64_checksum.sha512sum) | 2023-11-02 |
| [v0.13.1](../../../middleware/rabbitmq/release-notes.md) | AMD 64 | 162.34 MB | [:arrow_down: rabbitmq_0.13.1_amd64.tar](https://qiniu-download-public.daocloud.io/DaoCloud_Enterprise/mcamel-rabbitmq_0.13.1_amd64.tar) | [:arrow_down: rabbitmq_0.13.1_amd64_checksum.sha512sum](https://qiniu-download-public.daocloud.io/DaoCloud_Enterprise/mcamel-rabbitmq_0.13.1_amd64_checksum.sha512sum) | 2023-10-20 |

## Validation

In the directory where you downloaded the offline package and checksum file, run the following command to validate the integrity:

```sh
echo "$(cat rabbitmq_0.13.1_amd64_checksum.sha512sum)" | sha512sum -c
```

Upon successful validation, the output will be similar to:

```none
rabbitmq_0.13.1_amd64.tar: OK
```

## Installation

If this is your first time installing, please [apply for a free trial](../../../dce/license0.md) or contact us for authorization: email info@daocloud.io or call 400 002 6898.
If you have any questions related to license keys, please contact the DaoCloud delivery team.
