# AWS-Test

## 计算
---
**AWS Batch**
- 概念：AWS Batch可以运行任何规模的批处理任务


---
**AWS EC2**
- 概念：AWS Batch可以运行任何规模的批处理任务




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
