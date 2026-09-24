---
title: Reporting a bug
permalink: /contribute/report-a-bug/
---

Bugs affecting upstream QEMU releases should be filed at our
[bug tracker](https://gitlab.com/qemu-project/qemu/-/issues), which is hosted
on GitLab, taking into account the following guidance.

* Use the provided GitLab issue template, filling in all
  requested pieces of information that are relevant to the
  discovered bug.

* Bugs which are suspected, or known, to have security implications
  **must** be marked as "*confidential*" prior to submitting the
  disclosure. Consult the [security process](../security-process)
  for further guidance on security issue handling.

* Reproduce the problem with the latest upstream QEMU release.
  Reports against older versions may not be acted upon with
  with the same priority.

* Problems that have only been demonstrated with an release
  packaged by an OS distribution vendor must be either reported
  to the vendor's own bug tracker instead, or reproduced with
  an upstream QEMU build prior to submission.

* If any automated tools (AI/LLM based, traditional static
  analysis, or fuzzers) were used to discover the issue, the
  reporter is required to declare this at the start of the
  bug report. Users of such tools are required to perform
  triage of their output to validate all findings and reproducer
  scenarios prior to submitting a bug report.

* QEMU policy forbids the bulk filing of large numbers of
  bug disclosures that were generated with automated tools
  (AI/LLM, static analysis, fuzzers). Such actions are not
  a benefit to the project, placing an unsustainable burden
  on maintainers.

  * **No more than 5 bug/security reports, discovered
    with assistance of automated tools, are permitted
    to be filed per week, per reporter.**
  * **No more than 10 bug/security reports, discovered
    with assistance of automated tools are permitted
    to be open at any time, per reporter.**
  * Reporters must refrain from filing any reports
    that would cause these thresholds to be exceeded
    without first obtaining explicit prior permission
    from project maintainers.
  * Reporters are **required** to respond to triage
    comments from maintainers on bugs related to
    automated tools on a timely basis.
  * If at any time, the project maintainers request
    the reporter to stop filing bug reports discovered
    with assistance of automated tools, this must be
    honoured.

  Ignoring any of the above rules may lead to the bugs being
  mass closed without further triage, even if valid reports.
  In cases where the filing limits are grossly exceeded,
  the reporter's GitLab account may be reported for abuse
  (spam), potentially leading to termination.

  If intending to file large numbers of bug disclosures
  in aggregate, reporters are expected to invest their
  time in writing patches, providing the patches for
  review, and then further responding to feedback and
  iterating on the patches until a maintainer accepts
  them for it.

* Reproduce the problem directly with a QEMU command-line. Avoid
  frontends and management stacks, to ensure that the bug is in
  QEMU itself and not in a frontend and make it easier for
  maintainers to understand the problematic scenario.

* If patches are available for an issue, they should be sent to
  the mailing list according to QEMU's [patch submissions
  guidelines](../submit-a-patch/). QEMU does not use a merge
  request workflow for contribution.

* If the problem is believed to lie in the KVM kernel module,
  following the [KVM wiki bug report](https://www.linux-kvm.org/page/Bugs)
  guidance to submit an issue to the kernel bug tracker.
