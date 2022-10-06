# CircleCI Pipeline Steps

## Jobs

### Build

1. All necessary CLIs are installed (Node, EB CLI, AWS CLI).
2. The build process is triggered.
3. Frontend dependencies are installed.
4. Backend dependencies are installed.
5. Fronted linter will run to check the whole code.
6. Frontend is built.
7. Backend is built.

### Deploy

1. Installs Node, EB CLI, AWS CLI.
2. Checkout code.
3. Deploys frontend code to S3.
4. Deployed backend code to EB.

## Workflows

### udagram workflow

1. Calls the build job above.
2. Waits for user's approval to deploy the code after build.
3. If approved, the deploy job above is called.
