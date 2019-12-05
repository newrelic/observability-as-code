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

<br/>

Problem | Reasons | Solution / Benefit
------- | ------- | ------------------
| Configuring New Relic is time consuming. | <ul><li>Users must use the UI, or create custom API scripts<li>Not all configuration can be done through APIs<li>APIs are different based on New Relic product<li>Existing libraries to reduce effort suffer from lack of ownership / maintenance</ul> | Provide tools to configure New Relic that reduces effort of the user |
| New Relic configuration can be inconsistent across applications | <ul><li>Manual configuration is required<li>Auditing configurations is labor intensive</ul> | Provide tools so New Relic configurations can be templated, repeatable, and audited easily |
| I cannot integrate New Relic into my exiting workflow | <ul><li>Using New Relic in a workflow currently requires significant time investment in custom scripts</ul> | Provide easy to consume tooling that can be leveraged in existing workflows to streamline New Relic usage |


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


## Recent Milestones

Ongoing work will be tracked in the [Developer Toolkit](https://github.com/orgs/newrelic/projects/6) Project, which will link to each individual tool that is in flight.  Here the latest summary for planned work by the New Relic team:

| State | Tool | Milestone | Rationale |
| ----- | ---- | --------- | --------- |
| Completed | New Relic Terraform Provider | (Tracked Internally)| The current Terraform Provider for New Relic was created by the community, and suffering from lack of attention.  DTK will integrate into the ecosystem, and create a clean base to work from. |
| **Current** | New Relic Terraform Provider | [Feature Parity with v2 APIs](https://github.com/terraform-providers/terraform-provider-newrelic/projects/1?card_filter_query=milestone%3A%22feature+parity+with+v2+apis%22) | Enhance the Terraform provider to include all capabilities of the REST v2 API and NerdGraph data access, including configuring Cloud Integrations and Tagging |
| Next | New Relic Client | [New Relic Client Consolidation](https://github.com/newrelic/newrelic-client-go/projects/1?card_filter_query=milestone%3A%22new+relic+client+consolidation%22) | Currently there is not a consistent, easy to use experience for developing against the New Relic APIs.  As the Developer Toolkit team continues to create new tools for users, having a consolidated library.  This MMF strives to create a unified client library for consumption by the community, and specifically utilized in the New Relic Terraform Provider. |

