# AWS-Lamda

- Setup 
```
npm install -g serverless
serverless create -t aws-nodejs
serverless config credentials --provider aws --key fakekey --secret fake
serverless deploy --stage prodcution
serverless deploy

```


- YAML Config 
```
service: testLambda

provider:
  name: aws
  runtime: nodejs8.10

functions:
  create:
    handler: handler.createUser
    events:
     - http:
         path: users/create
         method: get
  getUser:
      handler: handler.getUser
      events:
      - http:
          path: user/get
          method: get

````
