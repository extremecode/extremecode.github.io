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
![image](https://user-images.githubusercontent.com/20191454/177025530-dcc94b57-0c37-4dca-8e03-3441ed477140.png)
![image](https://user-images.githubusercontent.com/20191454/177025551-69fbd926-973d-42af-8cd0-643ab66e99e3.png)
mongoimport --db blogs --collection blogs --file "C:\Users\guptaaka\Documents\workspace\MS\SQL\blogs.json"
  
![image](https://user-images.githubusercontent.com/20191454/177026055-af745cf3-3b0a-4a7d-9c70-d7b701e2dca7.png)
![image](https://user-images.githubusercontent.com/20191454/177026072-a4921faf-12af-4b9e-a889-8f8623fcc3db.png)
![image](https://user-images.githubusercontent.com/20191454/177026079-8de2a977-f4fe-4898-8b8a-2fa3406ec821.png)
![image](https://user-images.githubusercontent.com/20191454/177026104-ff3cc525-dc78-46ab-8fc3-fdd707306d95.png)
![image](https://user-images.githubusercontent.com/20191454/177026187-f673b0bd-bfd6-4923-ba02-0290f06ae465.png)
![image](https://user-images.githubusercontent.com/20191454/177026208-ac9cd29d-52c2-4bc1-a9a0-3c39679dbe9d.png)
![image](https://user-images.githubusercontent.com/20191454/177026268-419b53d7-1962-4a85-96c3-47f282fe76a6.png)
![image](https://user-images.githubusercontent.com/20191454/177026287-dd117877-49c5-4220-9ac1-5a45dcf76d06.png)
![image](https://user-images.githubusercontent.com/20191454/177026335-cf96d5ab-bcf2-49c3-8da3-7f8358261799.png)

  ```markdown
  ## Unwind the data
db.purchases2.aggregate([{$unwind:'$Pur_hist'}]).pretty()

## Project only the specific fields 
db.purchases2.aggregate([{$unwind:'$Pur_hist'},{$project:{'Pur_hist.Category':1}}])

## Perform a filter  
db.purchases2.aggregate([{$unwind:'$Pur_hist'},{$project: {'Pur_hist.Category':1}},{$match:{'Pur_hist.Category':'Technology'}}])

## Peform a count operation
db.purchases2.aggregate([{$unwind:'$Pur_hist'},{$project: {'Pur_hist.Category':1}},{$match:{'Pur_hist.Category':'Technology'}},{$group: {_id:null,count:{$sum:1}}}])

## Show the total Sales across each Category and Segment combination
db.purchases2.aggregate( [{$unwind:'$Pur_hist'},{ $group: { _id: { segment: "$Segment", category: "$Pur_hist.Category" }, totalSales: { $sum: "$Pur_hist.Sales" } } }])

db.blogs.aggregate( [{$unwind:'$blogs'}, avgLikes: { $avg: "$blogs.likes" }])

  
## For each segment, show the category having the highest Sales
db.purchases2.aggregate( [{$unwind:'$Pur_hist'},{ $group: { _id: { segment: "$Segment", category: "$Pur_hist.Category" }, totalSales: { $sum: "$Pur_hist.Sales" } } },{$sort:{totalSales: 1}}])
  ```
  
![image](https://user-images.githubusercontent.com/20191454/177026464-100d8163-fa43-4e99-90ad-1c876e3f6b87.png)
![image](https://user-images.githubusercontent.com/20191454/177026488-b47f7991-075f-4cc9-8c01-f22dfbbe312b.png)
![image](https://user-images.githubusercontent.com/20191454/177026605-213d0de3-6152-4c06-889e-6ada8e675252.png)
![image](https://user-images.githubusercontent.com/20191454/177026642-9a1989cc-f0f6-4b72-aeeb-6e6ec500751f.png)
![image](https://user-images.githubusercontent.com/20191454/177026934-13f336f8-a55f-4f81-b760-756d6eda1941.png)
![image](https://user-images.githubusercontent.com/20191454/177026939-7deb309f-7d61-49cc-aba4-76fae0d00753.png)
![image](https://user-images.githubusercontent.com/20191454/177027795-23789dfb-37e2-400d-96a9-85367298a778.png)
![image](https://user-images.githubusercontent.com/20191454/177027808-a92fe01c-e6d6-400f-b19e-1a0977e11f30.png)
https://docs.mongodb.com/manual/core/replica-set-elections/
  ![image](https://user-images.githubusercontent.com/20191454/177027832-6b7ea768-a72a-4aa4-83dd-d47f387c52bb.png)
![image](https://user-images.githubusercontent.com/20191454/177027851-43d3d247-08aa-4a29-9a07-3a8cf425bd86.png)
![image](https://user-images.githubusercontent.com/20191454/177027909-a4fec85d-d24e-476c-b557-b70403b76729.png)
![image](https://user-images.githubusercontent.com/20191454/177028087-3a01a86e-b458-4227-b8eb-908c63d1ba9c.png)
![image](https://user-images.githubusercontent.com/20191454/177028100-b171be41-8012-4ab6-81a7-938affe3d404.png)
![image](https://user-images.githubusercontent.com/20191454/177028276-3ac0a0d8-012d-4a32-aee6-0be5ca89ccca.png)

  https://www.techtarget.com/searchdatamanagement/definition/hashing
  https://www.mongodb.com/docs/manual/core/index-hashed/#:~:text=MongoDB%20hashed%20indexes%20truncate%20floating,2.3%20%2C%202.2%20%2C%20and%202.9%20.
  
  ![image](https://user-images.githubusercontent.com/20191454/177028315-861321d9-a53f-4704-992d-3dc76158447c.png)
![image](https://user-images.githubusercontent.com/20191454/177028323-0b645452-416f-48f1-a3e7-99e420f14afe.png)
![image](https://user-images.githubusercontent.com/20191454/177028335-cc1f91d4-d119-4f19-8255-2ea975499c91.png)
![image](https://user-images.githubusercontent.com/20191454/177028342-91dd4a2c-f4bd-4039-be8e-bc82a0322db1.png)

  
  
  
  
  
  
  
  
  
  
  
  

  
  


  
  
  
