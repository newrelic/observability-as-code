# Developer Toolkit

The New Relic Developer Toolkit is a suite of tools expressly built to ease the configuration, management, and usage of New Relic through automation.  This repo serves as a central location for you to discover the tools currently available, see what's being worked on right now, and provide feedback.

> **Request for Comments!**
>
> We've recently published our [Roadmap](https://newrelic.github.io/developer-toolkit/roadmap/) and have sumbitted this to the community for review. If you have any questions or comments, please contribute to the thread in our [discussion forum](https://discuss.newrelic.com/c/build-on-new-relic/developer-toolkit).



* General Resources
  * [Project Website](https://newrelic.github.io/developer-toolkit/) - Main source of information about the Developer Toolkit
  * [Roadmap](https://newrelic.github.io/developer-toolkit/roadmap/) - Current and future work priorities
  * [Kanban Board](https://github.com/orgs/newrelic/projects/6) - Current work across all tools
* Tools in the Toolkit
  * [New Relic Terraform Provider](#new-relic-terraform-provider)
  * [New Relic API Client](#new-relic-api-client)
  * [New Relic CLI](#new-relic-cli)
  * [New Relic AWS CloudFormation Integration](#new-relic-aws-cloudformation-integration)
* Support
  * [Helpful Links](#helpful-links)
  * [Community](#community)
  * [Issues or Enhancement Requests](#issues-or-enhancement-requests)
  * [Contributing](#contributing)
  * [Open Source License](#open-source-license)

## Tools in the Toolkit

#### New Relic Terraform Provider

The New Relic Terraform Provider enables Observability as Code, reducing developer toil, and allows users to manage their entire ecosystem in a single place.

* [Documentation](https://www.terraform.io/docs/providers/newrelic/index.html)
* [Repo](https://github.com/terraform-providers/terraform-provider-newrelic/)
* [Project boards](https://github.com/terraform-providers/terraform-provider-newrelic/projects)


#### New Relic Client

The New Relic Client provides the building blocks for many tools in the toolkit, enabling quick access to the suite of New Relic APIs.  As a library, it can also be leveraged within your own custom applications.

* Documentation
* Repo
* Project Boards


#### New Relic CLI

The New Relic CLI enables integration of New Relic into your existing workflows. Be it fetching data from your laptop while troubleshooting an issue, or adding New Relic into your CI/CD pipeline.

* Documentation
* Repo
* Project Boards

#### New Relic AWS CloudFormation Integration

The AWS CloudFormation Integration enables developers using CloudFormation to easily provision a subset of New Relic resources.

* [Documentation](https://docs.newrelic.com/docs/integrations/amazon-integrations/aws-integrations-list/aws-cloudformation-integration)
* [Repo](https://github.com/newrelic/cloudformation-partner-integration)
* [Project Boards](https://github.com/newrelic/cloudformation-partner-integration/projects)


## Community

New Relic hosts and moderates an online forum where customers can interact with New Relic employees as well as other customers to get help and share best practices. Like all official New Relic open source projects, there's a related Community topic in the New Relic Explorers Hub. You can find this project's topic/threads here:

https://discuss.newrelic.com/c/build-on-new-relic/

The link for the Developer Toolkit discussion can be found here:

https://discuss.newrelic.com/c/build-on-new-relic/developer-toolkit


### Issues or Enhancement Requests

Issues and enhancement requests can be submitted in the [Issues tab of this repository](https://github.com/newrelic/developer-toolkit/issues). Please search for and review the existing open issues before submitting a new issue.


### Contributing

Contributions are welcome (and if you submit a Enhancement Request, expect to be invited to contribute it yourself :grin:). Please review our [Contributors Guide](CONTRIBUTING.md).

Keep in mind that when you submit your pull request, you'll need to sign the CLA via the click-through using CLA-Assistant. If you'd like to execute our corporate CLA, or if you have any questions, please drop us an email at opensource@newrelic.com.


### Support

New Relic has open-sourced this project. This project is provided AS-IS WITHOUT WARRANTY OR SUPPORT, although you can report issues and contribute to the project here on GitHub.

_Please do not report issues with this software to New Relic Global Technical Support._


## Open Source License

This project is distributed under the [Apache 2 license](LICENSE).


## Development

### Requirements

This repo mostly contains a site for GitHub Pages, which is rendered via
Jekyll.  In order to test local changes, you'll need the following:

* Ruby 2.6.5 (rbenv suggested!)
* Bundler

### Running Locally

Once you have installed the above requirements:

```
cd docs/

bundle install

bundle exec jekyell serve
```
