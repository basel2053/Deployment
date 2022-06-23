## Pipeline Process

The pipeline is using circleci on the main branch of the repo

- Repository link: <https://github.com/basel2053/Deployment>

### Orbs

1. `node`
2. `aws-cli`
3. `eb`

### Jobs

- build

1. Installing node and checking code
2. Install Front-End Dependencies
3. Install API Dependencies
4. Build the frontend app
5. Build the backend API

- deploy

1. Setting up EB
2. AWS-CLI Set up
3. Checking code for deployment
4. Deploying both the frontend and backend API

### Workflow

Build runs first, Then the deploy will be on hold until a human approval is provided

### CircleCI EB Secrets

- a screenshot can be found in screenshots folder

### CircleCI Steps

1. Push Code to a repo
2. The repository is then accessed by CircleCI
3. CircleCI runs our Pipeline
4. it will install our dependencies and check our code
5. it will start our jobs
6. first build
7. deploy will be on hold waitin for an approval
8. once approval is provided the deploy job will begin to execute
