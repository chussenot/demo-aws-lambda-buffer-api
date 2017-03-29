Build a serverless API Buffer with AWS Lambda, API Gateway services, Terraform
===============================================================================
[![Build Status](https://travis-ci.org/d2si-oss/demo-aws-lambda-buffer-api.svg?branch=master)](https://travis-ci.org/d2si-oss/demo-aws-lambda-buffer-api)

Project Overview
----------------

Here were the basic requirements for the project:

- One HTTP endpoint to accept a JSON GET/POST/PUT/DELETE/OPTIONS containing misc data. These values would need to be stored somewhere.
- Define everything via terraform to make it reproducible.

To accomplish this I needed a few components:

- A front-end to take in HTTP requests. [API Gateway](http://docs.aws.amazon.com/en_en/apigateway/latest/developerguide/welcome.html)
- A back-end to do something with the requests and generate responses. [AWS Lambda](http://docs.aws.amazon.com/lambda/latest/dg/lambda-introduction.html)
- A datastore to keep all the associated short tokens and API responses. [AWS Dynamo](http://docs.aws.amazon.com/amazondynamodb/latest/developerguide/HowItWorks.html)
