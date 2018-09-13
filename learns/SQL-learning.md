# <center>MySQL学习</center>
## 相关概念
1. 数据库定义：  
   存放数据的仓库，是为了实现一定目的，按照某种规则组织起来的数据的集合。广义上讲，计算机内所有可以保存数据的文件或系统都可以称为数据库，狭义上，数据库一般指**较小的数据冗余、较高的数据安全、易扩展的专门用于存储数据**的软件系统。  
2. 大数据  
   大数据是一个体量大、数据类别多的数据集，且这样的数据集无法用传统的数据库工具对其内容进行抓取、管理和处理。具有数据体量大、数据类型多样、处理速度快、价值密度低等特点。大数据是由数据量变到质变产生出来的一个概念，并衍生出一系列技术。
3. 数据库的优点  
   + 可以结构化存储大量信息，方便用户进行有效的检索和访问。
   + 可以有效保持数据信息的一致性、完整性，降低数据冗余。
   + 满足数据共享与安全的要求。
4. 常见的数据库  
   + 关系型数据库：MySQL、Oracle、SQL Server……
   + 非关系型数据库：文档存储数据库：MongoDB；  键值存储数据库：Redis、Memcached；  列存储数据库：HBase；  图形数据库：Neo4j。  
5. 实体和数据库表  
   + 实体：客观存在，可以被描述的事物。比如计算机、人、课本等。
   + 属性：在描述实体时，我们是针对该实体的种种属性进行描述的。
   + 记录：在存储的数据表格中，每一行对应一个实体，在数据库中，通常叫做一条“记录”。
   + 字段：在存储的数据表格中，每一列对应实体的一条属性，称之为“字段”。
   + 数据表：把相同类型的记录组织在一起的数据结构称为数据库“表”。
   + 数据库：数据表、关系（被抽象成统一的概念，通过键、类型、规则、权限、约束等抽象概念联系）、以及其他的各种数据库对象。
6. 数据库管理系统（DataBase Management System，DBMS）  
   + DBMS：是一种系统软件，由一个互相关联的数据集合和一组访问数据的程序构成。简而言之，数据库管理系统包括数据库以及用于数据库访问管理的接口系统。
   + 数据库系统（DataBase System，DBS）：是一个实际可运行的系统，可以对系统提供的数据进行存储、维护和应用，它是由存储介质、处理对象和管理系统共同组成的集合体，通常由软件、数据库以及数据库管理员组成。
   + 数据库管理员（DataBase Adminstrator，DBA）：是指在数据库系统中负责创建、监控和维护整个数据库的专业管理人员。
7. 数据冗余与数据完整  
   + 数据冗余：指不同记录中出现了数据重复。
   + 数据完整：指数据库中数据的准确性，如果两个或更多的表由于其存储的信息而相关联，那么只要修改了其中一个表，那么其他所有的与之相关联的数据都要做出相应的修改，如果不这么做，存储的数据就会不再准确，也就是说，失去了数据的完整性。
8. 主键和外键
   + 主键（Primary Key）：一个值可以用来唯一标识表中的每一行，用来强制表的完整性的列，定义为主键。选择原则：最少性（指列数最少的键）、稳定性（指列中的数据不要经常更新，理想情况下，应该永远不变）。
   + 外键（Foreign Key）：相对于主键而言的，从表中对应于主表的列，在从表中称为外键或者引用键。  

## SQL简介
###