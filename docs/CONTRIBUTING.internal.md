# How we use GitHub Issues

> Note: this page is intended for **Octopus team members only**. If you're an Octopus user and you've found a bug or something isn't working, please get in touch with [our support team](https://octopus.com/support) instead.

We use this public GitHub repository as a way to communicate with our community about what we are working on for the core Octopus product.

Different teams across Octopus use the public issues in this repository for the following purposes:

- **Engineers**: Use public issues for linking Pull Requests. This helps with automatic release note generation. Most private issues go to the [ResearchAndDevelopment issue list](https://github.com/OctopusDeploy/ResearchAndDevelopment/issues).
- **Support** and **Customer Success** teams:
  - If you want someone to address an issue, you still need to bring it to the attention of the appropriate team internally, see below.
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

The following conventions are in use across our repositories

- `team/<team>` - The team that is currently responsible for the Issue in a shared repository
- `state/triage` - New issues that have not yet been triaged by the team
- `priority/p1` and `priority/p2` - P1 and P2 issues, which are the most severe
- `kind/bug` - Bugs, defects, etc
- `kind/feature` - Features, additions, improvements and enhancements
- `closed/wontfix` - It’s a problem, but we don’t intend to fix it due to constraints
- `closed/duplicate` - This was the same as another issue
- `closed/invalid` - Could not reproduce, or was deemed to not be a problem

Team’s may also choose to add their own labels to manage their Issues

### Team Assignment

Each new Issue in a shared repository should have a `team/<team>` tag so that we 
Once you've created an issue, you still need to raise it with the relevant team internally.

_Future: We will automate this_


## Transferring to a different Repo
Use GitHub’s [Transfer Issue](https://docs.github.com/en/issues/tracking-your-work-with-issues/transferring-an-issue-to-another-repository) feature. If transferring from private to public repo, make sure you have scrubbed confidential information (e.g. customer names).

## Release Note generation

It's important that we have good release notes with each build (we never seem to get into trouble for having too many release notes).

We automatically create Release Notes in markdown by querying the public GitHub Issues linked to PRs that form part of a Release.

We scan the Comments of an Issue for one beginning with a specific string: `Release Note: ` (or any other defined in the source) and use that for the Release Note, otherwise, we'll use the Issue Title.

## GitHub Milestones deprecated

We used to create multiple issues for each bug and use GitHub Milestones to group Issues into a Release. Now that OctoNotes is smarter and Release Note generation is easier, we don't use milestones anymore, and we create a single issue per bug. 
