---
layout: home
---

The New Relic Developer Toolkit is a suite of tools expressly built to ease the configuration, management, and usage of New Relic through automation.  This repo serves as a central location for you to discover the tools currently available, see what's being worked on right now, and provide feedback.

* General Resources
  * [Getting Started Guides](#getting-started)
  * [New Relic Developer Resources](https://developer.newrelic.com)
  * [Roadmap](roadmap/) - Current and future work priorities
  * [Kanban Board](https://github.com/orgs/newrelic/projects/6) - Current work across all tools
* Tools in the Toolkit
  * [New Relic Terraform Provider](#new-relic-terraform-provider)
  * [New Relic CLI](#new-relic-cli)
  * [New Relic Client](#new-relic-client)
  * [New Relic Kubernetes Operator](#new-relic-kubernetes-operator)
  * [Deployment Marker Github Action](https://github.com/marketplace/actions/new-relic-application-deployment-marker)
  * [New Relic AWS CloudFormation Integration](#new-relic-aws-cloudformation-integration)
  * [New Relic Java Agent Ansible Role](#new-relic-java-agent-ansible-role)
* Support
  * [Helpful Links](#helpful-links)
  * [Community](#community)
  * [Issues or Enhancement Requests](#issues-or-enhancement-requests)
  * [Contributing](#contributing)
  * [Open Source License](#open-source-license)

## Getting Started

Ready to jump right in? Excellent! Here are some quick reference guides to
assist you in your journey to increased consistency and decreased toil:

> For more information on the toolkit and explore other programmability capabilities for New Relic One, check out our [developer](https://developer.newrelic.com/use-cases/workflow-automation) site.

* [New Relic Terraform Provider](#new-relic-terraform-provider)
  * [Quick Start Video](https://www.youtube.com/watch?v=UwJ-7BLylJo) - Walk through how to configure New Relic via Terraform in just a few minutes.
  * [Getting Started Guide](https://www.terraform.io/docs/providers/newrelic/guides/getting_started.html) - Easy to follow example to get you started.
* [New Relic CLI](#new-relic-cli)
  * [Quick Start Video](https://www.youtube.com/watch?v=g00AeKlECZA) - Overview of the key features the New Relic CLI provides (Spoiler: Deployment Markers, Tag Management, and more!)
  * [Getting Started Guide](https://github.com/newrelic/newrelic-cli/blob/master/docs/GETTING_STARTED.md) - For the quick copy/pasters out there. Get started ASAP.
* [New Relic Client](#new-relic-client)
  * [Example usage](https://github.com/newrelic/newrelic-client-go#example) - Quick overview of importing this library into your own application.
* [New Relic AWS CloudFormation Integration](#new-relic-aws-cloudformation-integration)
  * [Documentation](https://docs.newrelic.com/docs/integrations/amazon-integrations/aws-integrations-list/aws-cloudformation-integration) - Get up and running with New Relic + CloudFormation for NRQL Alerting


## Tools in the Toolkit

#### New Relic Terraform Provider

The New Relic Terraform Provider enables Observability as Code, reducing developer toil, and allows users to manage their entire ecosystem in a single place.

* [Documentation](https://www.terraform.io/docs/providers/newrelic/index.html)
* [Repo](https://github.com/newrelic/terraform-provider-newrelic)
* [Terraform Module for New Relic APM](https://registry.terraform.io/modules/newrelic/apm/newrelic/)


#### New Relic CLI

The New Relic CLI enables integration of New Relic into your existing workflows. Be it fetching data from your laptop while troubleshooting an issue, or adding New Relic into your CI/CD pipeline.

* [Documentation](https://github.com/newrelic/newrelic-cli)
* [Repo](https://github.com/newrelic/newrelic-cli)
* [Docker Image](https://hub.docker.com/r/newrelic/cli)


#### New Relic Kubernetes Operator

The newrelic-kubernetes-operator is a Kubernetes Operator that facilitates management of New Relic resources from within
your Kubernetes configuration. Managing New Relic resources via custom Kubernetes objects can be done the same way you
manage built-in Kubernetes objects.

* [Documentation](https://github.com/newrelic/newrelic-kubernetes-operator)
* [Repo](https://github.com/newrelic/newrelic-kubernetes-operator)
* [Docker Image](https://hub.docker.com/r/newrelic/kubernetes-operator)


#### New Relic Client

The New Relic Client provides the building blocks for many tools in the toolkit, enabling quick access to the suite of New Relic APIs.  As a library, it can also be leveraged within your own custom applications.

* [Documentation](https://pkg.go.dev/github.com/newrelic/newrelic-client-go)
* [Repo](https://github.com/newrelic/newrelic-client-go)


#### New Relic Java Agent Ansible Role

The New Relic Java Agent Ansible Role installs and configures the New Relic Java agent. It should work with minimal configuration for applications running under Tomcat, Jetty, or Wildfly. We aim to support the most popular Java web servers over time.

* [Documentation](https://github.com/newrelic/newrelic-java-agent-ansible-role#ansible-role-new-relic-java-agent)
* [Repo](https://github.com/newrelic/newrelic-java-agent-ansible-role)
* [Ansible Galaxy](https://galaxy.ansible.com/newrelic/newrelic_java_agent)


#### New Relic AWS CloudFormation Integration

The AWS CloudFormation Integration enables developers using CloudFormation to easily provision a subset of New Relic resources.

* [Documentation](https://docs.newrelic.com/docs/integrations/amazon-integrations/aws-integrations-list/aws-cloudformation-integration)
* [Repo](https://github.com/newrelic/cloudformation-partner-integration)


## Community

New Relic hosts and moderates an online forum where customers can interact with New Relic employees as well as other customers to get help and share best practices. Like all official New Relic open source projects, there's a related Community topic in the New Relic Explorers Hub. You can find this project's topic/threads here:

https://discuss.newrelic.com/c/build-on-new-relic/developer-toolkit


### Issues or Enhancement Requests

Issues and enhancement requests can be submitted in the [Issues tab of this repository](https://github.com/newrelic/developer-toolkit/issues). Please search for and review the existing open issues before submitting a new issue.


### Contributing

Contributions are welcome (and if you submit a Enhancement Request, expect to be invited to contribute it yourself :grin:). Please review our [Contributors Guide](CONTRIBUTING.md).

Keep in mind that when you submit your pull request, you'll need to sign the CLA via the click-through using CLA-Assistant. If you'd like to execute our corporate CLA, or if you have any questions, please drop us an email at opensource@newrelic.com.


### Support

New Relic has open-sourced this project. This project is provided AS-IS WITHOUT WARRANTY OR SUPPORT, although you can report issues and contribute to the project here on GitHub.

_Please do not report issues with this software to New Relic Global Technical Support._

## PGP Public Key
The team's PGP public key can be accessed [here](https://newrelic.github.io/developer-toolkit/developer-toolkit.asc).

## Open Source License

This project is distributed under the [Apache 2 license](LICENSE).
