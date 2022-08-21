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

![image](https://user-images.githubusercontent.com/20191454/185781345-b31695a9-96f6-4b00-8618-bddb579a7067.png)

https://spark.apache.org/docs/latest/
https://spark.apache.org/docs/2.3.1/api/python/index.html

RDD
Resilient Distributed Data sets (RDDs) form the core abstraction of Spark. In this segment, you will understand the structure of an RDD. RDDs are special data types that are tailor-made for Apache Spark. The first boost to the performance of Apache Spark came from the innovative nature of the structure of an RDD. An RDD can be considered a distributed set of elements. Let’s hear about it from our expert Vishwa in the next video.

![image](https://user-images.githubusercontent.com/20191454/185781503-7573f3e8-ec66-4d65-a07b-bab50cd15624.png)
![image](https://user-images.githubusercontent.com/20191454/185781516-0db33743-deed-4304-a39b-a82731f7aa25.png)
![image](https://user-images.githubusercontent.com/20191454/185781537-e0511cbb-196e-4612-b7eb-46e4b8539d4d.png)
![image](https://user-images.githubusercontent.com/20191454/185781566-866e3a41-d4c8-42e4-8f25-76a1c6ab72d4.png)
![image](https://user-images.githubusercontent.com/20191454/185781591-7c9bae40-3e0b-4bd8-ac90-1d9131c2a512.png)
https://www.usenix.org/system/files/conference/nsdi12/nsdi12-final138.pdf

![image](https://user-images.githubusercontent.com/20191454/185781606-d407ddc5-9571-43d7-8732-608a906bd85c.png)

---
sc
---

The collect() function sends all the values of an RDD back to the driver node. If the RDD is vast, then this function can result in an Out of Memory error.

Note: In the above case the output01 folder(the last folder mentioned in the path) will be created by Spark in the HDFS and should not already exist. 

https://spark.apache.org/docs/latest/rdd-programming-guide.html

RDDs are low-level APIs used by Spark to abstract information on how data is partitioned across various devices in a cluster. Since you can store data in RDDs, you can use multiple operations to manipulate and analyze data stored in RDDs. In the next video, let's hear from Vishwa Mohan, who explains these operations.
![image](https://user-images.githubusercontent.com/20191454/185782948-8d68555c-1ba7-4984-892e-b78f7e90f115.png)

 Some examples of actions are as follows:

 

count(): It counts the number of elements in an RDD.
collect(): It is used to retrieve all the elements of the RDD (from all nodes) to the driver node. 
reduce(): It reduces the elements through an aggregation function. The most common type of the reduce function is a sum.

https://spark.apache.org/docs/latest/rdd-programming-guide.html

![image](https://user-images.githubusercontent.com/20191454/185783001-5fe2269e-dfed-4748-94e8-93514dea349d.png)

union(): This operation will work on two RDDs and will result in an output that contains all the elements present in both the RDDs.

"rdd1.union(rdd2)"


intersection(): This operation will work on two RDDs and will result in an output that contains only those elements that are present in both the RDDs.

“rdd1.intersection(rdd2)”

 

subtract(): This operation will work on two RDDs and will result in an output that contains all the elements present in rdd1 but not those present in rdd2.

“rdd1.subtract(rdd2)”

 

cartesian(): This operation will work on two RDDs and will result in an output that contains pairs of each element of rdd1 with each element of rdd2.

"rdd1.cartesian(rdd2)"

 

Let’s take a look at the following example for cartesian().

document1 = [1,2,3]

document2 = [4,5,6]
sc.parallelize(document1).cartesian(sc.parallelize(document2)).collect()
![image](https://user-images.githubusercontent.com/20191454/185787708-f3932d16-dd2f-49f5-992d-3ff7ad00deae.png)

![image](https://user-images.githubusercontent.com/20191454/185787718-e10d7838-4e6e-4ae5-83c2-7fd834e6c557.png)


https://spark.apache.org/docs/latest/rdd-programming-guide.html#transformations

In the previous segment, you learned about different transformation functions on RDDs. Transformation functions are used to perform a particular operation on an RDD and store new values in a new RDD, as RDDs are immutable. However, you can get an output or a result only when you apply actions on an RDD. Also, all transformations on an RDD are executed only when an action is performed on that RDD. You will learn about this type of evaluation in the following segments.

 

In this segment, you will understand what actions are available for RDDs. Let's watch the next video where Vishwa Mohan will discuss action operations on an RDD.


Note: In this module, you may sometimes see that the kernel is mentioned as Python 2 instead of PySpark. This is because some of these videos are shot in a local environment/EC2, and the Python 2 kernel had the PySpark libraries installed already. For the current configuration of EMR, you will need to use the PySpark kernel only. The SME has used EC2 instance instead of EMR instance, but you are recommended to use the EMR instance for running all your codes in PySpark kernel.

The action operations discussed in this video are as follows:

 

collect(): This operation collects all the elements of an RDD from every partition and returns the result as an array to the driver node.


count(): This action returns the total number of elements of an RDD.


take(num): This operation takes the first num (number) of elements of an RDD.

It first scans one partition and then uses the results from that partition to estimate the number of additional partitions needed to satisfy the limit.

Question: If two RDDs are made from the same data file, with one RDD having n partitions and another RDD having m partitions, will the answer to first() or take(1) operation on both of these RDDs be the same?

Answer: Yes. The answer to first() or take(1) operation for both RDDs will remain the same.


top(num): This operator will return the num highest values in an RDD in descending order. 


countByValue(): This is a powerful operator. When applied to an RDD, it returns a dictionary of (key, value) pairs, where each key is one element of the RDD, and each value is the number of times an element has appeared in that RDD.


Let’s take a look at the following example for countByValue().

 

#words RDD was created in the previous segment.
words.countByValue()

 

collect(): This operation collects all the elements of an RDD from every partition and returns the result as an array to the driver node.


count(): This action returns the total number of elements of an RDD.


take(num): This operation takes the first num (number) of elements of an RDD.

It first scans one partition and then uses the results from that partition to estimate the number of additional partitions needed to satisfy the limit.



Pro Tip:

There is one more action operation, rdd.first(). It returns the first element of an RDD. There are two questions that can be asked regarding this action. 


Question: Is this action the same as take(1)?

Answer: The output of both first() and take(1) is the same, but the output type is not the same. Take(1) will return the output in the form of an array no matter the number of elements present in that array. On the other hand, first() will return only the first element of an RDD.


Question: If two RDDs are made from the same data file, with one RDD having n partitions and another RDD having m partitions, will the answer to first() or take(1) operation on both of these RDDs be the same?

Answer: Yes. The answer to first() or take(1) operation for both RDDs will remain the same.


top(num): This operator will return the num highest values in an RDD in descending order. 


countByValue(): This is a powerful operator. When applied to an RDD, it returns a dictionary of (key, value) pairs, where each key is one element of the RDD, and each value is the number of times an element has appeared in that RDD.

The output will be 15; x and y signify any two elements of the RDD [1,2,3,4,5].

 

fold() function: Aggregate the elements of each partition, and then the results for all the partitions, using a given associative function and a neutral zero value.  The zero value is used as the initial value for each partition in folding. It is used to initialize the accumulator for each partition. It acts as an initial call to each partition.

Both reduce() and fold () operations are quite similar with minimal difference between them. The difference is that fold doesn't need to worry about empty partitions or collections, because then it will just use the zero value.

Now, let’s try to understand another action function from Vishwa.

Aggregate() function: Aggregates the elements of each partition and then the results for all the partitions using a given combination of functions and a neutral zero value.

Since RDDs are partitioned, the aggregate takes full advantage of it by first aggregating elements in each partition and then aggregating results of all partitions to get the final result. Aggregate() lets you take an RDD and generate a single value that is of a different type than what was stored in the original RDD.

Let’s understand its arguments. 

seqOp aggregates the elements from all the partitions, and combOp merges all the results of seqOp in all the partitions. Both the operations share the same initial values which are called zeroValue.

Let’s understand these operators in more detail.

zeroValue: Initial value to be used for each partition in aggregation. This value would be used to initialize the accumulator. We mostly use 0 for integers and nil for collections.
seqOp: It is an operator used to accumulate results within a partition. This operation will walk through all the elements (T) in all the partitions. All the T[0] will merge with zeroValue, and its result will merge with T[1] and so on until it loops over all the partitions. In other words, this sequential operation is just like rolling a given function on RDD.
combOp: It is an associative operator used to combine results from different partitions. It will return a different type of result compared to the original RDD. As a result, you need to use seqOp to merge all the T in each partition to U, and then use combOp to combine all the U togeth

foreach() function: Applies a function to all elements of this RDD.  
It does not return any value, and it executes the input function on each element of an RDD. It does not return any value to the driver node, instead, the code is executed and stored in the worker node itself.

https://spark.apache.org/docs/latest/rdd-programming-guide.html#actions

![image](https://user-images.githubusercontent.com/20191454/185788719-d26da9ff-38d6-4afa-a7b1-7778c7b17264.png)
![image](https://user-images.githubusercontent.com/20191454/185788733-5dd8a280-8e14-4e5f-a576-ced8076aed31.png)
![image](https://user-images.githubusercontent.com/20191454/185788747-af303d5a-6ca5-4b34-b71a-02776a823372.png)

Spark records each transformation applied to an input RDD as an edge between the input RDD and the resulting RDD. Hence, in a way, the number of edges in the DAG represents the total of transformation applied. In this case, the number of edges present in the DAG is 5. Hence, the answer is 5.
 

This session will build on the programming aspect of Spark. You will learn how to process data in Spark paired RDDs using the PySpark API. This session covers:

 

Creating paired RDDs.
Operations on paired RDDs.
Solving problem statements. 
 The objective of this session is to give you hands-on experience of working on the computation engine of Spark. If you encounter errors while running codes, try debugging them on your own to gain valuable experience in handling Spark jobs.






As discussed in the video, you can easily create a paired RDD using the parallelize() function as the base RDDs.

 

rdd = sc.parallelize([(‘a’, 3), (‘b’, 4), (‘c’, 2), (‘d’, 5)])
rdd.collect()
 

You can also use the following methods to create the paired RDDs:

The textFile() method.
Transforming base RDDs.
The limitation with textFile() function is that the structure of the file must be in a <key, value> format to load the data directly in the form of paired RDDs. 

 

Another method to create paired RDDs is by transforming the base RDDs. Transformations like map() and flatMap() can be used to convert the base RDD into paired RDD.

 

Let’s look at an example of transforming the base RDDs using map() method.

 

rdd1 = sc.parallelize([1,2,3,4,5])
rdd2 = rdd1.map(lambda x:(x,1))
rdd2.collect()

There are two important methods, reduceByKey() and groupByKey(), in paired RDDs. Let's understand both of them one by one.

 

reduceByKey(): The reduceByKey() method is used to perform a particular operation on the elements of RDDs. Let’s look at an example.

 

rdd2 = sc.parallelize([("shampoo", 1), ("soap", 1), ("conditioner", 3), ("brush", 2), ("soap", 2), ("shampoo", 2), ("bread", 2), ("meat", 2), ("tshirt", 2), ("jeans", 2)])


sorted(rdd2.reduceByKey(lambda x, y:x+y).collect())

Here, x and y are any two values which are to be added for a particular key. Let’s look at the output of this operation.

 

[('bread', 2), ('brush', 2), ('conditioner', 3), ('jeans', 2), ('meat', 2), ('shampoo', 3), ('soap', 3), ('tshirt', 2)]

We can see that reduceByKey() will perform the defined operation on the values of a particular key.

 

Let’s understand this operation with another example.

reduceByKey() example
reduceByKey() example
Pro Tip:

The reduce() method in basic RDDs is an action operation that returns a result to the driver program. However, reduceByKey() is a transformation operation that results in a new paired RDD with a key-value pair where the value is now an aggregated result for that particular key.


groupByKey(): The groupByKey() method performs the same operation as reduceByKey(), but it creates an iterable for the values for a particular key. You get back an object which allows you to iterate over the results.

Let’s see the example learned in the video. 

 


rdd3 = sc.parallelize([("shampoo", 1), ("soap", 1), ("conditioner", 3), ("brush", 2), ("soap", 2), ("shampoo", 2), ("bread", 2), ("meat", 2), ("tshirt", 2), ("jeans", 2)])
sorted(rdd3.groupByKey().collect())

 

The output for this is: 

 

[('bread', <pyspark.resultiterable.ResultIterable object at 0x7f5fcb4c2bd0>), ('brush', <pyspark.resultiterable.ResultIterable object at 0x7f5fcb4c2e50>), ('conditioner', <pyspark.resultiterable.ResultIterable object at 0x7f5fcb4c2f90>), ('jeans', <pyspark.resultiterable.ResultIterable object at 0x7f5fcb4c2d90>), ('meat', <pyspark.resultiterable.ResultIterable object at 0x7f5fcb4c2510>), ('shampoo', <pyspark.resultiterable.ResultIterable object at 0x7f5fcb4c2f10>), ('soap', <pyspark.resultiterable.ResultIterable object at 0x7f5fcb4c2e90>), ('tshirt', <pyspark.resultiterable.ResultIterable object at 0x7f5fcb4c2650>)]

Now, you can turn the results of groupByKey into a list by calling list() on the values instead of rdd3.groupByKey().collect():


sorted(rdd3.groupByKey().map(lambda x : (x[0], list(x[1]))).collect())

The output for this is:

 

[('bread', [2]), ('brush', [2]), ('conditioner', [3]), ('jeans', [2]), ('meat', [2]), ('shampoo', [1, 2]), ('soap', [1, 2]), ('tshirt', [2])]

The groupByKey() involves a lot of shuffling as it does not combine the keys present in the same executor. Let’s look at an example to understand this.

groupByKey() example
groupByKey() example
In the next video, let's look at more operations that are available on paired RDDs.

Let us look at the operations discussed in this video.

mapValues(): This function is used for operating on the value part of the key-value pair. Let’s look at an example.

sales = sc.parallelize([("cosmetics", ["shampoo", "soap", "conditioner", "brush"]), ("food", ["bread", "meat"]), ("clothes", ["tshirt", "jeans"])])
def f(sales): return len(sales)
sales.mapValues(f).collect()

The output will be

[('cosmetics', 4), ('food', 2), ('clothes', 2)]

flatMapValues(): FlatMap "breaks down" collections into the elements of the collection. To understand flatMapValues(), let's look at an example.

sales = sc.parallelize([("cosmetics", ["shampoo", "soap", "conditioner", "brush"]), ("food", ["bread", "meat"]), ("clothes", ["tshirt", "jeans"])])
def f(sales): return sales
sales.flatMapValues(f).collect()
 

The output will be

[('cosmetics', 'shampoo'), ('cosmetics', 'soap'), ('cosmetics', 'conditioner'), ('cosmetics', 'brush'), ('food', 'bread'), ('food', 'meat'), ('clothes', 'tshirt'), ('clothes', 'jeans')]
keys(): The keys() function creates a new RDD that contains only the keys from the paired RDD.

sales_1 = sc.parallelize([("shampoo", 1), ("soap", 1), ("conditioner", 3), ("brush", 2), ("soap", 2), ("shampoo", 2), ("bread", 2), ("meat", 2), ("tshirt", 2), ("jeans", 2)])
k = sales_1.keys();
k.collect()

The output will be

['shampoo', 'soap', 'conditioner', 'brush', 'soap', 'shampoo', 'bread', 'meat', 'tshirt', 'jeans']

By now, you have understood some basic transformation and action operations on paired RDDs. In the upcoming segments, you will learn about various other operators and solve some problem statements using paired RDDs.

Let’s look at each of the operations discussed in the video above.

 

values(): The values() function creates a new RDD that contains only the values from the paired RDD.

 

sales_1 = sc.parallelize([("shampoo", 1), ("soap", 1), ("conditioner", 3), ("brush", 2), ("soap", 2), ("shampoo", 2), ("bread", 2), ("meat", 2), ("tshirt", 2), ("jeans", 2)])
v = sales_1.values() 
v.collect()

The output will be

 

[1, 1, 3, 2, 2, 2, 2, 2, 2, 2]

sortByKey(): This operator is used to sort the elements of a paired RDD. The sorting is done based on the key of the paired RDD.

 

tmp = [('Apple', 12), ('Banana', 11), ('Mango', 14), ('Carrot', 13), ('Orange', 15)]
sc.parallelize(tmp).sortByKey(True, 1).collect()
 

The output will be

 

[('Apple', 12), ('Banana', 11), ('Carrot', 13), ('Mango', 14), ('Orange', 15)]

 

subtractByKey(): Return each (key, value) pair in self that has no pair with matching key in other.

 

x = sc.parallelize([("a", 1), ("b", 4), ("b", 5), ("a", 2)])
y = sc.parallelize([("a", 3), ("c", None)])
sorted(x.subtractByKey(y).collect())

The output will be

 

[('b', 4), ('b', 5)]

join(): Return an RDD containing all pairs of elements with matching keys in self and other. Whenever you do an inner join, the key must be present in both the paired RDDs; however, for an outer join, the key may or may not be present in both the paired RDDs. We will learn more about the inner and outer joins in the upcoming videos.

 

Consider the following example:

 

x = sc.parallelize([('Apple', 50), ('Banana', 100), ('Mango', 150), ('Carrot', 120)])
y = sc.parallelize([('Apple', 100), ('Banana', 120), ('Mango',150)])
sorted(x.join(y).collect())

Now, if you apply the join operation on these two RDDs, the output is another RDD.

 

[('Apple', (50, 100)), ('Banana', (100, 120)), ('Mango', (150, 150))]

rightOuterJoin(): The rightOuterJoin() has the option to skip the key that is present on the left side of the operator; however, all keys that are present on the right side of the operator must be present. Let’s look at an example:

rdd2.rightOuterJoin(rdd1)

 

rdd2 is the operator on the left, and rdd1 is the operator on the right. All keys in the rdd1 must be present in the output. Let's look at an example.

 

rdd1 = sc.parallelize([('Apple', 50), ('Banana', 100), ('Mango', 150), ('Carrot', 120)])
rdd2 = sc.parallelize([('Apple', 100), ('Banana', 120), ('Mango',150)])
sorted(rdd2.rightOuterJoin(rdd1).collect())

The output is

 

[('Apple', (100, 50)), ('Banana', (120, 100)), ('Carrot', (None, 120)), ('Mango', (150, 150))]

leftOuterJoin(): The leftOuterJoin() has the option to skip the key that is present on the right side of the operator; however,all keys that are present on the left side of the operator must be present. Let’s look at an example.

rdd2.leftOuterJoin(rdd1)

 

rdd2 is the operator on the left, and rdd1 is the operator on the right. All keys in the rdd2 must be present in the output. Let’s look at an example.

 

rdd1 = sc.parallelize([('Apple', 50), ('Banana', 100), ('Mango', 150), ('Carrot', 120)])
rdd2 = sc.parallelize([('Apple', 100), ('Banana', 120), ('Mango',150)])
sorted(rdd2.leftOuterJoin(rdd1).collect())
 

The output will be

 

[('Apple', (100, 50)), ('Banana', (120, 100)), ('Mango', (150, 150))]

Now let's understand the cogroup() operator in the upcoming video.

cogroup(): In the case of cogroup(), if the key is present in any one of the RDDs, it will be present in the output. For each key k in self or other, return a resulting RDD that contains a tuple with the list of values for that key in self as well as other.

The following operations were discussed in the previous video:

countByKey(): Counts the number of elements for each key.
lookup(key): Finds all the values associated with the key provided.

![image](https://user-images.githubusercontent.com/20191454/185790765-fa942338-c568-48e6-8353-d70421b77396.png)
![image](https://user-images.githubusercontent.com/20191454/185790802-c35c95f0-eac5-4dfe-b583-48d36883ab07.png)
![image](https://user-images.githubusercontent.com/20191454/185790839-6aff8fd5-5c22-4071-a215-8e0e9ebcf155.png)
![image](https://user-images.githubusercontent.com/20191454/185790858-bc54e0f1-4774-4171-b012-25dfc2fbcb03.png)
![image](https://user-images.githubusercontent.com/20191454/185790870-0d5069fc-0655-4ca1-9c9a-7abd2eb8109c.png)
https://learn.upgrad.com/course/2151/segment/23256/150853/463432/2403235

Session-1

 

“Apache Spark™ is a unified analytics engine for large-scale data processing.’ It is an open-source, distributed computing engine, and it provides a productive environment for data analysis owing to its lightning speed and support for various libraries. 
The in-memory data processing system makes Spark faster than MapReduce.
Spark architecture includes driver nodes and worker nodes. Cluster manager is used to allocate resources to each component of the architecture.
Session-2

 

There are two different operations that can be performed on RDDs: transformation and action. Transformation operations operate on the elements of the RDD and store them in new RDDs as RDDs are immutable. Action operations cause all the transformations to execute and create a particular output.
Lazy Evaluation and the use of DAG execution in Spark make RDDs resilient as transformations are only executed once an action is called.
Session-3

 

Paired RDDs are key/value pairs that can be created from basic RDDs.
Due to the difference in structure, there are various operations associated with paired RDDs.
In the next module, you will learn about Spark Structured APIs. You will be introduced to various dataframe operations that Spark offers for analyzing dataframes which makes it so powerful as well as easy to use.














