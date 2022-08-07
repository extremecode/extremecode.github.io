# HiveSQL

![image](https://user-images.githubusercontent.com/20191454/183276204-e233bf48-6b50-4caf-921f-977d625ca99a.png)
![image](https://user-images.githubusercontent.com/20191454/183276521-4ae94fd7-0527-4d05-8de7-758cedfadfd1.png)

![image](https://user-images.githubusercontent.com/20191454/183276601-e8b076e6-2e02-49f7-9cf4-457780d4b0a1.png)
create table if not exists user_info (id int, age int, gender string, profession string, review int) row format delimited fields terminated by '|' lines terminated by '\n' stored as textfile ;
load data local inpath '/home/hadoop/u.user' into table user_info ;

ext table data
create external table if not exists user_info_external (id int, age int, gender string, profession string, review int) row format delimited fields terminated by '|' lines terminated by '\n' stored as textfile ;
load data local inpath '/home/hadoop/u.user' into table user_info_external ;

create table if not exists male_users (id int, gender string, job string) ;
create table if not exists female_users (id int, gender string, job string) ;

from user_info insert into table male_users select id, gender, profession where gender = 'M' insert into table female_users select id, gender, profession where gender = 'F' ;

alter table male_users add columns ( name string ) ;

alter table male_users change gender gender string after name;

![image](https://user-images.githubusercontent.com/20191454/183277309-e7b5e6c9-12d2-4670-9a86-2f823441dc35.png)
![image](https://user-images.githubusercontent.com/20191454/183277313-09490f1f-dc1b-41e3-acd2-60c781e356d2.png)
![image](https://user-images.githubusercontent.com/20191454/183277324-2996d4a7-d3ff-4b18-9dbc-e31e698e44b9.png)
![image](https://user-images.githubusercontent.com/20191454/183277337-a5b3b66d-d256-44f1-a168-18b844d24b47.png)
set hive.cli.print.header = true ;

select id, profession, age from user_info order by age limit 10 ;

So, we have executed the same query with the 'SORT BY' clause on the age column. As you may have noticed in the video, two reducers are used to sort the data. Each mapper will get the data and sort it at the reducer level.
When you run the below query, you will get the sorted data but at the reducer level only.

select id, age, gender, profession from user_info sort by age limit 25 ;
 
 ![image](https://user-images.githubusercontent.com/20191454/183277458-11c6665c-1890-42ce-b767-2361324d3e0a.png)

 https://www.revisitclass.com/hadoop/how-to-set-the-different-execution-engine-in-hive-with-examples/
 ![image](https://user-images.githubusercontent.com/20191454/183277561-2f4c044f-14a2-44a5-a7ab-bbb5eb6dee55.png)

The SORT BY clause may use multiple reducers but does not guarantee the sorting of the total data. Whereas, the ORDER BY clause uses single reducers and guarantees the sorting of the total data.

![image](https://user-images.githubusercontent.com/20191454/183277635-e8489a43-1ce0-42a2-9ffe-a2b777307186.png)

https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jarGuide.html
https://docs.oracle.com/javase/7/docs/api/java/nio/file/attribute/UserDefinedFileAttributeView.html

![image](https://user-images.githubusercontent.com/20191454/183278145-147d2e3c-7c56-43ff-9a1b-e0ee4056e449.png)
![image](https://user-images.githubusercontent.com/20191454/183278151-118c934f-afa2-4777-9af6-52f88b51751b.png)
http://brainbloggerblog.blogspot.com/2017/08/in-hive-index-is-table-which-is.html
![image](https://user-images.githubusercontent.com/20191454/183278190-a616f7fd-8037-4fff-9fc0-fac6a14be95c.png)
![image](https://user-images.githubusercontent.com/20191454/183278272-e1384477-00ae-4b11-bf07-9b21cb657063.png)

create index i2 on table user_info(profession) as 'COMPACT' with deferred rebuild stored as rcfile ;
alter index i2 on user_info rebuild ; 

drop index i1 on user_info ;
https://cwiki.apache.org/confluence/display/Hive/LanguageManual+Indexing
https://issues.apache.org/jira/browse/HIVE-18448










 
