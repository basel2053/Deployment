## Infrastructure description

- Node v14.15.1 (LTS) or more recent. While older versions can work it is advisable to keep node to latest LTS version

- RDS database to host our postgres database

- AWS Elastic Beanstalk to host the backend API

- S3 Bucket for hosting the frontend application (angular)

- Circleci for processing the pipeline to build and deploy

### Installation

Provision the necessary AWS services needed for running the application:

1. In AWS, provision a publicly available RDS database running Postgres. <Place database-1.cobzaxlh4qf3.us-east-1.rds.amazonaws.com/>
2. In AWS, provision a s3 bucket for hosting the uploaded files. <http://udacityrandom2053.s3-website-us-east-1.amazonaws.com/>
3. In AWS, provision an elastic beanstalk environment to host our API <http://udagram-api-dev2222.us-east-1.elasticbeanstalk.com/>
4. using a package for the environment variables, like [dotnev](https://www.npmjs.com/package/dotenv)/.
5. From the root of the repo, navigate udagram-api folder `cd starter/udagram-api` to install the node_modules `npm install`. After installation is done start the api in dev mode with `npm run dev`.
6. Without closing the terminal in step 5, navigate to the udagram-frontend `cd starter/udagram-frontend` to intall the node_modules `npm install`. After installation is done start the api in dev mode with `npm run start`.
7. Authorize circleci to use Github repo and configuring CircleCI pipeline
