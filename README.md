# Admin

Administrative web-interface for our amazing Shop (tm)  

Consists of SPA Frontend application and also thin layer of backend
responsible for server-side rendering and initial request routing.

Owner|Tier|Status|Landscape|Contexts
---|---|---|---|---
FrontendTeam|Tier1|Prod|Web|Customers,Orders,Payments,Catalog

##### Environments

Production:

- URL: https://...
- AWS account: 1234567890
- Logs: https://...
- Dashboard: https://...

Staging:

- URL: https://...
- AWS account: 0987654321
- Logs: https://...
- Dashboard: https://...

##### Tech

- React 16.x: frontend implementation framework
- NodeJS 10.x: backend implementation language
- AWS Lambda: backend execution env
- AWS API Gateway: main backend entry point
- Serverless: deployment
- CircleCI: CI tooling

##### Links

- [Project documentation](https://www.projectconnections.com/knowhow/burning-questions/what-is-project-documentation.html)

## Dev environment

To setup dev environment simply run

    docker-compose up
    
## Deployment

Deployment to production environment is done by CircleCI and is triggered
by git tag creation.

Staging environment is deployed on every tag creation or push to master/release
branch.

In case you need to manually deploy for whatever reason use following command:

    AWS_PROFILE=... ENV=... VERSION=... make deploy