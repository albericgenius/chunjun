====================
Select DB Cloud Sink
====================

一、介绍
--------
Select DB Cloud Sink 支持向 SelectDB Cloud 云原生数据库中写入数据

二、支持版本
------------
Select DB Cloud 全部版本

三、插件名称
------------
.. code-block:: text

 插件类型| 插件名称
 -------+--------------------+
 Sync   | selectdbcloudwriter
 SQL    | selectdbcloud-x

四、插件参数
------------

.. list-table:: Sync
    :widths: 30, 30, 8, 24, 8
    :header-rows: 1

    * - Property name
      - Description
      - Required
      - Column type
      - Default
    * - ``host``
      - SelectDB Cloud 仓库地址
      - 是
      - String
      - 无
    * - ``httpPort``
      - SelectDB Cloud 仓库 HTTP 端口
      - 是
      - String
      - 无
    * - ``queryPort``
      - SelectDB Cloud 仓库查询端口
      - 是
      - String
      - 无
    * - ``cluster``
      - SelectDB Cloud 集群名称
      - 是
      - String
      - 无
    * - ``username``
      - SelectDB Cloud 仓库用户名
      - 是
      - String
      - 无
    * - ``password``
      - SelectDB Cloud 仓库密码
      - 是
      - String
      - 无
    * - ``table.Identifier``
      - 写入表名称，格式为：数据库名称.数据表名称
      - 是
      - String
      - 无
    * - ``column``
      - 需要写入的字段，需要说明字段名称和类型，例如："column":[{"name":"id","type":"int"}]
      - 是
      - List
      - 无
    * - ``batchSize``
      - 数据写入的批次大小
      - 否
      - int
      - 10000
    * - ``flushIntervalMills``
      - 批量写入时间间隔：单位毫秒
      - 否
      - int
      - 10000
    * - ``maxRetries``
      - 重试次数
      - 否
      - int
      - 3
    * - ``enableDelete``
      - 是否开启删除
      - 否
      - bool
      - true
    * - ``loadProperties``
      - SelectDB Cloud 写入任务的系统参数
      - 否
      - Object
      - 无

.. list-table:: SQL
    :widths: 30, 30, 8, 24, 8
    :header-rows: 1

    * - Property name
      - Description
      - Required
      - Column type
      - Default
    * - ``host``
      - SelectDB Cloud 仓库地址
      - 是
      - String
      - 无
    * - ``http-port``
      - SelectDB Cloud 仓库 HTTP 端口
      - 是
      - String
      - 无
    * - ``query-port``
      - SelectDB Cloud 仓库查询端口
      - 是
      - String
      - 无
    * - ``cluster-name``
      - SelectDB Cloud 集群名称
      - 是
      - String
      - 无
    * - ``username``
      - SelectDB Cloud 仓库用户名
      - 是
      - String
      - 无
    * - ``password``
      - SelectDB Cloud 仓库密码
      - 是
      - String
      - 无
    * - ``table.Identifier``
      - 写入表名称，格式为：数据库名称.数据表名称
      - 是
      - String
      - 无
    * - ``sink.batch-size``
      - 数据写入的批次大小
      - 否
      - int
      - 10000
    * - ``sink.batch.interval``
      - 批量写入时间间隔：单位毫秒
      - 否
      - int
      - 10000
    * - ``sink.max-retries``
      - 重试次数
      - 否
      - int
      - 3
    * - ``sink.enable-delete``
      - 是否开启删除
      - 否
      - bool
      - true
    * - ``sink.properties``
      - SelectDB Cloud 写入任务的系统参数, 例如想要配置 file.type 属性为 json，则配置 'sink.properties.file.type' = 'json'
      - 否
      - String
      - 无

五、数据类型
------------

六、脚本示例
------------

见项目内 ``chunjun-examples`` 文件夹。