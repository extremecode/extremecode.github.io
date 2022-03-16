
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


usecases
* create a array of 55 ones - np.ones(55) , multi np.ones((2,2)) similary zeros
* create a array equidistant - np.arange(start,end,step_size) end is excluded
* np.random.randint(start_range,end_range,size) size no of elements to generate ,multi np.random.random([2,2]) np.random.randint(1,10,[2,2])
* np.linspace - splite a given start and end range into equalt segments np.linspace(1,10,20,endpoint=True) endpoint = True means inclusive.
* np.hstack - horizontal stacking of arrays np.hstack([np.array([1,2]),np.array([3,4])]) - [1,2,3,4]
* np.vstack - vertical stacking of arrays np.vstack([np.array([1,2]),np.array([3,4])]) - [[1,2],[3,4]]
* np.reshape - reshape an array - np.reshape(np.arange(10),(1,2,5)) - [[[0,1,2,3,4],[5,6,7,8,9]]]
* np.log, - transfromation function power etc
* np.empty - use to create empty array and populate later.y = np.empty(4) np.multiply(arr,2,out=y) print(y)
* 
