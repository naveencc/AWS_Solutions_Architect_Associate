## AWS: Platform & Services

### Infrastructure:
AWS infra is split into Regions and Availability Zones

Regions(R): A geographic area where AWS resources exist, currently 15. Each R contains 2 or more AZ and these AZ provide the services
Availability Zones(AZ): A physical data center, nearly 35
Edge Location: A content delivery network, that can be used to cache the data/content for user. It is the CDN endpoint for AWS Cloudfront. There are nearly 66 Edge Location

#### VPC: 
It is a virtual Data Center in all the regions, multiple VPC / region.
Note: Very Important

#### Route 53:  
Amazon DNS service, Route + 53< here 53 is DNS port> and route is after route 66

#### Cloud Front: 
Caching and CDN service for large files and media services

#### Direct Connect: Dedicated line connection, this service is not used to reduce reliability on Internet

#### EC2 / Elastic Compute Cloud: 
This is virtual machine on AWS, provide compute resources
EC2 Container Service (ECS) - Its basically a docker instance

#### EBS / Elastic Bean Stalk: 
this is used to deploy and manage applications and code to AWS. 
EBS will review the application and automatically detect deployment requirements, autoscaling, load balancing, health monitoring.
Use other services such as EC2, S3, ELB,  Autoscaling to deliver highly reliable, scalable and cost-effective infrastructure
AWS cloud watch can be used to monitor the status and health and requirements of the application.

#### Lambda: 
Allow to run application without need of a Server.
The code is run whenever there is new data, or a new trigger for code. no charges for ideal time
Good for real time data processing.
Good for Not, mobile or Web apps
Benefits: No server to manage or maintain, pay per use, no charge for idle time
Trigger for Lambda can be generated by either kinesis, S3, Simple Notification Service, DynamoDB to trigger Lambda operation. This is due to any incoming load or change in the state
Charging - Every 100ms code runs, or every trigger for the code.

#### Light sail: 
Allow users to deploy basic websites on Joomla or Wordpress if they do not have much experience with AWS


### Storage:
Has  4 components - 

#### S3 / Simple Storage Service :
Used to store objects on cloud 

#### Glacier:
Archive files off S3 to it
Store these files for long time, extremely low cost.
Very slow retrieval time <3-4 hr>

#### AFS / Elastic File System:
This is Block based service
This can be shared between different systems on EC2 which can access the file simultaneously and update it.
Similar to Google sheet/slide
Pay only for files and directories used, no minimum fee or setup charge
Durable and high availability, replicate in different AZ in a region

#### Storage Gateway Service:
This service connects S3 to on premise data-center
Its a image that can connect with the S3.


### Databases:

#### RDS <Relational Database Storage>: Important
Offer relational data storage, with following flavors : MySql, MariaDB, PostgresQL(2016), Aurora, Oracle
Have pre-configured image of all the database, does not require need of an adminstrator

#### DynamoDB <Non Relational NoSQL DB>:
This is No SQL data system, it offers scalable storage
Competitors: Cassandra, MongoDB

#### Aurora:
- Amazon’s own relational database system.
- Have a mySQL compatible storage engine
- provide 5 time throughput compared to current RDBMS
- 1/10 cost of existing enterprise solutions and no license fee
- Read heavy applications can increase availability with data replicated across servers in less than 10ms
- Security: network isolation using VPC, data encryption in rest through AWS key management, data encryption in motion by SSL
- automated backups, snapshots and create replicas for data
- Compatible with MySQL 5.6 using InnoDB storage engine , any code used with MySQL can be used with it.
- Can replace Oracle, Postgres, SQL Server
- AWS DMS and AWS Schema Conversion tools can be used to migrate the data to Aurora
- Offer high availability, failover < 30sec, 6 copies replicated across 3 AZ and copies replicated on S3 

#### Redshift < Data Warehouse Solution>:
Its data warehouse for storage of big data
Running queries on production system make it slow, so queries can be run on a data warehouse for the purpose of analytics. 
Competitors: Vertica,  Terradata
Store in columnar format, parallel process data, OLAP Database

#### Elastic Cache <Caching Storage>:
Allow fast data retrieval through data stored in memory caches, its in memory data cache system
E.g. If user is interested in top 10 items in a store, it can get the result directly from cache.
Can help to improve performance of read heavy applications as  it reduce latency in returning results.
It will take care of persistence itself
Use following open source engines - Memcached / Redis for task
Redis: Good to store data which is structured with common use cases as  - Leaderboards, Counting, Tracking, session management. Redis vs Memcached: https://stackoverflow.com/questions/10558465/memcached-vs-redis
On demand nodes,


### Migration:

#### Snowball:
- import export data over hard disk and move data on cloud
- Hardware appliance that copy data and move to S3
- It has been extended to on premise data center

#### DMS<Database Migration Service>:
- allow to migrate on premise database to cloud
- allow to move data from RDS to redshift or other region
- allow to migrate from one DB to other DB eg. Oracle to AURORA
- There is no downtime in migration

#### SMS <server migration service>
- allow to migrate the virtual machines on ec2
- no downtime


### Analytics:

#### Athena:
Allow to run SQL Query on S3.
Allow to query CSV, txt

#### EMR<Elastic Map Reduce>:
Big Data processing
Log Analysis, 

#### Elastic Search:

#### Cloud Search

#### Kinesis: <important>
Stream and analyze real-time stream data


#### Data Pipeline:


#### Quick Sight:








