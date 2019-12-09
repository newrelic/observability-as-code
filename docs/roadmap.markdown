---
layout: page
title: "Roadmap"
permalink: /roadmap/
---

---
---
# Note that this is a work-in-progress, and subject to change!
---
---

## Context

The Developer Toolkit is a set of tools that simplify New Relic configuration and management. Enabling developers to implement Observability as Code through industry standard frameworks such as Terraform and CloudFormation, or integrate into their existing workflow with the New Relic CLI. For those who require fine-grained control, the New Relic Client takes all of the guesswork out of directly using New Relic APIs.


## Personas

**Software Engineer** - A software engineer is someone who is writing, deploying, and managing the lifecycle of any software stack that utilizes New Relic. As the owner of the application, they are responsible for managing all Alerts, Dashboards, Nerdpacks, and other New Relic resources specific to their application.

**Site Reliability Engineer** - A Site Reliability Engineer (SRE) is an individual who is responsible for the stability of the entire software stack.  They assist Software Engineers with proper New Relic configuration, and provide overall guidance across teams.  Working with multiple teams becomes difficult when they do not operate in a similar way, so SREs strive to develop easy to follow standards.

**Security Engineer** - A Security Engineer is someone responsible for auditing and verify compliance of their software.  In order to facilitate this, New Relic has been made a requirement for all services, and as such needs specific tagging and configuration across all assets.  When faced with any reasonable sized organization this becomes a daunting task.


## Job Stories

**Observability As Code Providers**

* When I deploy a service, I want to embed the New Relic configuration in code with the rest of the service definition
* When I audit our systems, I want an easy way to verify the New Relic configuration is defined as expected

**New Relic CLI**

* When I deploy an applications, I want to record the deployment in New Relic without having to learn how their API works
* When service ownership changes, I want an easily, automated way to change tags within New Relic

**New Relic Client**

* When I have custom tooling in place that I want to leverage New Relic, I want to be able to use a supported library.
* When I build a deployment pipeline using serverless functions, I want to include New Relic.



## Developer Toolkit v1

To solve for the above problems, the initial version of the Developer Toolkit is defined to contain the following resources.  All resources shall be built as Open Source projects, and actively engage with the broader community.

* **[New Relic Terraform Provider](https://github.com/terraform-providers/terraform-provider-newrelic/)** - The New Relic Terraform Provider enables Observability as Code, reducing developer toil, and allows users to manage their entire ecosystem in a single place.

   * Built on the New Relic Client
   * Fully implementations APIs available through the New Relic Client
   <br/>

* **New Relic Client** - The New Relic Client provides the building blocks for many tools in the toolkit, enabling quick access to the suite of New Relic APIs.  As a library, it can also be leveraged within your own custom applications.

   * Full support for the followin New Relic API endpoints
     * APM REST v2 API
     * Infrastructure API
     * Synthetics API
     * GraphQL
   <br/>

* **New Relic CLI** - The New Relic CLI allows integrating New Relic into your existing workflows. Be it fetching data from your laptop while troubleshooting an issue, or adding New Relic into your CI/CD pipeline.

   * Build on the New Relic Client
   * Initial implementation of
     * Deployment Markers
     * Tagging
   <br/>

* **[New Relic AWS CloudFormation Integration](https://github.com/newrelic/cloudformation-partner-integration)** - The AWS CloudFormation Integration enables developers using CloudFormation to easily provision a subset of New Relic resources.

   * Build on the NR Client
   * Initial implementation of
     * Basic NRQL Alert configuration
   <br/>


## Milestones

Ongoing work will be tracked in the [Developer Toolkit](https://github.com/orgs/newrelic/projects/6) Project, which will link to each individual tool that is in flight.  Here the latest summary for planned work by the New Relic team:

### 2019 Winter

| State | Tool | Milestone | Rationale |
| ----- | ---- | --------- | --------- |
| Completed | New Relic Terraform Provider | (Tracked Internally)| The current Terraform Provider for New Relic was created by the community, and suffering from lack of attention.  DTK will integrate into the ecosystem, and create a clean base to work from. |
| **Current** | New Relic Terraform Provider | [Feature Parity with v2 APIs](https://github.com/terraform-providers/terraform-provider-newrelic/projects/1?card_filter_query=milestone%3A%22feature+parity+with+v2+apis%22) | Enhance the Terraform provider to include all capabilities of the REST v2 API and NerdGraph data access, including configuring Cloud Integrations and Tagging |
| Next | New Relic Client | [New Relic Client Consolidation](https://github.com/newrelic/newrelic-client-go/projects/1?card_filter_query=milestone%3A%22new+relic+client+consolidation%22) | Currently there is not a consistent, easy to use experience for developing against the New Relic APIs.  As the Developer Toolkit team continues to create new tools for users, having a consolidated library.  This MMF strives to create a unified client library for consumption by the community, and specifically utilized in the New Relic Terraform Provider. |

### 2020 Spring

| State | Tool | Milestone | Rationale |
| ----- | ---- | --------- | --------- |
| Planning | New Relic Client | GraphQL Support | NerdGraph, New Relic's implementation of GraphQL is the future platform for all API requests, and is the backing solution for New Relic One. As such, the NR Client needs to implement GraphQL to support any additional data. |
| Planning | New Relic Terraform Provider | Provider 2.0 | In order to add some newer features to the New Relic Terraform Provider, we need to implement some breaking changes.  This is a delicate area, so reving the major version and implementing the most important of those changes is warranted. |
| Planning | New Relic CLI | Initial Support | Community members with existing workflows want to be able to leverage command line tooling for interacting with New Relic. Leveraging the New Relic Client, we can build a CLI to simplify user interactions with New Relic in scripted and interactive workflows. |
| Planning | CloudFormation | Initial Support | New Relic has released a minimal Partner integration for CloudFormation specifically covering NRQL Alerting. Evaluate if reproducing this using the New Relic Client would allow for quickly adding support for other resources available through the NR Client for feature parity with the New Relic Terraform Provider. |
| Planning | Developer Toolkit Docs | Enhanced Docs and Examples | The Developer Toolkit as a collection of tools is extremely useful, however spreading the documentation across multiple repositories and in various levels of detail increases friction.  Create a consolidated collection of examples and documentation for tools, including when it is appropriate to use a specific tool vs another. |

### 2020 Summer

| State | Tool | Milestone | Rationale |
| ----- | ---- | --------- | --------- |
| Proposed | New Relic Client | Lambda Support | For community members already leveraging Serverless for their workflows, enabling the New Relic Client to be deployed in this way creates a quick path to embedding New Relic along side their existing best practices. |
| Proposed | New Relic CLI | Streamlined Installation | Enabling easy installation and upgrading of the NR CLI following existing workflows provides a streamlined experience to the user.  This should include installation through well-known package managers for supported platforms, so maintenance of the CLI fits into existing practices for the user. |
| Proposed | New Relic CLI | New Relic Logs Support | Integration of New Relic Logs and the NR CLI extends the user experience of the New Relic's logging solution into the terminal. |
| Proposed | Developer Toolkit Docs | Curate Community Docs / Examples | As a community focused project, it is important that we work with the extended community in providing documentation and example workflows. Engaging in this way will drive inovation across the broader community, and easy onboarding for those new to the space. |

### 2020 Fall

| State | Tool | Milestone | Rationale |
| ----- | ---- | --------- | --------- |
| Proposed | New Relic Client | Initial Automated Actions | Working with automation service providers, the New Relic Client should become a first class application that can be consumed by the community. |
| Proposed | Developer Toolkit | Initial IDE Plugin | Building a plugin for commonly used IDEs enables users to move faster, utilizing the environment that they are already accustom to. Initial work is to be defined, but should include items such as syntax highlighting for the New Relic Terraform Provider and/or CloudFormation Integration |
