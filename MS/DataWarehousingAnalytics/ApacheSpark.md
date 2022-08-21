# Apache Spark

Installation : https://phoenixnap.com/kb/install-spark-on-windows-10

MapReduce: ​​It is a framework that allows the automatic implementation of parallelization for task processing.
Apache Hadoop: It is a collection of software utilities for scalable distributed computing.
Hadoop Distributed File System (HDFS): This file system is designed to store GBs/TBs of data with high reliability.
Apache Hive: It is an abstraction used for reading, writing, and managing large data sets residing in HDFS using SQL-type queries.

Apache Spark is a big data utility that has gained a lot of popularity in a very short period. Since its development in 2013, global giants such as Amazon, LinkedIn, Alibaba, Uber, etc., have been using Spark extensively in their production environments. Let's hear from our SME, Vishwa Mohan, about the contents of this module.

“Apache Spark™ is a multi-language engine for executing data engineering, data science, and machine learning on single-node machines or clusters." as defined on the company’s website. It is an open-source, distributed computing engine that provides a productive environment for data analysis owing to its lightning speed and support for various libraries.

Being an open-source, distributed-computing engine, Spark allows developers and companies to constantly improve the rich library it offers. Some typical use cases of Spark include the following:

 To perform exploratory analysis on data sets in the scale of hundreds of GBs (or even TBs) within a realistic time frame.
To run near real-time reports from streaming data.
To develop machine learning models.

The four main features which make Spark a powerful unified engine for data processing at a massive scale are below:

* Speed: Big data processing is all about processing large volumes of complex data. Hence, organizations and enterprises want frameworks that can process massive amounts of data at high speed when it comes to big data processing. This is one of the defining characteristics of Spark. Spark is known for its speed, which is considered to be 100x faster than the MapReduce framework. This speed results from its in-memory computation and use of the DAG scheduler.                                   
* Ease of use: Spark offers language support in Java, Scala, SQL, Python, and R to run queries using 80+ high-level operators interactively.
* Generality: Spark not only supports simple map and reduce operations but also supports SQL queries, streaming data, and advanced analytics, including ML and graph algorithms. It has a powerful stack of libraries, such as SQL, DataFrames, MLlib (for ML), GraphX, and Spark Streaming. What’s fascinating is that Spark lets you combine the capabilities of all these libraries within a single workflow/application in its ecosystem.
* Runs everywhere: Spark can run using its standalone cluster manager on Apache Mesos, on Hadoop Yarn or Kubernetes, and even in the cloud. Spark can access data stored in various storages, including HDFS, S3, and others.


As you can see, Spark is extensively used by multiple industry domains for its day-to-day activities. You learned about a few use cases in the video, so now let’s discuss a few more of them.

 

Spark can process a large pool of data and return results very quickly. Thus, it aids in many business decisions and optimizes the workflow for companies. Companies like Walmart can analyze data across multiple stores quickly and therefore manage their sales and inventory efficiently. 
The abilities of Spark also benefit the banking and finance industry. Banks process billions of transactions daily as their network spreads worldwide. They have databases that collect real-time data, which is then analyzed using frameworks like Spark to detect if any fraud is occurring in the background.
Several industries rely on Spark to maximize their revenue. For instance, ride-sharing applications, such as Uber calculate surge prices based on bookings and the availability of drivers in a particular area. They run complex machine learning algorithms in real-time, and the results are reflected directly on their mobile applications. Running such machine learning algorithms is possible because of the rich support of libraries offered by Spark. 
Another use case is personalized advertisements. Companies track users' browser histories and show them personalized ads on websites or applications they access. Running such ads becomes possible owing to the rich library support and the quick analysis features of Spark.

https://spark.apache.org/
https://www.dezyre.com/article/top-5-apache-spark-use-cases/271
![image](https://user-images.githubusercontent.com/20191454/185745297-f224cc82-a9c7-4edf-946a-7acb1d9b6163.png)

Now, let’s discuss the types of delays that occur while accessing data from a disk:

* Seek time: This is the time taken by the read/write head to move from the current position to a new position.
* Rotational delay: This is the time taken by the disk to rotate so that the read/write head points to the beginning of the data chunk.
* Transfer time: This is the time taken to read/write the data from/to the hard disk to/from the main memory.
Access time denotes the total time delay or the latency between when a request to read data is submitted and when the disk returns the requested data. The access time of a disk is calculated by adding all the delays, as shown below:

 

Access Time = Seek time + Rotational delay + Transfer time

Why in-memory data processing systems?

* Real-time data processing: Since data can be accessed very fast, in-memory processing can be used in cases where immediate results are required.
* Accessing data randomly in memory: Since data is stored in the RAM, memory can be accessed randomly without scanning the entire storage.
* Iterative and interactive operations: Intermediate results are stored in memory and not in disk storage so that we can use this output in other computations.



 In the iterative operations on the MapReduce slide, it is to clarify that the memory between Map and Reduce jobs is disk-based memory and not in-memory.

 

As explained in the video, iterative queries are much faster in Spark than in MapReduce, and this is because of Spark’s in-memory processing. Interactive queries also work better on Spark since, for every query, data is not fetched again from disk memory.

 

Now let’s learn about processing. Processing is of the following two types:

Batch processing

In batch processing, data is collected over a period of time and is available for analysis in a batch. Output from such tasks is not expected instantly, and, hence, you can work without a high-speed processing framework. An example of batch processing can be processing credit card bills at the end of every month. The credit card company runs a monthly batch job to process all the transactions a user makes in a month to generate the bill.

Real-time processing.
 
In real-time processing, data is collected and processed continuously. Typically, for such tasks, the system needs to produce output in a very short span of time, sometimes almost instantly. As an example, payment systems such as PayPal, credit card companies like Visa, and many others use fraud detection algorithms to identify suspicious transactions. For instance, someone hacks a person’s account and makes purchases. Since fraud detection will be useful only if one can identify a fraudulent transaction right when it occurs, the data needs to be analyzed as soon as the transaction is initiated. (Additional reading about this is provided below.)

https://opensource.com/business/15/1/apache-spark-new-world-record

he main differences between Spark and MapReduce are below:

MapReduce involves disk-based processing, and the processing is slow; whereas Spark involves in-memory processing, and the processing is fast.
MapReduce involves only batch processing, and Spark involves both batch processing and real-time data processing.
In MapReduce, interactive queries repeatedly access data from disk; whereas in Spark, interactive queries are done on distributed in-memory da

![image](https://user-images.githubusercontent.com/20191454/185778724-b6681add-6a23-4ac5-8c36-a508e0662759.png)


Spark Core:

Spark Core is the heart of Spark and is responsible for all kinds of processing.
Everything in Spark, including Spark API, is built on top of Spark Core, which provides an execution platform for every other Spark API. 
The Spark Core engine executes all Spark jobs with RDDs as inputs.
Even if you use any high-level API for optimizing your Spark tasks, Spark handles the data internally in the distributed environment using RDDs. You will learn about Spark RDDs in upcoming sessions.
Here is a glimpse of RDD storage and representation of data:
Spark RDD
Spark RDD
Dataframe API:

When dealing with a structured form of data, you will be using the Dataframe API.
Dataframe API stores the data in a table structure. You will learn more about the different data types in the next module.
Let us have a glance at Dataframe storage and representation of data.
Spark Dataframe
Spark Dataframe
SparkSQL:

Spark SQL is Apache Spark's module for working with structured data.
It is a high-level API that lets you utilize Spark's power using SQL queries.
You do not have to modify your SQL query code. Spark SQL functionality can run your SQL query.
Spark SQL supports the HiveQL syntax as well as Hive SerDes and UDFs, allowing you to access existing Hive warehouses. We will discuss Spark SQL in the next module.
Spark Streaming:

Spark Streaming involves processing live data streams in Spark. This feature of Spark is another advantage over MapReduce. 
Spark Streaming provides APIs that resemble the RDD API used in Spark Core. Due to this, you can easily manipulate data that is either stored on disk or is coming from live data streams.
It provides the same level of fault tolerance as provided by Spark Core.
Spark streaming is used extensively in the industry. Companies like Netflix use Kafka and Spark Streaming to run real-time engines that provide movie recommendations to their users. Banks can build real-time fraud detection systems to minimize fraud. To know more about Spark Streaming use cases, refer to this link: Spark Streaming use cases.
MLlib:

MLlib involves applying machine learning algorithms. To analyze and build models over the distributed data sets, MLlib offers a wide range of features.
It supports functionalities that include model evaluation and data import.
GraphX:

GraphX is used to process large volumes of data in Spark in the form of graphs.
It is Spark’s tool for ETL (Extract, Transform & Load) process, exploratory analysis, and iterative graph computation.
This package also provides different operators for working with graphs and manipulating them.
The usage of graphs can be seen in LinkedIn’s connections (networks), Facebook friends, and Google maps. These are all different kinds of graphs. For example, if you want to find out which family member has the most number of connections on Facebook or which two cities in the country are located farthest from each other, you can use GraphX to get the answers. To know more about Spark Streaming use cases, refer to this link Introduction to Spark GraphX.
Packages:

Different packages like PySpark, SparkR, etc., help you run queries on big data through the libraries supported by languages like Python, R, etc. This flexibility of using different languages to write code adds to Spark's ease of use.

https://www.projectpro.io/article/apache-spark-ecosystem-and-spark-components/219#:~:text=analytics%20than%20Hadoop.-,Apache%20Spark%20Ecosystem,vital%20factor%20in%20its%20growth.

https://www.freecodecamp.org/news/what-is-an-api-in-english-please-b880a3214a82

![image](https://user-images.githubusercontent.com/20191454/185778907-2bc043cb-24ce-4ebe-9201-3f151acc24fd.png)


From the image above, it should be clear that the driver and the worker nodes are physical machines on which the driver program and the executor work. The driver program manages the Spark application you submit, and the executor program uses the worker nodes as the distributed storage and processing space to run those applications. Both storage and processing require multiple worker nodes, as you are dealing with the distributed data.

 

Now you have the driver and worker nodes to perform the tasks that a user submits. However, in a distributed cluster, multiple processes are running at the same time. Therefore, you will also require a resource manager which can efficiently divide the resources. Let’s watch the upcoming video and try to get an understanding of this.

To summarize, the driver program and the executor program are managed by the cluster manager. A cluster manager is a pluggable component in Spark. Because of this, Spark can run on various cluster manager modes, which include the following:

 

In the Standalone mode, Spark uses its own cluster manager and does not require any external infrastructure.
However, at an enterprise level, for running large Spark jobs, Spark can be integrated with external cluster managers like Apache YARN or Apache Mesos. This facility allows it to be deployed on the same infrastructure as Hadoop and acts as an advantage for companies looking to use Spark as an analytics platform.
Apache Mesos is deprecated in the latest version of Spark, but it’s still a widely used cluster in the industry.
Spark has also added Kubernetes as a cluster manager in its latest version.
 

Now, let's understand how a Spark job gets executed in Spark.

![image](https://user-images.githubusercontent.com/20191454/185779052-3045ab7f-75a6-4255-b3a6-7741af0341b9.png)

To understand each process even more efficiently, let's figure out the role of each part in the entire process.

 

The role of SparkContext:

SparkContext does not execute the code but creates an optimized physical plan of the execution within the Spark architecture. It is the initial entry point of Spark to the distributed environment.
The role of the driver program:

The driver program is like the main() method that contains the instructions and action steps to be taken on the data present in each worker node.
A driver program creates a general logical graph of operations. These operations mostly involve the creation of RDD from some source data, transformation functions to manipulate and filter data, and finally, some action to save the data or print it.
When the driver program runs, the logical graph is turned into an execution plan.
In Spark terminology, a process or action on data is called a Spark job. A job is further broken down into different stages. These stages help make the Spark environment reliable and fault-tolerant, which we will look at in the later sections. Finally, each stage comprises tasks the executors implement. A task is the most basic unit of work that each executor performs parallelly on the respective partition of data. 
Once the entire execution plan is ready, the Spark driver coordinates with executors to run various tasks.
The role of the executors:

Executors are processes that are launched for a Spark application on worker nodes.
Each worker node consists of one or more executor(s) and is responsible for running the task.
The main task of an executor is to run the tasks and send results to the driver program.
It also stores the cached data that is created while running a user program.
One executor can consume one or more cores on a single worker node.

Assume the following:

If one executor runs on one core, and one worker node contains eight cores, there will be eight executors in a single worker node. Since every executor has only one core to run a process or task, the operations in the program cannot be parallelized.
If one executor runs on two cores, and one worker node contains eight cores, there will be four executors in a single worker node. Since every executor has two cores to run a process or task, the operations in the program can be parallelized.

If you are running Spark in local mode and not a distributed environment, the driver and executor programs run on the same JVM.

 

The role of cluster manager:

It launches the executor programs and allocates and manages the resources allocated to each component.
Now, let’s revisit how the different components in Spark work together to execute the physical plan that SparkContext creates. SparkContext sends the optimized physical plan to a cluster manager (could be Standalone, YARN, or Mesos) in the Spark framework. The cluster manager first checks for the availability of resources in the cluster and then allocates worker nodes based on the requirement. These worker nodes are responsible for loading the data and executing the desired tasks over each partition of the distributed data. This parallelism is responsible for fast computation in Apache Spark.


Another added advantage of the Spark architecture is that it can be deployed over distributed storage systems such as Hadoop as it is. No additional support is required to make it functional over these storage systems.

https://spark.apache.org/docs/latest/cluster-overview.html
![image](https://user-images.githubusercontent.com/20191454/185779194-39184d36-3537-4f1f-8ab1-fbc5b304682d.png)

![image](https://user-images.githubusercontent.com/20191454/185779489-d88d9ca4-cafd-4d65-9c5e-65ba9d65d338.png)
![image](https://user-images.githubusercontent.com/20191454/185779513-db31ed19-244c-4af5-99dd-23a56677b3e9.png)




