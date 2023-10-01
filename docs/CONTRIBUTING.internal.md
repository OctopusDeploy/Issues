# How we use GitHub Issues

> Note: this page is intended for **Octopus team members only**. If you're an Octopus user and you've found a bug or something isn't working, please get in touch with [our support team](https://octopus.com/support) instead.

Internally, we use shortcut to track, label and triage all work and requests that flow through the R&D single front door. See [How we use shortcut](https://octopushq.atlassian.net/l/cp/rHgRH200)
This public GitHub repository is our way to communicate with our community about what we are working on for the core Octopus product. Ideally, for all fixes made on Octopus Server, there should be a corresponding issue.

When raising a github issue, be sure to also notify the R&D team through the single front door to ensure the appropriate action can be taken.

**See the [R&D Request Process flowchart](https://whimsical.com/r-and-d-request-process-5QHDgBDPSpszuBk4MdmhhM)** and [R&D Single Front Door](https://octopushq.atlassian.net/l/cp/eqs6uxfZ) for an overview

Different teams across Octopus use the public issues in this repository for the following purposes:

- **Engineers**: Use public issues for linking Pull Requests. This helps with automatic release note generation. Most private issues go to the [ResearchAndDevelopment issue list](https://github.com/OctopusDeploy/ResearchAndDevelopment/issues).
- **Support** and **Customer Success** teams:
  - Please follow the [R&D Request Process flowchart](https://whimsical.com/r-and-d-request-process-5QHDgBDPSpszuBk4MdmhhM)
  - If you want someone to address an issue, contact the appropriate channel as outlined in the flowchart. If in doubt, contact #rnd-requests. See [Types of Requests](https://octopushq.atlassian.net/wiki/spaces/RND/pages/2639954003/R+D+Single+Front+Door#Types-of-Requests)
  - Use public issues to aid communication with customers while waiting on a possible fix. Customers can subscribe to these GitHub issues, you can use them to collate and track relevant support tickets, and publish workarounds for multiple customers in a single place.
- **Product** teams: Product teams own the Issues list, they will close anything that's unlikely to be fixed and provide context to Support and Customer Success teams as necessary to help manage expectations.

## Why creating issues is important
Creating and properly crafting issues with descriptions and tagging is important because use them to:

- **Generate release notes** - We generate our release notes off the Issues linked to the code. We want to tell our customers all the great things we are doing.
- **See what’s changed** - When we find something odd or a ticket comes in it helps to look at what recently changed.
- **Track progress** - Customers and staff subscribe to Issues to stay informed on it’s progress
- **Reduce effort** - It provides context for future us. For current us it avoids duplication of effort when bugs are found.
- **Generate metrics** - Is our quality good? Do we have enough people? How responsive are we?

## Which repository should I create the issue in?

If you want to track an Issue that doesn't deserve public attention, you can track it with an Issue in the [ResearchAndDevelopment repository](https://github.com/OctopusDeploy/ResearchAndDevelopment/issues).

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

When in doubt, raise the issue to this repo for triage and it will be redirected if necessary. 

## How to raise an issue

Make use of the issue templates and fill out all of the sections. The more specific details you can provide, the better. For example, providing links to the original reports for bugs (e.g. support tickets), details of how to replicate the issue, and known workarounds wherever possible will help affected customers, and help speed up a resolution. 

### Labels

Refer to shortcut tickets as the source of truth for labels.

### Team Assignment

Please refer to the connected shortcut ticket to see team ownership. The [R&D Single Front Door](https://octopushq.atlassian.net/l/cp/eqs6uxfZ) and [Ownership Map](https://whimsical.com/NzbiD4HJyvhC9jNJNfS6TG) is used to guide this choice.

If in doubt, contact the Fire and Motion team. For more details on each team, see their [team page](https://octopushq.atlassian.net/wiki/spaces/RND/pages/1817084067/Teams)

## Transferring to a different Repo
Use GitHub’s [Transfer Issue](https://docs.github.com/en/issues/tracking-your-work-with-issues/transferring-an-issue-to-another-repository) feature. If transferring from private to public repo, make sure you have scrubbed confidential information (e.g. customer names).

## Release Note generation

It's important that we have good release notes with each build (we never seem to get into trouble for having too many release notes).

We automatically create Release Notes in markdown by querying the public GitHub Issues linked to PRs that form part of a Release.

We scan the Comments of an Issue for one beginning with a specific string: `Release Note: ` (or any other defined in the source) and use that for the Release Note, otherwise, we'll use the Issue Title.
