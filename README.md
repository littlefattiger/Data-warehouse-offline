# Data-warehouse

This is a repo code for my code from [here](https://www.bilibili.com/video/BV1rL411E7uz)

Main idea:
- Collect logging and behaviour by using flume
- Dimension data is store in Hbase because it is easy to extract
- Using Kafka to do message queue and pass data
- once data is in HIve, all DB process, by using script daily or arzkaban. Easy now.
- Finally we can do a display

### This is a offline data-warehouse, the data will refresh daily.

Tools:

- 3 nodes(VM)
- Hadoop: 3.1.3 -> Storing and computingh
- zookeeper: 3.5.7 -> coordinator, using paxos protocal
- Mysql: 5.7.30 -> OLTP, can not hold too large data
- Hive: 3.1.2 -> OLTP data warehouse
- Flume: 1.9.0 ->loging collection
- kafka: 2.4.1 -> Message Queue
- Azkaban: 3.84.4 -> Task scheduler
- Spark: 3.0.0 -> Real time computing(here use hive on spark)
- Hbase: 2.0.5 -> Key value database
- Sqoop: 1.4.6 -> sync between HDFS and Mysql
- Presto: 0.189 -> realtime OLAP
- Kylin: 3.0.1 -> realtime OLAP but with pre-calculate used Hbase
- Atlas: 2.0.0 -> data manager
- Ranger: 2.0.0 -> role manager
- Solr: 7.7.0: Search engineer. Similar as Elasticsearch

## Overview/Offline warehouse
![image](https://github.com/littlefattiger/Data-warehouse/blob/main/offline_Warehouse.png)
