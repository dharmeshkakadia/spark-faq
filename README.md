# spark-faq
Frequently asked questions about Spark

### How do I run SQL queries from Spark from headnode?
Use beeline to talk to Spark thrift server. The thrfit server runs on 10002 port. Following will connect to default database 
``
beeline -u "jdbc:hive2://localhost:10002/default;transportMode=http"
``

### Where do I see query details(plan,tasks,counters etc.) when running queries using thrift server?
Go to Ambari --> Yarn UI --> scheduler --> click on thrift server application master.

### How do I cache table while running queries through thrift server?
Use ``cache table <tablename>``.
