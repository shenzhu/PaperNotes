# Big Data @ Facebook
---

## Keyword
***Big Data***, ***Data Storage***, ***Facebook***

## 1. Introduction
Many kinds of applicatons in Facebook depend on a data infrastructure platform that can **process**, **analyze** and **serve large quantities of data**.

The data storage of Facebook has three main components:

- **MySQL/DB** plus caching component that serves as the **primary data repository** for serving production traffic.
- **HDFS/MaoReduce/Hive** component that serves as a platform for **deep analytics** on Facebook data.
- **HBase** runs OLTP-like applications, both for internal applications and some external products.

## 2. Data Warehousing and Analytics Infrastructure
The following are the main components in the Data Warehousing platform:

- ***Scribe:*** collecting **log data** from the web server tier and **making it available** in the Hadoop/HDFS cluster for later analysis.
- ***HDFS/MapReduce:*** Facebook's data analytics engine is built on top on the ***core platform*** of Hadoop HDFS and MapReduce.
- ***Hive:*** a data warehouse system for Hadoop that facilitates easy data summarizing, ad-hoc queries, and analysis of data stored in Hadoop HDFS.
- ***HiPal:*** a UI platform for SQL syntax softwares.
- ***NoCron:*** an automation framework that allows engineers and non-engineers to automate repetitive tasks. NoCron allows users to organize their **analysis tasks** into workflows and specify parameters of the workflow.


## 3. Challenges in Managing Big Data
1. ***Data Growth:*** The main techniques for dealing with data growth:
	- HDFS Federation - federating data across multiple HDFS clusters
	- Improvements to JobTracker scalability in MapReduce
	- Reducing data footprint by using RAIN instead of 3-way replication
	- Improved Data storage formats such as RCFile
2. ***Isolation:*** As the load and the number of applications running on the shares data infrastructure increases, ioslation between the different application becomes increasingly important, three aspects of isolation:
	- **Space Isolation** - ensuring space requirements of one application do not stomp on the usage requirements of other applications.
	- **Compute Isolation** - ensuring compute performance of different applications are isolated from each other.
	- **Fault Isolation** - ensuring faults in one applications do not adversely affect other applications.
	
       The current solution is to **ensure isolation at the hardware layer**

3. ***Multiple Data Centers:*** scaling the data infrastructure to take advantage of and cope with multiple data centers becomes import, challenges:
	- Replicating data across data centers
	- Flexible use of storage/compute capacity available in different data centers.
	- Ability to share data between different regions so that applications can be run in any region without worrying about locality.
	
	Facebook is currently working on the next generation of Facebook's data infrastructure, named **project Prism**.


## 4. Conclusions

## Questions & Ideas

## Location
***D:\Papers\MBDS.2012.Aravind Menon.pdf***

## Date
**2013.10.11**

---