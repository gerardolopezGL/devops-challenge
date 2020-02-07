There are my considerations for Production ready:

# Governance (RBAC)
Role-based access control (RBAC) is a method of regulating access to computer or network resources based on the roles of individual users within an enterprise.

Processes around governance, auditing and compliance are a sign of the growing maturity of Kubernetes and the growing proliferation of Kubernetes-based application in large enterprises and regulated industries.

#Security
It goes without saying that security is a critical part of cloud native applications and needs to be considered and designed for from the very start. Security is a constant throughout the container lifecycle and it affects the design, development, DevOps practices and infrastructure choice for your container-based application. A range of technology choices is available to cover various areas such as application-level security and the security of the container and infrastructure itself. There range from using role-based access control, multifactor authentication (MFA), A&A (Authentication & Authorization) using protocols such as OAuth, OpenID, SSO etc.; Different tools that provide certification and security for what goes inside the container itself (such as image registry, image signing, packaging), CVE scans, and more.

# Cluster Provisioning as Ansible

# Registry and Package Management — Helm/Terraform
A private registry server is an important function in that it stores Docker images securely. The registry enables image management workflow, with image signing, security, LDAP integration, and more. Package managers, such as Helm, provide a template (called a “chart” in Helm) to define, install, and upgrade Kubernetes-based application.

# Cluster Monitoring and Logging
Production deployments of Kubernetes often scale up to hundreds of pods and the lack of effective monitoring and logging can result in an inability to diagnose severe failures that result in service interruptions and impact customer satisfaction and the business. Considere to use FluentBit, Fluentd, Elasticsearch and Kibana

#Replicas MongoDB
Replication provides redundancy and increases data availability. With multiple copies of data on different database servers, replication provides a level of fault tolerance against the loss of a single database server.

#Secrets
- Vault
- Secrets k8s

#Store config in the environment
Stores config in environment variables (often shortened to env vars or env). Env vars are easy to change between deploys without changing any code; unlike config files, there is little chance of them being checked into the code repo accidentally; and unlike custom config files, or other config mechanisms such as Java System Properties, they are a language- and OS-agnostic standard.

#Auto-scaler

The Horizontal Pod Autoscaler automatically scales the number of pods in a replication controller, deployment, replica set or stateful set based on observed CPU utilization (or, with custom metrics support, on some other application-provided metrics). Note that Horizontal Pod Autoscaling does not apply to objects that can’t be scaled, for example, DaemonSets.

#Features flags


