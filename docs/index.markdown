# Observability as Code

New Relic provides a premier suite of tools expressly built to ease the configuration, management, and usage of New Relic through automation. This repo serves as a central location for you to discover the tools currently available, see what's being worked on right now, and provide feedback.

* [Project Website](https://newrelic.github.io/observability-as-code/) - Main source of information about New Relic Observability as Code
* [Our Projects](#our-projects) - Choose the right tool for the job. Find the tool that best integrates New Relic into your workflow.
* [Support](#support) - Need additional help? Check out our support links.

<br>

## Our Projects

* [**New Relic Terraform Provider**](https://github.com/newrelic/terraform-provider-newrelic)
  * [Documentation](https://www.terraform.io/docs/providers/newrelic/index.html)
  * [Quick Start Video](https://www.youtube.com/watch?v=UwJ-7BLylJo) - Walk through how to configure New Relic via Terraform in just a few minutes.
  * [Getting Started Guide](https://www.terraform.io/docs/providers/newrelic/guides/getting_started.html) - Easy to follow example to get you started.
* [**New Relic CLI**](https://github.com/newrelic/newrelic-cli)
  * [Documentation](https://github.com/newrelic/newrelic-cli/tree/main/docs/cli)
  * [Quick Start Video]() - Overview of the key features the New Relic CLI provides (Spoiler: Deployment Markers, Tag Management, and more!)
  * [Getting Started Guide](https://github.com/newrelic/newrelic-cli/blob/master/docs/GETTING_STARTED.md) - For the quick copy/pasters out there. Get started ASAP.
* [**New Relic Client**](https://github.com/newrelic/newrelic-cli)
  * [Documentation](https://github.com/newrelic/newrelic-client-go#example) - Quick overview of importing this library into your own application.

<br>

## Community

New Relic hosts and moderates an online forum called the [New Relic Explorers Hub](https://discuss.newrelic.com/c/build-on-new-relic/). Customers can interact with New Relic employees as well as other customers to get help and share best practices. Like all official New Relic open source projects, there's a related Community topic in the New Relic Explorers Hub.

<br>

### Issues or Enhancement Requests

Issues and enhancement requests can be submitted in the [Issues tab of this repository](https://github.com/newrelic/observability-as-code/issues). Please search for and review the existing open issues before submitting a new issue.

<br>

### Contributing

Contributions are welcome (and if you submit a Enhancement Request, expect to be invited to contribute it yourself :grin:). Please review our [Contributors Guide](CONTRIBUTING.md).

Keep in mind that when you submit your pull request, you'll need to sign the CLA via the click-through using CLA-Assistant. If you'd like to execute our corporate CLA, or if you have any questions, please drop us an email at opensource@newrelic.com.

<br>

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

bundle exec jekyll serve
```

### Support

New Relic has open-sourced this project. This project is provided AS-IS WITHOUT WARRANTY OR SUPPORT, although you can report issues and contribute to the project here on GitHub.

_Please do not report issues with this software to New Relic Global Technical Support._

* [Issues or Enhancement Requests](#issues-or-enhancement-requests)
* [Contributing](#contributing)
* [Community](#community)

<br>

## Open Source License

This project is distributed under the [Apache 2 license](LICENSE).
