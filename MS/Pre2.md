
![image](https://user-images.githubusercontent.com/20191454/158605420-83f1f370-5f74-4a4c-a523-b49bbd116cf7.png)

![image](https://user-images.githubusercontent.com/20191454/158605763-2f7b5fa8-89c3-42fa-99d8-e9fbcd43ab4d.png)

![image](https://user-images.githubusercontent.com/20191454/158605994-68d90112-3a7d-4898-910f-63892dee92dd.png)

![image](https://user-images.githubusercontent.com/20191454/158607272-7132760d-13da-4f48-b153-0128fa3155e5.png)

![image](https://user-images.githubusercontent.com/20191454/158607835-a0e56288-6165-45e0-bf2d-d459f98dfcae.png)

![image](https://user-images.githubusercontent.com/20191454/158609316-a26adc7e-cfea-4864-b1fc-683ce7c7068e.png)

![image](https://user-images.githubusercontent.com/20191454/158609435-24e07a1b-5977-4b93-80cb-70d31cc246e2.png)

![image](https://user-images.githubusercontent.com/20191454/158610097-434dc7cc-cde6-474f-b437-6f31cb8b9bbe.png)

![image](https://user-images.githubusercontent.com/20191454/158611020-df69e0d4-eccc-4655-8fcc-12e03a2babe4.png)

![image](https://user-images.githubusercontent.com/20191454/158611469-ff08925d-071b-4a7d-9444-b60b0845a011.png)

![image](https://user-images.githubusercontent.com/20191454/158615737-d758dd0d-e662-4032-83fc-9cad35b61206.png)

![image](https://user-images.githubusercontent.com/20191454/158768524-511af687-433c-4101-b86a-5a5344eca99d.png)

![image](https://user-images.githubusercontent.com/20191454/158769317-5b0463ce-71f4-492f-9a57-b13e02edf6e2.png)

![image](https://user-images.githubusercontent.com/20191454/158769875-f14a5934-713d-4eec-99ee-50771499b240.png)

![image](https://user-images.githubusercontent.com/20191454/158770202-32036bdf-6734-426b-a8f8-bee83a3a283b.png)

![image](https://user-images.githubusercontent.com/20191454/159044727-c0eae57b-e4f9-4149-8fc7-11b9a0714872.png)

![image](https://user-images.githubusercontent.com/20191454/159046067-a549db3c-4db0-48eb-8a15-165c8cc8346f.png)

![image](https://user-images.githubusercontent.com/20191454/159046171-398973e8-2294-425f-9305-86790e92fa08.png)

![image](https://user-images.githubusercontent.com/20191454/159046682-93c57f31-1d45-47db-b794-0ede187a0105.png)

![image](https://user-images.githubusercontent.com/20191454/159047891-2a0f8672-8876-4b6e-971d-1bb06c03be25.png)

![image](https://user-images.githubusercontent.com/20191454/159048576-eb3da932-c86d-4b8f-87d1-ff81a8e5247b.png)
![image](https://user-images.githubusercontent.com/20191454/159048956-03cd525b-beef-4a54-b272-df24c104edc7.png)
![image](https://user-images.githubusercontent.com/20191454/159049593-329521ba-3110-4189-b555-c4d83e7ae4eb.png)
![image](https://user-images.githubusercontent.com/20191454/159050012-92a1304e-56b8-48da-ab98-65c108e83ec4.png)
![image](https://user-images.githubusercontent.com/20191454/159050448-681a329f-b001-419e-a8ad-cbebe618f3ee.png)
![image](https://user-images.githubusercontent.com/20191454/159051917-3acb2ccc-35c3-4c5c-a759-0a40eca6ce7e.png)
![image](https://user-images.githubusercontent.com/20191454/159055014-cb13aea1-9caf-484b-b0ce-93371f2df024.png)
![image](https://user-images.githubusercontent.com/20191454/159055142-231aecbb-194e-4745-ae88-c986ed1f750f.png)
![image](https://user-images.githubusercontent.com/20191454/159055264-6a4bdd6a-677a-4407-b816-b31e9c590906.png)
![image](https://user-images.githubusercontent.com/20191454/159056292-e77af17d-a2d4-4f3a-ac23-8fc215bf5180.png)
![image](https://user-images.githubusercontent.com/20191454/159056949-a622f553-aa28-4cd3-8241-3b63327d4582.png)
![image](https://user-images.githubusercontent.com/20191454/159057867-b446afbe-3783-4184-8bea-ead3f52fa48b.png)

#### Numpy usecases
* create a array of 55 ones - np.ones(55) , multi np.ones((2,2)) similary zeros
* create a array equidistant - np.arange(start,end,step_size) end is excluded
* np.random.randint(start_range,end_range,size) size no of elements to generate ,multi np.random.random([2,2]) np.random.randint(1,10,[2,2])
* np.linspace - splite a given start and end range into equalt segments np.linspace(1,10,20,endpoint=True) endpoint = True means inclusive.
* np.hstack - horizontal stacking of arrays np.hstack([np.array([1,2]),np.array([3,4])]) - [1,2,3,4]
* np.vstack - vertical stacking of arrays np.vstack([np.array([1,2]),np.array([3,4])]) - [[1,2],[3,4]]
* np.reshape - reshape an array - np.reshape(np.arange(10),(1,2,5)) - [[[0,1,2,3,4],[5,6,7,8,9]]]
* np.log, - transfromation function power etc
* np.empty - use to create empty array and populate later.y = np.empty(4) np.multiply(arr,2,out=y) print(y)
* reduce function - to reduce to a single value - np.add.reuduce(np.arange(10)) - 45 - 0+...+9 = 45
* accumulate - to apply as  commulative function sequentially - np.add.accumulate(np.arange(10)) - array([ 0,  1,  3,  6, 10, 15, 21, 28, 36, 45], dtype=int32)
#### Pandas Usecases-
* load in tabular format dict,json,csv,excel - we will create a data frame pd.DataFrame({'name':["akash","vikash"],'age':[24,25]}) - 
* read a csv - pd.read_csv(filepath)
* rename header/add/override headers - df.columns = ['Track Name','Artist Name','Genre','Beats Per Minute']
* index a column - for columns - pd.read_csv(filepath,index_col=[col_no list]) for multiple - df.set_index(["Track Name","Genre"])
* describe data - print top n rows - df.head(no) default 5, print last n rows df.tail(no) default -5 ,  df.info() - get type of col,non null val count etc, df.describe() - give detail mean,stddev,min,max,quantiles values of numeric,float columns, for categarical - count,uniq,top,freq
* slicing and index of data - select a range for a index col - df = pd.read_csv("top50.csv",index_col=[1]) , df['canadian pop':'dance pop'], selecting single column - df[column name].head(), selecting multiple columns df[["col1","col2"]].head() 
* row indexing - to locate rows - df.loc[["canadian pop","reggaeton flow"]] 
* column indexing  - to select filtered columns - df.loc[:,["Track Name","Artist Name"]]
* access rows and columns using index no - df.iloc[1,2] row 1 column 2 value for multiple - df.iloc[[0,1],[1,2]], for a range - df.iloc[1:13,1:4]
* filtering data based on a criteria/slice - filter by column value -  df[df["Track Name"]=="Señorita"] , contains - df[df["Track Name"].isin(["China"])], multiple criteria - df[df["Track Name"].isin(["China"]) & (df["Energy"]=="81")] = df[(crtiteria 1) & (criteria 2) and so on]
* handling time series data - pd.DatetimeIndex(df["col"]).(year/day/month)
* create a custom column - df["newcol"] = df["col"]*2 or using apply df["columns"].apply(lambda expression) - df["Energy"].apply(lambda x: "fifty five" if x == "55" else "not fifty five" )
* groupby and aggregation = df.groupby(by="column name").aggregation_Func().head() 
* merge two dataframe- df1.merge(df2,on="common column name",how=(left,right,inner,outer)) - left - from first df all rows , right - from secondf df all rows, outer - union on df1,df2, , inner - intersection of df1,df2
* create a agg table - comaring index and a range of columns - df.pivot_table(index="Track Name",columns="Energy",values="Liveness",aggfunc="count").head()

![image](https://user-images.githubusercontent.com/20191454/159105658-b3ef6fa7-8b0b-4c6c-8836-e8a4fb984b1e.png
![image](https://user-images.githubusercontent.com/20191454/159107441-685fa48d-d00f-4345-b7ac-43c88f7607b4.png)
#### Data Visualization usecases -
* [Bar chart -
```markdown
product_cateogary= np.array(["Furntitue","Technology","Office Supplier"]) product_sales= np.array([1000.11,2002,1500]) plt.bar(product_cateogary,product_sales)plt.show()
```
](./comparision/among-items/one-variable-per-item/few-catrogaries/many-items)
* [Columns chart](./comparision/among-items/one-variable-per-item/few-catrogaries/few-items)








