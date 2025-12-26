### List all Lambda functions
awslocal lambda list-functions

### Deploy a new Lambda function
First zip the function `zip function.zip index.js`

Deploy it using awslocal
```
awslocal lambda create-function \
--function-name hello-world \
--runtime nodejs18.x \
--handler index.handler \
--zip-file fileb://function.zip \
--role arn:aws:iam::000000000000:role/lambda-role
```

### Invoke the Lambda function
`awslocal lambda invoke --function-name hello-world /dev/stdout`

### Update the Lambda function code
First zip the updated function `zip function.zip index.js`
```
awslocal lambda update-function-code \
--function-name hello-world \
--zip-file fileb://function.zip
```
### Delete the Lambda function
`awslocal lambda delete-function --function-name hello-world`

### PYTHONNNNNNN
```
awslocal lambda create-function \
--function-name hello-world-python \
--runtime python3.11 \
--handler index.handler \
--zip-file fileb://function.zip \
--role arn:aws:iam::000000000000:role/lambda-role
```
