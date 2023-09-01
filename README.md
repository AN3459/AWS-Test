
## 计算
---
**AWS Batch**
- 概念：AWS Batch可以运行任何规模的批处理任务


---
**AWS EC2**
- 概念：AWS Batch可以运行任何规模的批处理任务
- 存储：
  + 对操作系统和数据分别使用单独的EBS卷，可以确保数据在实例终止后保留
  + 
- Amazon Machine Images (AMI)：
  + 一个AMI可以包含一个或者多个EBS快照，EBS快照是快照的组成部分之一，比如AMI中可以包含操作系统的EBS，也可以包含应用程序的EBS，通过该AMI创建出来的EC2实例就会包含这些内容
  + AMI可以在同一个AWS中复制，也可以复制到其他AWS区域
  + AMI生命周期![ami_lifecycle](https://github.com/AN3459/AWS-Test/assets/77662211/94f86e9d-4423-4757-b065-074542c52ec1)
  + 注销某个AMI之后，就无法用该AMI创建新的实例，但是已经用该AMI创建的实例不受影响
  + AMI分为两种，一种是Amazon EBS-backed AMI，从这个AMI启动的实例的根设备时从EBS快照创建出来的EBS卷，这种实例的启动时间通常不到1分钟，根设备的大小限制为64TiB
  + 另一种是Amazon 实例存储支持的 AMI，从这种AMI创建出来的根设备是存储在S3中的一个模板创建出来的实例存储卷
| 特征 | Amazon EBS-backed AMI | 由 Amazon 实例存储支持的 AMI |
| ------- | ------- | ------- |
| 实例的启动时间 | 通常不到 1 分钟 |通常不到 5 分钟 |
| 单元格3 | 单元格4 |

## 分析
---
**Amazon Athena**
- 概念：Athena是一种交互式的查询服务，可以用标准sql语句直接分析s3中的数据
- 收费：
  + Athena中的sql和Spark是无服务的，无需维护基础设施，只需为查询收费
- 考点：
  + 可以使用Apache Spark运行数据分析
  + Athena可以自动扩展
  + 可以分析非结构化、半结构化和结构化的数据，包括CSV，JSON或列式数据格式
  + 运行查询时无需将数据加载到Athena中


---
**AWS Data Pipeline**
- 概念：类似jenkins，可以像jenkins一样配置好文件，每天在指定时间自动执行pipline，可以与s3配合，将运行结果存储到s3上，也可以对这些日志运行EMR生成报告


---
**Amazon EMR**
- 概念：EMR(Amazon Elastic MapReduce)是一个托管集群平台，可以简化大数据框架(Apache Hadoop,Apache Spark)的运行过程，用来分析和处理大量数据
- 考点：
  + EMR允许大量数据转入和转出到其他存储服务，如s3和dynamoDB
