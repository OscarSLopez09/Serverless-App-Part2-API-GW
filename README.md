## Lab Overview And High Level Design

<img src="https://github.com/OscarSLopez09/Serverless-App-Part2-API-GW/blob/main/Images/Capture.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>

An Amazon API Gateway is a collection of resources and methods. For this section of the project, you create one resource (NewsReaderAPI) and define one method (POST) on it. The method is backed by a Lambda function (NewsReaderBacked). That is, when you call the API through an HTTPS endpoint, Amazon API Gateway invokes the Lambda function.

The POST method on the DynamoDBManager resource supports the following DynamoDB operations:

* Create, update, and delete an item.
* Read an item.
* Scan an item.











