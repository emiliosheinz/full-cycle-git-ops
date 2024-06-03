# GitOps

The usual development lifecycle occurs as follows: the developer writes the code, pushes it to the repository, and then the CI/CD pipeline takes over to build, test, and deploy the code to the target environment.

![Development Lifecycle](./docs/images/without-gitops.png)

Although this approach works well, it has some drawbacks, such as the possibility of someone manually changing the code deployed in the target environment without reflecting those changes in the repository, leading to a divergence between the code in the repository and the code in the target environment.

To address this issue, GitOps was introduced. GitOps is a way to do Continuous Deployment. It works by using Git as a single source of truth for declarative infrastructure and applications definitions. With GitOps, the developer writes the code, pushes it to the repository, and then the CI/CD pipeline takes over to build and test the application. The difference is that an agent that watches the repository for changes is responsible for deploying the application to the target environment.

![Development Lifecycle with GitOps](./docs/images/with-gitops.png)

This also reduces coupling between the CI/CD process and the target environment. Since the CI/CD pipeline does not need to connect to the target environment to deploy the application.
