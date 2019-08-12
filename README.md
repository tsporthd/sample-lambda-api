# sample-lambda-api
Sample Lambda API which uses nodejs, apigateway and dynamodb

Steps to use

1. Setup local AWS configuration such that aws cli works
2. npm install serverless -g 
3. Optional setup alias #alias sls='serverless' in your .bashrc or .bash_profile
4. clone this repo and cd to sample-lambda-api
5. run npm install 
5. run - serverless or sls deploy
```{r chunk-name-with-no-spaces}
Output of serverless deploy should be something like
sls deploy
Serverless: Packaging service...
Serverless: Excluding development dependencies...
Serverless: Uploading CloudFormation file to S3...
Serverless: Uploading artifacts...
Serverless: Uploading service candidate-service.zip file to S3 (208.45 KB)...
Serverless: Validating template...
Serverless: Updating Stack...
Serverless: Checking Stack update progress...
..........................
Serverless: Stack update finished...
Service Information
service: candidate-service
stage: dev
region: us-east-1
stack: candidate-service-dev
resources: 22
api keys:
  None
endpoints:
  GET - https://l9gi451txb.execute-api.us-east-1.amazonaws.com/dev/candidates
  GET - https://l9gi451txb.execute-api.us-east-1.amazonaws.com/dev/candidates/{id}
  POST - https://l9gi451txb.execute-api.us-east-1.amazonaws.com/dev/candidates
functions:
  listCandidates: candidate-service-dev-listCandidates
  candidateDetails: candidate-service-dev-candidateDetails
  candidateSubmission: candidate-service-dev-candidateSubmission
layers:
  None
Serverless: Removing old service artifacts from S3...
Serverless: Run the "serverless" command to setup monitoring, troubleshooting and testing.
```

You can refer to testing this once deployed by looking at original authors link here https://serverless.com/blog/node-rest-api-with-serverless-lambda-and-dynamodb/ 

