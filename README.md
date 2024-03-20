## Lab Overview And High Level Design

<img src="https://github.com/OscarSLopez09/Serverless-App-Part2-API-GW/blob/main/Images/Capture.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>

In this section of the project I'm going to create the API Gateway that is going to make calls to my backend lambda function (NewsReaderBacked), subsequently is going to Dynamo DB to fetch the sentiment with the news.

You are in Part3 of the project, links to the other sections:

- [Part 1 Lambda Serverless App ](https://github.com/OscarSLopez09/Lambda-Serverless-App)
- [Part 2 Testing the first part ](https://github.com/OscarSLopez09/Serverless-Testing-Part1)
- [Part 3 Creating the backend lambda](https://github.com/OscarSLopez09/Lambda-Serverless-App-Part2)
- [Part 4 Creating CloudWatch event](https://github.com/OscarSLopez09/Serverless-Cloudwatch-Rule)
- [Part 5 Implementing security with API keys ](https://github.com/OscarSLopez09/Lambda-Serverless-App-Security)

An Amazon API Gateway is a collection of resources and methods. For this section of the project, you create one resource (NewsReaderAPI) and define one method (POST) on it. The method is backed by a Lambda function (NewsReaderBacked). That is, when you call the API through an HTTPS endpoint, Amazon API Gateway invokes the Lambda function.

* On AWS console search box type API Gateway to access the API service.
<img src="https://github.com/OscarSLopez09/Serverless-App-Part2-API-GW/blob/main/Images/api00.PNG" height="90%" width="90%" alt="Disk Sanitization Steps"/>

* Select API type - Rest API and click on build
<img src="https://github.com/OscarSLopez09/Serverless-App-Part2-API-GW/blob/main/Images/api01.PNG" height="90%" width="90%" alt="Disk Sanitization Steps"/>

* On API details select - New API
* API name - NewsReaderAPI 
* API endpoint type - Regional
* Click Create API
<img src="https://github.com/OscarSLopez09/Serverless-App-Part2-API-GW/blob/main/Images/api02.PNG" height="90%" width="90%" alt="Disk Sanitization Steps"/>

* Click on Create resource
<img src="https://github.com/OscarSLopez09/Serverless-App-Part2-API-GW/blob/main/Images/api03.PNG" height="90%" width="90%" alt="Disk Sanitization Steps"/>

* Resource details open create a Resource name - NewsReaderAPI
* Click on Create resource
<img src="https://github.com/OscarSLopez09/Serverless-App-Part2-API-GW/blob/main/Images/api04.PNG" height="90%" width="90%" alt="Disk Sanitization Steps"/>

* Click on Create method
<img src="https://github.com/OscarSLopez09/Serverless-App-Part2-API-GW/blob/main/Images/api05.PNG" height="90%" width="90%" alt="Disk Sanitization Steps"/>

* Method details select - Method type POST
* Integration type - Lambda function
* Lambda function, select - NewsReaderBacked (Backend function)
* Click on Create method
<img src="https://github.com/OscarSLopez09/Serverless-App-Part2-API-GW/blob/main/Images/api06.PNG" height="90%" width="90%" alt="Disk Sanitization Steps"/>

* Scroll down and select the Test tab
<img src="https://github.com/OscarSLopez09/Serverless-App-Part2-API-GW/blob/main/Images/api07.PNG" height="90%" width="90%" alt="Disk Sanitization Steps"/>

* Scroll down to Request body and type:
```json
{
  "sentiment":"NEGATIVE"
}
```
* Click on Test
<img src="https://github.com/OscarSLopez09/Serverless-App-Part2-API-GW/blob/main/Images/api08.PNG" height="90%" width="90%" alt="Disk Sanitization Steps"/>

* The test POST method result is successfull (Status code: 200)
<img src="https://github.com/OscarSLopez09/Serverless-App-Part2-API-GW/blob/main/Images/api09.PNG" height="90%" width="90%" alt="Disk Sanitization Steps"/>

* Click on Deploy API to deploy it.
<img src="https://github.com/OscarSLopez09/Serverless-App-Part2-API-GW/blob/main/Images/api10.PNG" height="90%" width="90%" alt="Disk Sanitization Steps"/>

* Deploy API select stage
* New stage  
* Stage name - Dev
* Click on Deploy to deploy the stage
<img src="https://github.com/OscarSLopez09/Serverless-App-Part2-API-GW/blob/main/Images/api11.PNG" height="90%" width="90%" alt="Disk Sanitization Steps"/>

* Check the stage by clicking on the Dev /NewsReaderAPI /Post
* Shows you the Invoke URL, click on the invoke URL to copy
<img src="https://github.com/OscarSLopez09/Serverless-App-Part2-API-GW/blob/main/Images/api12.PNG" height="90%" width="90%" alt="Disk Sanitization Steps"/>

## Testing the API Gateway by going to Postman app.

* On Postman click on the method drop-down menu and select POST
<img src="https://github.com/OscarSLopez09/Serverless-App-Part2-API-GW/blob/main/Images/api13.PNG" height="90%" width="90%" alt="Disk Sanitization Steps"/>

* On the Enter URL box, paste the invoke URL 
<img src="https://github.com/OscarSLopez09/Serverless-App-Part2-API-GW/blob/main/Images/api14.PNG" height="90%" width="90%" alt="Disk Sanitization Steps"/>

* Click on Body and click on raw
* Type the JSON test code:
  
```json
{
    "sentiment":"NEGATIVE"
}
```

* Click on the Send button
<img src="https://github.com/OscarSLopez09/Serverless-App-Part2-API-GW/blob/main/Images/api15.PNG" height="100%" width="100%" alt="Disk Sanitization Steps"/>

## We get a successful response!
<img src="https://github.com/OscarSLopez09/Serverless-App-Part2-API-GW/blob/main/Images/api16.PNG" height="90%" width="90%" alt="Disk Sanitization Steps"/>

Link to part 4 of the project:

- [Part 4 Creating CloudWatch event](https://github.com/OscarSLopez09/Serverless-Cloudwatch-Rule)
 



















