## Lab Overview And High Level Design

An Amazon API Gateway is a collection of resources and methods. For this project, you create one resource (NewsReaderAPI) and define one method (POST) on it. The method is backed by a Lambda function (NewsReaderBacked). That is, when you call the API through an HTTPS endpoint, Amazon API Gateway invokes the Lambda function.

The POST method on the DynamoDBManager resource supports the following DynamoDB operations:

* Create, update, and delete an item.
* Read an item.
* Scan an item.









