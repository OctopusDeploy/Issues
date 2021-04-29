# How we use GitHub Issues

> Note: this page is intended for Octopus team members only. If you're an Octopus user and you've found a bug or something isn't working, please get in touch with [our support team](https://octopus.com/support) instead.

We use this public GitHub repository as a way to communicate with our community about what we are working on for the core Octopus product.

Different teams across Octopus use the public issues in this repository for the following purposes:

- **Engineers**: Use public issues for linking Pull Requests. This helps with automatic release note generation.
- **Support** and **Customer Success** teams:
  - If you want someone to address an issue, you still need to bring it to the attention of the appropriate team internally, for example, via the requests channel of a Quick Reaction Force.
  - Use public issues to aid communication with customers while waiting on a possible fix. Customers can subscribe to these GitHub issues, you can use them to collate and track relevant support tickets, and publish workarounds for multiple customers in a single place.
- **Product** teams: Product teams own the Issues list, they will close anything that's unlikely to be fixed and provide context to Support and Customer Success teams as necessary to help manage expectations.

## Which repository should I create the issue in?

If you want to track an Issue that doesn't deserve public attention, you can track it with an Issue in the [Private GitHub repository](https://github.com/OctopusDeploy/OctopusDeploy/issues).

This issues repository is for the core Octopus product.  Open-source extensions to Octopus have their own repositories, and issues for them should be managed there. 

For example:
- [Azure DevOps and TFS](https://github.com/OctopusDeploy/OctoTFS/issues)
- [Bamboo Add-On](https://github.com/OctopusDeploy/Octopus-Bamboo/issues)
- [GitHub Issue Tracker](https://github.com/OctopusDeploy/GitHubIssueTracker/issues)
- [Go Client](https://github.com/OctopusDeploy/go-octopusdeploy/issues)
- [Jenkins Plugin](https://github.com/OctopusDeploy/octopus-jenkins-plugin/issues)
- [Jira Integration](https://github.com/OctopusDeploy/JiraIntegration/issues)
- [Octopus CLI](https://github.com/OctopusDeploy/OctopusCLI/issues)
- [Octopus Client](https://github.com/OctopusDeploy/OctopusClients/issues)
- [TeamCity Plugin](https://github.com/OctopusDeploy/Octopus-TeamCity/issues)
- [Terraform Provider](https://github.com/OctopusDeployLabs/terraform-provider-octopusdeploy/issues)

## How to raise an issue

Make use of the issue templates and fill out all of the sections. The more specific details you can provide, the better. For example, providing links to the original reports for bugs (e.g. support tickets), details of how to replicate the issue, and known workarounds wherever possible will help affected customers, and help speed up a resolution. 

Remember, once you've created an issue, you still need to raise it with the relevant team internally.

## How we use GitHub Milestones

We use GitHub Milestones to group Issues into a Release, not for planning purposes. Once an Issue is closed we add it to the Milestone representing the Release that will ship the fix for the Issue. We find all of the closed Issues in a Milestone to build Release Notes.

## Release Note generation
It's important that we have good release notes with each build (we never seem to get into trouble for having too many release notes).

We automatically create Release Notes in markdown by querying the public GitHub Issues that form part of a Release.

We scan the Comments of an Issue for one beginning with a specific string: `Release Note: ` (or any other defined in the source) and use that for the Release Note, otherwise, we'll use the Issue Title.
