Spotify API - Provided by Spotify to extract data from it. We register our app on Spotify and get the client id and the secret id. 

Spotify package is used to collect the data from Spotify API. 

Lambda - Code is deployed on this. It's a server less compute service which is AWS managed. It's scalable. 

Amazon CloudWatch (daily trigger) -  Scheduling part can be done here which will run our code on Lambda. 

S3 - scalable Object storage service allows storing & retrieval of different types of files of any size. This will store our data extracted from Spotify. As soon as data is stored in S3, it will trigger the transformation code stored on Lambda and after transformation data will be stored on S3. 

Both extract and transform part of automated. 

Glue Crawler - It will infer schema. It goes through each file and understand how many column file has. What are the different column names and data type it has. This will build a glue catalog which will store the information about the data.

Athena - Run sql service to analyze the data

Spotify API  has 3 things - Music Artist, Album and Track. 

Architecture - 

![image](https://github.com/user-attachments/assets/1587bc2a-41a9-4f89-846d-2f07b806c0d5)


