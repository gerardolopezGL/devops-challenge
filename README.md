# Devops-Gorilla-challenge
This repo contains the findings from DevOps challenge.

# Stack
- Angular
- Node
- Mongo
- jenkins
- Terraform
- Packer
- Kubernetes

## Why I chose Angular and Node?
In recent years, single page applications (SPAs) have become more and more popular. A SPA is a website that consists of just one page. That lone page acts as a container for a JavaScript application. The JavaScript is responsible for obtaining the content and rendering it within the container. The content is typically obtained from a web service and RESTful APIs have become the go-to choice in many situations. The part of the application making up the SPA is commonly known as the client or front-end, while the part responsible for the REST API is known as the server or back-end. 

For the server, I will be using Node with Express. Express is a framework that makes it easy to create REST APIs by allowing to define code that runs for different requests on the server. Additional services can be plugged in globally, or depending on the request. There are a number of frameworks that build on top of Express and automate the task of turning your database models into an API. 

Angular encourages the use of TypeScript. TypeScript adds typing information to JavaScript and, *in my opinion*, is the future of developing large scale applications in JavaScript. 

# Deliverables
- [IaC repo](https://github.com/gelopfalcon/terraform-k8s-gcp)
- [Angular-Frontend](https://github.com/gelopfalcon/angular-realworld-example-app)
- [Node-Backend](https://github.com/gelopfalcon/node-express-realworld-example-app)

 Automated deployment upon code commit to an environment.
- A zero downtime release
  - Rollback strategy in Kubernetes: Zero unavailable pods.
  - livenessProbe to check if a pod needs being restarted.
  - readinessProbe to check when the pod is ready to receive traffic.
- Health checks
   - readinessProbe
   - Health checks in Ingress (We are using it as LB)
- Use of Infrastructure as Code
   - Terraform
   - Packer
- High availability, Load balanced and TLS secured solution
 - Kubernetes regional cluster. 3 regions, 2 nodes per region.
 - Ingress to manage the traffic of our services
