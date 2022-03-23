## I. Overview
This governance policy describes how an open source project can formally join the
eBPF Foundation via the
[Project Proposal Process](#ii-project-proposal-process). Projects that have joined the eBPF Foundation
(hereinafter "the Foundation") are
"Technical Projects". It describes what the criteria and expectations are for acceptance
as well as the [Annual Review Process](#iv-annual-review-process).

### Benefits of being a recognized Foundation project

Unlike non-Foundation projects in the eBPF project landscape at large, Technical Projects
can receive benefits that require budgeted funds from the eBPF Foundation, which is
[chartered](https://ebpf.io/charter/) to "spend funds in support of various open source,
open data and/or open standards projects relating to eBPF technologies, including infrastructure
and support initiatives related thereto".   By charter, the eBPF Steering Committee (BSC) is
responsible for "making recommendations to the Governing Board of resource priorities for Technical Projects".

Some ways a project can potentially benefit by becoming a Foundation-recognized project include:

1. Recognition: A Foundation project is recognized as meeting the goals of the Foundation.
2. Community: The Foundation is fostering a community of like-minded members.
3. Participation: Participate and lead in the ongoing development of the eBPF paradigm. All projects are assigned a [mentor](#v-mentors) to assist in the integration of the project to the Foundation and support beyond that.
4. Project Support: The Foundation can potentially provide limited funds to support project communication and infrastructure costs for CI/CD.
5. Internships: As part of Diversity and Inclusion, an intern could potentially be available to a project that commits to the list of "Mentor Responsibilities" on the [Outreachy mentor page](https://www.outreachy.org/mentor/).

## II. Project Proposal Process

### Introduction
This governance policy sets forth the proposal process for projects to be accepted into the Foundation. The process is the same for both existing projects which seek to move into the Foundation and new projects to be formed within the Foundation.

### Project Acceptance Process

The acceptance process is a three-stage process: a technical review with the
eBPF Steering Committee (BSC), legal submission to LF Projects, LLC,
and a vote by the Governing Board.

#### Technical Review

Projects are required to present their proposal at a BSC meeting.
This proposal should cover all the items in the [Project Submission Template](project-submission-template.md)
and the [Technical Charter template](Technical%20Charter%20%28custom+data%29%20--%20LF%20Projects,%20LLC%204-10-2019%20FINAL.docx).

The BSC may ask for changes to bring the project into better alignment with
the Foundation (adding a governance document to a
repository or adopting a Code of Conduct, for example). The project will
need to make these changes in order to progress further.

Projects are accepted via a majority vote
of BSC representatives present if quorum is reached or a majority of all
BSC representatives if voting by email.

Once a project passes Technical Review, the BSC will inform the Governing
Board that the submission proposal and Technical Charter are ready for the
next step.

#### Legal Submission

As noted in clause 8 of the [eBPF Foundation Charter](https://ebpf.io/charter/),
the Foundation requires that any trademarks be transferred to, or be available for
use by, LF Projects, LLC.  Even if no trademarks exist, the current
policy is that projects be submitted to LF Projects, LLC.

This submission entails sending the proposed Technical Charter (as reviewed
by the BSC), and a signed
[Project Contribution Agreement](LF%20Projects%20--%20Form%20of%20Trademark%20and%20Account%20Assignment.docx).
that assigns trademarks to LF Projects, LLC.

This submission might in some cases be done in parallel with, or even
before, Technical Review.  It is recommended though that this be
done after the Technical Review where practical.

#### Governing Board Vote

Once the Technical Review and Legal Submission steps are complete,
the Governing Board will review
the project proposal and the proposed Technical Charter.

Once any questions have been addressed, the Governing Board will
vote at its next available meeting.

Upon acceptance by the board, the project's approved Technical Charter
must be included in the project's main repository.  This document can
be in whatever format is most appropriate for the project, as long as
the content is the same as what was approved.

### Spin-off Projects ###

Technical Projects can create multiple subordinate projects (such as github repositories) that are governed under the structure agreed on and accepted by the BSC.

A project may want to spin out a new project because the original scope, governance or participants are distinctly different from the original agreed project charter, and not merely an organization of code or minor expansion of scope.
In this case a new project acceptance proposal, as defined above, should be submitted to the BSC.

## III. Requirements for Technical Projects

To be considered for acceptance, a project must meet the following requirements:

* It must minimally meet the requirements for a project to be listed as a "landscape" project at https://ebpf.io/projects
* A representative of the project must present an overview at a meeting of the BSC
* Its purpose must encourage/foster the deployment and use of eBPF in the industry, not merely allow use
  of eBPF as an option
* It must provide satisfactory answers to the other questions in the project submission template
* A Technical Charter must be presented to the BSC
* Any requests that would affect budget must be present to the BSC
* Upon acceptance, Technical Projects must list their status prominently on their website/README.

Technical Projects will be reviewed on an annual basis; they may also request a status review by submitting
a report to the BSC.

The BSC may assign a [mentor](#v-mentors) to a project to help them through the submission process and/or the annual review
process.  A mentor need not be a BSC member, but should be familiar with the process and be able to help others.

## IV. Annual Review Process

The BSC will conduct a review of each accepted project on an annual basis.

The review includes the following:

1. Review whether any answers to the project's submission template or Technical Charter have
   changed, and if so, review the new answers. A representative from the
   project is responsible for presenting any deltas to the template answers
   since the last review, if any. If there are no changes, there is nothing
   to review here.

2. Review any budget allocations relevant to the project, and whether any
   adjustments are needed.
   
3. Review any license scans provided by the Linux Foundation. Provide feedback
   on any outstanding issues and evaluate the scanning service from the
   project's perspective.

Projects are encouraged to proactively inform the BSC when something
changes that affects their submission template or Technical Charter (changing a License, security
reporting process, CoC, etc.), rather than waiting for the next annual review.

## V. Mentors

Responsibilities of a mentor include:

1. Help the project determine what needs to be reviewed by the BSC as part of
   the [Annual Review Process](#iv-annual-review-process).

2. Make sure the BSC is informed if something changes that affects the
   project's submission template (changing a License, security reporting process, CoC, etc.),
   rather than waiting for the next annual review.

3. Make sure the Technical Project is informed about any eBPF Foundation events
   of relevance, and the BSC is informed about non-Foundation events that
   the Technical Project is participating in.

4. In order to be a coach to the project maintainers, be familiar with open source best practices,
   including those for diversity and inclusion.
