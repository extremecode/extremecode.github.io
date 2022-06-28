![image](https://user-images.githubusercontent.com/20191454/175806389-9bb604dc-1005-4750-b138-4185d0a6580d.png)
![image](https://user-images.githubusercontent.com/20191454/175806436-747f0af2-5885-48e0-8c13-d943dd646218.png)
![image](https://user-images.githubusercontent.com/20191454/175806607-07564e6b-cf65-4e21-bfbc-ae46c749cc83.png)
![image](https://user-images.githubusercontent.com/20191454/175806618-6461184b-ef9a-40d3-9a8c-9ea29b9293ad.png)
![image](https://user-images.githubusercontent.com/20191454/175806678-f4f8d464-312d-426f-99fb-94f4f574e0e8.png)
![image](https://user-images.githubusercontent.com/20191454/175806719-43b2c32b-692a-44d4-a556-39de4766b159.png)
![image](https://user-images.githubusercontent.com/20191454/175806938-749cdf90-bb89-4524-b7b2-7f6f4a9197eb.png)
![image](https://user-images.githubusercontent.com/20191454/175807444-51c7cdd7-ebed-406f-af89-441d4ed685da.png)
![image](https://user-images.githubusercontent.com/20191454/175807463-d066cbba-a4eb-43c4-b822-4ab1639401e1.png)
![image](https://user-images.githubusercontent.com/20191454/175807468-dcf8e0e8-97e0-4e75-9385-3566b1ff2a1f.png)

mongoimport --db <database name> --collection <collection name> --type csv --file <filepath> --headerline
![image](https://user-images.githubusercontent.com/20191454/176003366-5758a9bf-0a3a-4606-b77c-0452d51520ef.png)
db.collection.find({$and: [{field : {condition 1}},{field : {condition 2}}...]})
db.collection.find({$or: [{field: {condition 1}},{field : {condition 2}}...]})
db.collection.find({ field: { $not: {condition} } })
  db.collection.find({"field": {$regex: <pattern>}})


db.purchases.find({'Order ID': {$regex: /^IN/}}).count()

  
 
  
  db.Collection.aggregate([{stage1},{stage2},{stage3}....])
https://docs.mongodb.com/manual/reference/operator/aggregation-pipeline/
 db.purchases.aggregate([{$group:{_id:null, total: {$sum: '$Sales'}}}]) 
db.purchases.aggregate([{$group:{_id:'$Segment',average:{$avg:'$Sales'}}}])
