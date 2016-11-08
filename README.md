# circleci-cron-serverless

A simple project that allow scheduled build for the circleci free tier.  

Here what happens.

1. A aws lamdba function named `circle-ci-cron` is created
2. The `circle-ci-cron` lamdba function will run once an hour
3. Each time the `circle-ci-cron` lamdba function runs it will use the circleci REST api to start a build

The following are required:

1. You need to first install https://serverless.com/ on your local computer
2. You need a aws account with API credential set up for serverless.com (see: https://serverless.com/framework/docs/providers/aws/guide/credentials/)

To run:

1. Update the handler.js constants with your circleci api key, project name, etc.
2. Run `serverless deploy`
3. Double check that your circleci.com project to make sure that the build started
