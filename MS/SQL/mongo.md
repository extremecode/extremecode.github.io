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
  
 Embedded Documents
  Reference Documents
![image](https://user-images.githubusercontent.com/20191454/177022239-f502a41c-3cc0-4e88-8ebd-6bc201cbe26f.png)
![image](https://user-images.githubusercontent.com/20191454/177022244-59fcccc4-b7f1-4037-8e1e-47878c9e89d4.png)
![image](https://user-images.githubusercontent.com/20191454/177022247-5b01f8d3-672b-4860-afcb-4f0aa7219716.png)
![image](https://user-images.githubusercontent.com/20191454/177022264-704de52a-9743-401a-85a3-0fa1c75282bb.png)
![image](https://user-images.githubusercontent.com/20191454/177022271-e896e2cc-2001-44c4-b40c-190e303f4f45.png)
![image](https://user-images.githubusercontent.com/20191454/177022321-eaa33eb0-6f9a-49be-8173-617abc68b69e.png)
![image](https://user-images.githubusercontent.com/20191454/177022333-fa218959-17a4-4bf9-b174-c74331ac4cf9.png)
https://www.mongodb.com/docs/manual/reference/operator/aggregation/lookup/

 ![image](https://user-images.githubusercontent.com/20191454/177022532-f38e4199-77f4-4406-a620-0bb245c7c9c3.png)
  ![image](https://user-images.githubusercontent.com/20191454/177022556-6361fc4a-0c1c-48cf-9047-92b45aea09a5.png)
![image](https://user-images.githubusercontent.com/20191454/177022558-2a5fca28-057f-4095-be4f-7b596b7d20d5.png)
https://docs.mongodb.com/manual/tutorial/model-embedded-one-to-many-relationships-between-documents/

  
  ![image](https://user-images.githubusercontent.com/20191454/177022836-ff78cd41-8a31-4653-baca-2209d0326c70.png)
![image](https://user-images.githubusercontent.com/20191454/177022635-de68a956-d6d5-4881-be04-65e1654882f3.png)
![image](https://user-images.githubusercontent.com/20191454/177022703-e003b23a-b6fd-4a60-8029-c15020321955.png)
![image](https://user-images.githubusercontent.com/20191454/177022725-914db0e5-2fd3-45a2-b3e1-1eeccb474615.png)
![image](https://user-images.githubusercontent.com/20191454/177022780-2dcd4566-3707-4fe3-b819-b4914a2e7d13.png)

 ![image](https://user-images.githubusercontent.com/20191454/177022822-b440ea69-79bc-404b-926f-30afcfbba79a.png)
  ![image](https://user-images.githubusercontent.com/20191454/177022886-98bf325a-ab87-47fb-b2d9-c31131b09aed.png)


  
  ![image](https://user-images.githubusercontent.com/20191454/177022894-3ebfc8e8-ad37-42bb-a23f-9d71b6cfdfdd.png)
![image](https://user-images.githubusercontent.com/20191454/177022935-63f20cf3-a5e5-491d-a723-4bc2ad7f4374.png)
![image](https://user-images.githubusercontent.com/20191454/177024978-67a5387d-d8b1-43a4-aa77-6a0f055cddaf.png)
![image](https://user-images.githubusercontent.com/20191454/177025091-2484bfa3-149f-415f-8723-e10052c2c287.png)
![image](https://user-images.githubusercontent.com/20191454/177025140-59a0be7e-17ff-4458-9c73-76600cb387c0.png)
![image](https://user-images.githubusercontent.com/20191454/177025205-337b5ad7-d8fa-4a0d-9171-c8040379d058.png)
![image](https://user-images.githubusercontent.com/20191454/177025260-139e63a0-a478-40ab-8f61-9a50250bd4ae.png)
![image](https://user-images.githubusercontent.com/20191454/177025437-3f09014d-0199-4057-9d1f-2fb814b84ff5.png)
![image](https://user-images.githubusercontent.com/20191454/177025445-17050520-a8ac-4331-aae5-3cc6a9995d93.png)
![image](https://user-images.githubusercontent.com/20191454/177025471-b36dd64c-637c-4ff0-85d5-6429ca442f43.png)
![image](https://user-images.githubusercontent.com/20191454/177025483-751c44cf-c892-48de-b26e-31ca76e10a33.png)

  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  

  
  


  
  
  
