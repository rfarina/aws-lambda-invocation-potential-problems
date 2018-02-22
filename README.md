# aws-lambda-invocation-potential-problems


#### This video shows how the AWS Lambda incoming event and outgoing response is handled differently based on how it was invoked; for example via the API Gateway, the JavaScript Browser SDK, or the AWS CLI. It also asks whether this is expected behavior, or something that AWS would consider as something it needs to address.

##### To use this application you will need to:
1. create a DynamoDB table named "orders-geodata" with a Primary partition key of "orderid" and Primary sort key of "transtimestamp". Add at least the "lat" and "lon" attributes to the table.
2. create a lambda function named "orders-geodata-read" using the "orders-geodata-read.js" file in this repo as the code base.
3. create an API Gateway api that uses Lambda Proxy Integration to communicate with the orders-geodata-read Lambda function
4. deploy your api to generate the API Gateway endpoint for the HTTP_POST method
5. modify the $.ajax call in index.html to use the api endpoint created in step 4.
6. modify the js/config.js file to use your "accessKeyId", "secretAccessKey", and "region" credentials

There is also a corresponding youTube video that provides a full description of this code and the potential problems related to lambda invocations. It can be viewed here https://youtu.be/GfQX36KPrq8


