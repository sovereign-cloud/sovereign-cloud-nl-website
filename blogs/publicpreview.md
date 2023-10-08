---
title: "Microsoft ACA updates 2023 - Q3" # Title of the blog post.
date: 2023-08-23T16:12:35+01:00 # Date of post creation.
description: "Microsoft ACA Updates Q3 2023." # Description used for search engine.
featured: false # Sets if post is a featured post, making appear on the home page side bar.
draft: true # Sets whether to render this page. Draft of true will not be rendered.
toc: false # Controls if a table of contents should be generated for first-level links automatically.
# menu: main
usePageBundles: false # Set to true to group assets like images in the same folder as this post.
# featureImage: "/images/ignite.png" # Sets featured image on blog post.
# featureImageAlt: 'DockerCon 2018' # Alternative text for featured image.
# featureImageCap: 'This is the featured image.' # Caption (optional).
thumbnail: "/images/aca.png" # Sets thumbnail image appearing inside card on homepage.
# shareImage: "/images/DockerCon2018.png" # Designate a separate image for social media sharing.
codeMaxLines: 10 # Override global value for how many lines within a code block before auto-collapsing.
codeLineNumbers: false # Override global value for showing of line numbers within code block.
figurePositionShow: true # Override global value for showing the figure label.
categories:
  - Technology
  - Microsoft
tags:
  - Kubernetes
  - ACA
# comment: false # Disable comment if false.
---

Within this blog, I want to give an overview of all the feature in Q3 2023 that becomes available in General Availability, Technical Preview or End of Support by Microsoft.
This information can be found at Microsoft <a href="https://azure.microsoft.com/en-us/updates/?query=AKS"> Azure Updates</a>.

<b> Features are now supported by Microsoft (GA): </b>
- [General available] <a href="https://azure.microsoft.com/en-us/updates/generally-available-azure-container-apps-savings-plan-support/">Apps is now eligible for Azure savings plan for compute</a> <br>
  Azure Container Apps is now eligible for Azure savings plan for compute! All Azure Container Apps regions and plans are eligible to receive 15% savings (1 year) and 17% savings (3 years) compared to pay-as-you-go when you commit to an Azure savings plan. You can save by committing to spending a fixed hourly amount for 1 or 3 years, unlocking lower prices. Click <a href="https://techcommunity.microsoft.com/t5/apps-on-azure-blog/azure-container-apps-eligible-for-azure-savings-plan-for-compute/ba-p/3941243">here</a> to learn more. <br>
- [General available] <a href="https://azure.microsoft.com/en-us/updates/ga-azure-container-apps-in-azure-china-cloud/">Azure Container Apps in Azure China cloud</a> <br>
  We are pleased to announce that Azure Containers Apps is now generally available in the Azure China cloud. Azure Container Apps is a fully managed serverless container service which offers an ideal platform for application developers who want to run microservices, APIs, and more using containers without managing infrastructure. Azure Container Apps is available in the China North 3 region. Write code using your preferred programming language or framework and build microservices with full support for Distributed Application Runtime (Dapr). Scale dynamically based on HTTP traffic or events powered by Kubernetes Event-Driven Autoscaling (KEDA)
  Container Apps is built on a foundation of powerful open-source technology. Behind the scenes, every container app runs using the Kubernetes API, with KEDA, Dapr, and Envoy baked in. This lets you perform modern application lifecycle tasks such as application upgrades, traffic shifting, and versioning ready-to-run for teams of every skillset. Click <a href="https://learn.microsoft.com/en-gb/azure/container-apps/get-started?ocid=AID3042118&tabs=bash">here</a> to visit the get started guide. <br>
- [General available] <a href="https://azure.microsoft.com/en-us/updates/general-availability-use-azure-key-vault-to-securely-store-and-retrieve-access-key-when-mounting-azure-storage-as-a-local-sha/">Use Azure Key Vault to securely store and retrieve access key when mounting Azure Storage as a local share in App Service</a> <br>
  You can now use Azure Key Vault to securely store and retrieve Azure Storage account access key when mounting it as a local share in App Service. Azure Key Vault has the benefits of storing application secrets centrally and securely with the ability to monitor, administer, and integrate with other Azure services like Azure App Service.
  This feature is available for App Service Linux code and container, Windows containers and Windows code. Click <a href="https://learn.microsoft.com/en-us/azure/app-service/configure-connect-to-azure-storage?tabs=key-vault%2Ccli&pivots=container-linux ">here</a> to learn more. <br>
- [General available] <a href="https://azure.microsoft.com/en-us/updates/generally-available-azure-container-apps-jobs/">Azure Container Apps jobs</a> <br>
  Jobs — a new Azure Container Apps feature previewed at Microsoft Build 2023 — is now generally available. In addition to continuously running services that can scale to zero, Azure Container Apps now supports jobs. Jobs enable you to run serverless containers that perform tasks that run to completion.
  Azure Container Apps jobs support three trigger types: manual (on-demand), scheduled, and event-driven. Manual jobs are triggered by a user or an external system, such as another container app. Scheduled jobs are triggered at a specified time or interval. Event-driven jobs are triggered by scaling rules.
  Common scenarios for jobs include:
    - Running a one-time containerized data migration job;
    - Running a scheduled, recurring containerized batch job, such as a nightly inventory processing job;
    - Running a containerized job in response to an event, such as a message arriving in a queue;
    - Running CI/CD build processes such as Azure Pipelines agents and GitHub Actions runners in a Container Apps environment;
  A job can run multiple executions concurrently, and each job execution can run multiple replicas in parallel.
  Container apps and jobs share the same Container Apps environment, providing them with a common serverless platform and shared capabilities such as networking and observability. Jobs can communicate with container apps in the same environment. Jobs support both the Consumption and Dedicated plans. When jobs run in the Consumption plan, you pay only when jobs are executing, by the second. In the Dedicated plan, jobs with specialized compute requirements can take advantage of custom workload profiles. Click <a href="https://learn.microsoft.com/en-gb/azure/container-apps/jobs?tabs=azure-cli">here for the documentation</a> or <a href="https://techcommunity.microsoft.com/t5/apps-on-azure-blog/generally-available-azure-container-apps-workload-profiles-more/ba-p/3913345">here for the blog</a>to learn more. <br>
- [General available] <a href="https://azure.microsoft.com/en-us/updates/generally-available-azure-container-apps-support-for-udr-nat-gateway-and-smaller-subnets/">Azure Container Apps support for UDR, NAT Gateway, and smaller subnets</a> <br>
  User defined routes (UDR), NAT Gateway, and smaller required subnet sizes are now generally available for Azure Container Apps on the new workload profiles environment type. Workload profiles environments support both the consumption and dedicated plans. You can define UDRs to manage how outbound traffic is routed to your container app environment’s subnet by enabling network appliances such as firewalls for workload profiles environments.
  When using a workload profiles environment, you can also configure a NAT Gateway to provide a static public IP address for all outbound traffic from your container apps. In addition, with workload profiles environment, the minimum subnet size required is a /27 CIDR. A minimum subnet size of /23 is still required for container apps created on the consumption only environment type.. Click <a href="https://learn.microsoft.com/en-gb/azure/container-apps/networking?tabs=azure-cli#environment-selection">here</a> to learn more. <br>
- [General available] <a href="https://azure.microsoft.com/en-us/updates/generally-available-azure-container-apps-dedicated-plan/">Azure Container Apps dedicated plan</a> <br>
  Azure Container Apps dedicated plan is now generally available in the new workload profiles environment type. A workload profile determines the amount of compute and memory resources available to container apps deployed in an environment. Compute options are represented as workload profiles defined at the Azure Container Apps environment scope. We currently support general purpose and memory optimized workload profiles with up to 32 vCPU’s and 256 GiB’s of memory.
  Workload profiles environments support both the consumption and dedicated plans. When using dedicated workload profiles you are billed per compute instance, compared to consumption where you are billed per app. Each app can be configured to run on any of the workload profiles defined for the Azure Container Apps environment scope with consumption and dedicated plans running seamlessly in the same Azure Container Apps environment. This is ideal for developers when deploying a microservice solution where each app can run on the appropriate compute infrastructure. Additionally, the consumption workload profile allows developers to request up to 4 vCPU’s and 8Gib’s of memory for an app, twice what can be requested when using a consumption only environment. Click <a href="hhttps://learn.microsoft.com/en-gb/azure/container-apps/plans#consumption--dedicated-plan-structure-preview">here</a> to learn more. <br>
- [General available] <a href="https://azure.microsoft.com/en-us/updates/generally-available-azure-key-vault-references-for-secrets-in-azure-container-apps/">Azure Key Vault references for secrets in Azure Container Apps</a> <br>
  Azure Container Apps support for Azure Key Vault references in application secrets is now generally available.
  Azure Key Vault references enable you to source a container app’s secrets from secrets stored in Azure Key Vault. Using the container app's managed identity, the platform automatically retrieves the secret values from Azure Key Vault and injects it into your application's secrets.
  Both versioned and non-versioned secrets are supported. Click <a href="https://learn.microsoft.com/en-gb/azure/container-apps/manage-secrets?tabs=azure-portal">here</a> to learn more. <br>
- [General available] <a href="https://azure.microsoft.com/en-us/updates/generally-available-session-affinity-for-azure-container-apps/">Session affinity for Azure Container Apps</a> <br>
  Azure Container Apps now supports session affinity, also known as sticky sessions, for HTTP-based workloads. This feature is generally available.
  Session affinity enables you to route all requests from a single client to the same Container Apps replica. This is useful for stateful workloads that require session affinity.Container apps in single revision mode support session affinity. When enabled, Container Apps automatically adds a cookie to HTTP responses to track the replica being used by the client.
  Click <a href="https://learn.microsoft.com/en-gb/azure/container-apps/sticky-sessions?pivots=azure-portal">here</a> to learn more. <br>
- [General available] <a href="https://azure.microsoft.com/en-us/updates/generally-available-secrets-volume-mounts-for-azure-container-apps/">Secrets volume mounts for Azure Container Apps</a> <br>
  Support for secrets volume mounts in Azure Container Apps is now generally available. In addition to referencing secrets as environment variables, you can now mount secrets as volumes in your container apps. Your apps can access all or selected secrets as files in a mounted volume.
  This feature works with secrets stored directly in Azure Container Apps and secrets referenced from Azure Key Vault.
  Click <a href="https://learn.microsoft.com/en-gb/azure/container-apps/manage-secrets?tabs=azure-portal">here</a> to learn more. <br>
- [General available] <a href="https://azure.microsoft.com/en-us/updates/generally-available-init-containers-in-azure-container-apps/">Init containers in Azure Container Apps</a> <br>
  The init containers feature in Azure Container Apps is now generally available. Init containers are specialized containers that run to completion before application containers are started in a replica, and they can contain utilities or setup scripts not present in your container app image. Init containers are useful for performing initialization logic such as setting up accounts, running setup scripts, and configuring databases.
  Click <a href="https://learn.microsoft.com/en-gb/azure/container-apps/containers#init-containers">here</a> to learn more. <br>
- [General available] <a href="https://azure.microsoft.com/en-us/updates/generally-available-cross-origin-resource-sharing-cors-in-azure-container-apps/">Cross Origin Resource Sharing (CORS) in Azure Container Apps</a> <br>
  Azure Container Apps support for Cross Origin Resource Sharing (CORS) is now generally available.
  By default, requests made through a browser to a domain that doesn’t match the page’s origin domain are blocked. The CORS feature allows specific origins to make calls on their app through the browser. Now Azure Container Apps customers can easily set up Cross Origin Resource Sharing from the portal or through the CLI.
  Click <a href="https://review.learn.microsoft.com/en-us/azure/container-apps/cors">here</a> to learn more. <br>

<b> Features are not yet supported by Microsoft (GA) </b> 
- [Public Preview] <a href="https://azure.microsoft.com/en-us/updates/public-preview-azure-container-apps-supports-additional-tcp-ports/">Azure Container Apps supports additional TCP ports</a> <br>
  Azure Container Apps now support additional TCP ports, enabling applications to accept TCP connections on multiple ports. This feature is in preview.
  Click <a href="https://learn.microsoft.com/en-gb/azure/container-apps/ingress-overview#additional-tcp-ports">here</a> to learn more. <br>
- [Public Preview] <a href="https://azure.microsoft.com/en-us/updates/public-preview-azure-container-apps-supports-environment-level-mtls-encryption/">Azure Container Apps supports environment level mTLS encryption</a> <br>
  Azure Container Apps now supports environment level network encryption using mutual transport layer security (mTLS). This feature is in preview. When end-to-end encryption is required, mTLS will encrypt data transmitted between applications within an environment..
  Click <a href="https://learn.microsoft.com/en-gb/azure/container-apps/networking?tabs=azure-cli#mtls">here</a> to learn more. <br>

<b> Features that are retired </b> 
- [Retired] <a href="https://azure.microsoft.com/en-us/updates/retirement-azure-container-apps-preview-api-versions-20220601preview-and-20221101preview/">Azure Container Apps preview API versions 2022-06-01-preview and 2022-11-01-preview</a> <br>
  Starting on November 16, 2023, Azure Container Apps control plane API versions 2022-06-01-preview and 2022-11-01-preview will be retired. Before that date, please migrate to the latest stable API version (2023-05-01) or latest preview API version (2023-04-01-preview).
  <b> Required action </b>
  If you're using Azure Resource Manager API version 2022-06-01-preview or 2022-11-01-preview to manage Azure Container Apps, please update your API requests to use version 2023-04-01-preview or later. Management operations using the retired API versions may fail after the retirement date.
  

For more information about the features that are coming out, please refer to the public <a href="https://github.com/orgs/microsoft/projects/540">roadmap</a> of Microsoft ACA team.
<br><br>


<img src="/images/aksk8s.png" width="400" height="400">

<br>
<br>

