---
name: Patch Release Note
about: This issue represents the fact we have shipped a bug fix for a previous, supported
  release.
title: "[Copy the title from the core issue describing this bug]"
labels: kind/patch-release-note
assignees: ''

---

# Tips for success

- Copy the title from the "core issue" which describes the bug in more detail. This issue points to the core issue and adds a release note.
- Assign this issue to the single milestone appropriate for the patch. If you are shipping a fix for `2020.2` in the patch `2020.2.5`, assign the issue to a milestone called `2020.2.5`.
- Tag this issue with the single `release/major.minor` tag appropriate for the patch. If you are shipping a fix for `2020.2` apply the tag `release/2020.2`.
- Add a comment with the prefix `Release Note:`. This comment will be used to build the release notes when you ship the patch.
- Delete all this help text, and keep the templated section below.

# Replace the details in this example and delete everything else including this heading

#1 also affected `2020.2`. The fix has been shipped in the patch indicated by the milestone. If you are using `2020.2` we highly recommend applying this patch.

Learn about [Releases of Octopus Deploy Server](https://g.octopushq.com/longtermsupport).
