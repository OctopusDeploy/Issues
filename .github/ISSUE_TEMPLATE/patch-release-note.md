---
name: Patch Release Note
about: This issue represents the fact we have shipped a bug fix for a previous, supported
  release.
title: "[Copy the title from the core issue describing this bug]"
labels: kind/LTS-patch-release-note
assignees: ''

---

# Tips for success

- Copy the title from the "core issue" which describes the bug in more detail. This issue points to the core issue and adds a release note.
- Assign this issue to the single milestone appropriate for the patch. If you are shipping a fix for `2019.3` in the patch `2019.3.5`, assign the issue to a milestone called `2019.3.5`.
- Tag this issue with the single `LTS/major.minor` tag appropriate for the patch. If you are shipping a fix for `2019.3` apply the tag `LTS/2019.3`.
- Add a comment with the prefix `Release Note:`. This comment will be used to build the release notes when you ship the patch.
- Delete all this help text, and keep the templated section below.

# Replace the details in this example and delete everything else including this heading

#1 also affected `2019.3`. The fix has been shipped in the patch indicated by the milestone. If you are using `2019.3` we highly recommend applying this patch.

Learn about [Releases of Octopus Deploy Server](https://g.octopushq.com/longtermsupport).
