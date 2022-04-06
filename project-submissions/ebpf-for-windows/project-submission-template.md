## Instructions
1.  Review the [Project Progression Policy](project-progression-policy.md).
2.  Send an email to the eBPF Steering Committee <bsc@ebpf.io> using the following template and attaching any supporting documentation. Any non-applicable response can be listed as N/A.
3.  For any questions or comments on this process please email bsc@ebpf.io.

## Project Proposal Template

### General Information
1.1. Name of Project

eBPF for Windows

1.2. Project Description (what it does, why it is valuable, origin and history)

eBPF for Windows allows using existing eBPF toolchains and APIs familiar in the Linux ecosystem
to be used on top of Windows. That is, this project takes existing eBPF projects as submodules
and adds the layer in between to make them run on top of Windows.

An architectural overview of the eBPF for Windows runtime is at
https://github.com/microsoft/ebpf-for-windows#architectural-overview

The project was first announced in May 2021 in the blog at
https://cloudblogs.microsoft.com/opensource/2021/05/10/making-ebpf-work-on-windows/
which included the statement that it "is intended to eventually reside in a community-governed
foundation in the eBPF ecosystem", and this submission contributes it according to that intent.

1.3. How does this project align with the Foundation's Mission Statement to encourage/foster the deployment and use of eBPF in the industry (e.g., not merely allow using eBPF as an option)

The eBPF for Windows project expands the applicability of eBPF to also apply to Windows,
and thus directly facilitates more deployment and use of eBPF.

1.4. Project website URL

https://microsoft.github.io/ebpf-for-windows/

1.5. Social media accounts, if any

None

### Legal Information
2.1. Project Logo URL or attachment (Vector Graphic: SVG, EPS), if any.

https://github.com/ebpf-io/ebpf.io/blob/master/src/assets/projects-logos/eBPF%20for%20Windows%20logo.png

2.2. Project license.  We recommend an [OSI-approved license](https://opensource.org/licenses), so if the license is not one on the list, explain why.

MIT

2.3. Existing financial sponsorship, if any.

Funded by Microsoft

2.4. Trademark status, if any.

None, but the name includes Windows, which is a trademark of Microsoft

2.5. Proposed Technical Charter, based on the [template](Technical%20Charter%20%28custom+data%29%20--%20LF%20Projects,%20LLC%204-10-2019%20FINAL.docx).
Include doc as attachment or give URL of doc.  It is ok to change the
text (e.g., "Technical Steering Committee") to match the actual structure of
the project; projects are free to use whatever governance structure they want.

* [Technical Charter](TechnicalCharter.docx)

### Technical Information
3.1. High level assessment of project synergy with any existing projects under the eBPF Foundation, including how the project compliments/overlaps with existing projects, and potential ways to harmonize over time. Responses may be included both inline and/or in accompanying documentation.

There are no existing projects under the eBPF Foundation.

It uses the following eBPF landscape projects:

* [uBPF](https://github.com/iovisor/ubpf)
* [PREVAIL verifier](https://github.com/vbpf/ebpf-verifier)
* [libbpf](https://github.com/libbpf/libbpf)
* [bpftool](https://github.com/libbpf/bpftool)

3.2. Project Code of Conduct URL.  We recommend one based on the [Contributor Covenant v2.0](https://www.contributor-covenant.org/version/2/0/code_of_conduct/) or the [LF Projects Code of Conduct](https://lfprojects.org/policies/code-of-conduct/).

Currently the project uses
https://github.com/microsoft/.github/blob/main/CODE_OF_CONDUCT.md
which is based on Contributor Covenant v2.0.

3.3. Source control URL

https://github.com/microsoft/ebpf-for-windows

3.4. Issue tracker URL

https://github.com/microsoft/ebpf-for-windows/issues

3.5. External dependencies (including licenses, and indicate whether each is a build time or runtime dependency)

Runtime dependencies:

* PREVAIL verifier: Apache-2.0
* ELFIO library: MIT
* uBPF project: Apache-2.0
* bpftool: GPL-2.0-only OR BSD-2-Clause
* libbpf: LGPL-2.1 OR BSD-2-Clause
* https://github.com/takamin/win-c: MIT
* https://github.com/trailofbits/pe-parse: MIT
* https://github.com/ytakano/radix_tree: BSD-2-Clause

Build/test dependencies:
* Catch2: BSL-1.0
* https://github.com/SergiusTheBest/FindWDK: BSD-3-Clause
* OpenCppCoverage (used in binary form): GPL-3.0

3.6. Standards implemented by the project, if any. Include links to any such standards.

No formal standards.  It does adhere to bpf de facto standards such as:
* https://github.com/iovisor/bpf-docs/blob/master/eBPF.md
* https://github.com/iovisor/bpf-docs/blob/master/bpf_helpers.rst

3.7. Release methodology and mechanics

There have been no releases yet.

3.8. List of project's official communication channels (slack, irc, mailing lists)

Slack channel:
https://cilium.slack.com/messages/ebpf-for-windows

Discussions also happen via github discussions at
https://github.com/microsoft/ebpf-for-windows/discussions

And at the weekly ebpf for windows office hours / triage meeting
https://github.com/microsoft/ebpf-for-windows/discussions/427

3.9. Project Security Response Policy for handling any vulnerabilities reported

https://github.com/microsoft/ebpf-for-windows/blob/main/docs/SECURITY.md

3.10. Expected budget request.  See [Project Benefits](project-progression-policy.md#benefits-of-being-a-recognized-foundation-project) for items that may be requested for potential support.

At some point later this year, the project expects to need a code coverage tool that
supports Windows kernel code.  To our knowledge this is only available in commercial
products such as [Qt](https://www.qt.io/pricing) or [Bullseye](https://www.bullseye.com/cgi-bin/store).

Currently Microsoft hosts github CI/CD resources, and if contributed to the consortium
then we expect that the project should out from under the Microsoft organization in github.
If the free github account is not sufficient for CI/CD runs in the future, we expect
that the Foundation would also cover a github organizational account for Foundation
projects.

3.11. Any additional information the BSC and Board should take into consideration when reviewing your proposal.
