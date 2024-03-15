## Lab Overview And High Level Design

In this section of the project I'm going to create a test event and verify if the Lambda function is actually making the calls to News API
and storing the results on Dynamo DB.

## Cofiguring Timeout on Lambda

First, I open the AWS consol and look for Lambda, on the lambda Console I click on the function NewsReaderAPI
the lambda code source open. 
* Now, i procedd to change the Lambda function Timeout
* Go to configurations and select edit
  
<img src="https://github.com/OscarSLopez09/Serverless-Testing-Part1/blob/main/Images/testingpart100.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>

* On basic settings I'm going to Timeout and change the time to 2 minutes
* On execution role, select Use an existing role - DynamoDB_Comprehend
* Click save
<img src="https://github.com/OscarSLopez09/Serverless-Testing-Part1/blob/main/Images/testingpart101.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>

By default, Lambda Timeout is 3 seconds and is going to time out the function before stops running
so, I change the timeout to allow time for the function to run properly.

<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>

## Test Event

* On the lambda code source, click on test
<img src="https://github.com/OscarSLopez09/Serverless-Testing-Part1/blob/main/Images/testingpart02.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>

* Go back to the Test section and create a test event -Even1
* Event JSON section type - {"action":"insert news"}
* Click on save
<img src="https://github.com/OscarSLopez09/Serverless-Testing-Part1/blob/main/Images/testingpart103.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>

* Click on Test
<img src="https://github.com/OscarSLopez09/Serverless-Testing-Part1/blob/main/Images/testingpart104.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>

* After the Executing function succeeded - click on details
* Verify the results on the section below
* Go to the AWS DynanoDB console and select the table - news
* Click on the refresh to check the results
* The Sentiment with the news are being store







