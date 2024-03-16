## Lab Overview And High Level Design

<img src="https://github.com/OscarSLopez09/Serverless-App-Part2-API-GW/blob/main/Images/Capture.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>

In this section of the project I'm going to create the API Gateway that is going to make calls to my backend lambda function (NewsReaderBacked), subsequently is going to Dynamo DB to fetch the sentiment with the news.

An Amazon API Gateway is a collection of resources and methods. For this section of the project, you create one resource (NewsReaderAPI) and define one method (POST) on it. The method is backed by a Lambda function (NewsReaderBacked). That is, when you call the API through an HTTPS endpoint, Amazon API Gateway invokes the Lambda function.














