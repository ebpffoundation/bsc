# Meetings & Meeting Notes

Color codes:

-   **Black:** pre-meeting / topics for meeting

-   **Red:** post-meeting / results from discussions

-   **Green:** action item (AI) for individual BSC members

**Important:** All BSC members are expected to regularly check the
summarized meeting notes from the BSC chair (the chair will notify the
BSC mailing list once notes are cleaned up), and members either propose
changes to the notes or add comments on some of the sections if
something was not correctly represented from the meeting. The BSC chair
will then finalize and notify the GB chair about it. Silent deadline is
one week after the BSC meeting took place.

## Meeting \#8 - 2022-02-09

-   **Duration:**

    -   **1h**

-   **Chair:**

    -   **Andrii Nakryiko**

-   **Participants:**

    -   **Andrii Nakryiko**

    -   **Brendan Gregg**

    -   **Daniel Borkmann**

    -   **Dave Thaler**

    -   **KP Singh**

    -   **Joe Stringer**

    -   **Alexei Starovoitov**

    -   **External:**

        -   **John Fastabend (Isovalent)**

        -   **Daniel Havey (Microsoft)**

        -   **Sophie Schmieg (Google)**

        -   **Jason (Google)**

        -   **Devjit (Google Security)**

-   Intros

-   KP and Alexei giving overview of previous discussion on BPF signing
    and trust

    -   Various places where things can be signed

    -   Chain of trust problem

    -   Dave gives overview on hypervisor type 1 and 2 and how HECI
        mechanism works by signing any executable memory page.

-   Passing baton to guests to explain their use cases and requirements

    -   John Fastabend prefers to have a flexibility to decide on
        policy. E.g., be strict during early boot process, but allow
        various classes after the system booted.

        -   Bpftrace is important use case, blocking it means losing a
            lot of BPF advantage

        -   Suspects a lot of realistic use case involved some amount of
            dynamism in BPF program generation

        -   Dave Thaler: who would be controlling this policy?

            -   A: platform team, there could be even multiple tiers of
                policies; all this is driven by config

        -   Q: for dynamic code loading cases why can't this be
            pre-signed

            -   A: the code can be generated on the fly by local daemon,
                so no way to pre-sign

        -   Do we need to support removing trust for some vendors?

        -   Brendan: dynamic programs for zero day/sec issue detection
            should still work as use case (security team)

        -   Alexei: would be great to have something like WWW's model
            for HTTPS certificates

        -   Dave: there should be multiple root anchor keys to prevent
            vendor buy-in

        -   Sophie: what about key rotation and expiration?

        -   Jason: crypto agility for post-quantum era

        -   X.509 discussion, do we need something simpler or better to
            stick to complicated x.509 which is already used by the
            kernel

        -   Dave: whatever the signing mechanism, ideally it's
            cross-platform

            -   Sophie: there are attacks that use signed certificate
                from one platform on another one and exploits slight
                platform-specific differences for an attack

        -   Daniel: how to support delegated trust (e.g., bpftrace is
            trusted and thus all generated progs by bpftrace should be
            trusted)

            -   Individual JITed program's trust should be revoked
                independently from the trusted JITer (bpftrace)

                -   Could be done via certificate revocation

                -   Could be done by changing a policy on what the JITer
                    can do

        -   Dave: summarizing use case about chain of gatekeepers with
            hypervisor enforcing which kernels can be loaded, kernel
            enforcing which boot-time gatekeeper ebpf program can be
            started, which in turn controls which user-space apps are
            allowed/trusted, and those in turn might be enforcing which
            BPF programs are to be trusted

        -   Live policy changes can be additive, but subtractive (like
            revocation) would require a reboot since may already be in a
            bad state

        -   KP: what do we sign? User-space app with BPF object
            embedded?

            -   John: for dynamically JITed programs it doesn't matter
                because we already trust JITer

        -   John: we can combine both gatekeeper app with pre-populated
            static key ring for something more static and less
            privileged.

        -   John and Dave: multiple gatekeepers are necessary (Google
            has its own, Cilium has its own, etc)

            -   Andrii: should multiple gate keepers be at one system

                -   John: let's allow just one

## Meeting \#7 - 2022-01-26

-   Participants

    -   Brendan Gregg

    -   Daniel Borkmann

    -   Dave Thaler

    -   KP Singh

    -   Joe Stringer

    -   Lorenz Bauer

    -   Alexei Starovoitov

    -   [[Andrii]{.ul} [Nakryiko]{.ul}](mailto:andrii@kernel.org)

-   Recap of L3AF

    -   GH PR merged

-   BPF Steering (?) Committee

    -   KP took part as representative of the BSC

        -   Ownership of ebpf.io

        -   Rename "ebpf projects" -\> "ebpf landscape"

            -   There is a desire to distinguish BPF foundation projects
                from other things

    -   We should set up a dedicated group that cares about ebpf.io
        (Alexei)

        -   [[dthaler\@microsoft.com]{.ul}](mailto:dthaler@microsoft.com)

        -   [[daniel\@iogearbox.net]{.ul}](mailto:daniel@iogearbox.net)

        -   Who else?

            -   Linux Foundation "outreach people"?

        -   Invert the model: have the outreach committee make
            suggestions that we can vote on.

-   Signed Programs (Alexei)

    -   Ask is from big distros, large companies (Amazon)

    -   Only knob right now: disable BPF entirely. There is a risk that
        others will solve this problem badly for us.

    -   Two types:

        -   dynamic generation of BPF (cilium, bpftrace)

        -   modification of programs (libbpf CO-RE)

    -   What is our position on signing programs?

        -   KP

            -   We need to be able to trust binaries and BPF programs

            -   Trusted binary: may load unsigned BPF

            -   Untrusted binary: may load signed BPF

            -   Trust doesn't have to mean signing: could be apparmor,
                selinux, etc.

            -   How would signing of BPF programs even work if they are
                shipped as part of a binary?

            -   Distro signing is scary

        -   Dave

            -   Windows and Linux distro (CBL-Mariner)

            -   Windows: change of OS memory protected by hypervisor
                (HVCI)

                -   Executable pages (native code) have to be signed

            -   Three ways to sign:

                -   Sign JITed code (checked by hypervisor)

                -   Sign BPF bytecode (checked by kernel, not
                    hypervisor) (RFC by Matteo Croce)

                -   Sign package that contains BPF and any user space
                    app (L3AF repository use case)

            -   Tangent: if signing happens offline, we could also
                verify "offline" (REST API for example)

        -   Alexei: Let's not spend much time solving for interpreters.
            Interpreters are wrought with security concerns. Assume
            there is no interpreter.

        -   Lorenz

            -   What about developers of eBPF being shut out by Red Hat,
                etc.?

            -   Alexei: all of these things will inevitably be shut down
                by signed BPF programs.

        -   Andrii

            -   Trusting user space binary is more general than trusting
                BPF programs

            -   Will Red Hat actually go ahead and come up with a
                proprietary way of doing things?

                -   Alexei thinks yes

        -   What if an LSM is the arbitrator of which programs may be
            loaded? (KP)

            -   Have a list of hashes of allowed programs and check
                against that

        -   Signing BPF bytecode could allow novel uses: serverless,
            enabled by default on Windows, macOS, etc.

        -   Integrity vs singing: how should the root of trust work? Any
            experts in our companies we can reach out to?

        -   Organise an open forum / office hours on trust / signing
            (w/e) where stakeholders can voice their concerns

            -   Are there people that have solved a similar problem
                before?

            -   Operating systems

            -   Distributors

            -   Tool developers

            -   This will happen on the next BSC meeting

-   Cross-project engagement - BSC not involved eg with LLVM (Alexei)

    -   GCC people want to standardise BTF before adding support

    -   LLVM wants more formal engagement from BPF

        -   Is eBPF a standalone dialect of C?

        -   Clean up BPF documentation

    -   Open up BSC mailing list to the public and CC the list for such
        discussions

        -   Allow anyone to send to the list, not subscribe to it

        -   AI: [[Daniel]{.ul}
            [Borkmann]{.ul}](mailto:daniel@iogearbox.net) follow up
            \[DONE\]

-   Extension of cgroup files (KP)

    -   Dynamic file creation on sys , proc, cgroup

## Meeting \#6 - 2022-01-12

-   **Duration:**

    -   **1h**

-   **Chair:**

    -   **Alexei Starovoitov**

-   **Participants:**

    -   **Andrii Nakryiko**

    -   **Brendan Gregg**

    -   **Daniel Borkmann**

    -   **Dave Thaler**

    -   **KP Singh**

    -   **Joe Stringer**

    -   **Jason Niesz (Walmart, L3AF maintainer)**

    -   **Brian Merrell (Walmart, L3AF maintainer)**

    -   **Louis Illuzzi (LF Networking, PM for L3AF)**

    -   **Vicky Brasseur (Wipro CTO, L3AF TSC member)**

-   Jason presented L3AF

    -   Some questions asked:

    -   Who is authoritative for what programs run on the node? (answer:
        admin of machine, who does so via a JSON config file)

    -   Would you really trust a public program repository? (unclear,
        L3AF TSC is discussing same question, cases today use private
        ones with paths specified by machine admin)

    -   Any coordination with Kubernetes or OpenStack? (today is
        standalone, may integrate with other things in future)

    -   How do you config/customize ebpf programs? (today Walmart's
        programs used with L3AF factor config/customization to be done
        via maps)

    -   Any standard way of communicating with userspace, like protobufs
        etc? (not yet but L3AF would like to go in that direction)

    -   What about gatekeeping, i.e. reject "bad" tools that were
        rejected by kernel patch requests? Compare to bcc tool repo.
        Private program repositories are safer, public repository is
        dangerous/risky if just accepted (could just be reference
        implementations, always use private repos from L3AFD?)

    -   What happens if something other than L3AFD tries to deploy an
        ebpf program to the kernel? (today, can interfere, L3AF TSC
        should discuss) can you have SELinux like functionality or just
        use SELinux to control?

    -   How can you disincent/prevent admins from pointing to a public
        repo and being unsafe?

    -   How does it differ from the
        [[bumblebee]{.ul}](https://github.com/solo-io/bumblebee)
        project?

-   AI(BSC): Deal with L3AF PR for presenting on the website. Note:
    Scoped to l3afd.

-   AI(L3AF TSC): Discuss dangers of public repo, gatekeeping

-   AI(L3AF TSC): Map formats, userspace\<-\>kernel communication
    formats, bundling vs. other orchestrators (eg k8s)

## 

## Meeting \#5 - 2021-12-08

-   **Duration:**

    -   **1h**

-   **Chair:**

    -   **KP SIngh**

-   **Participants:**

    -   **Joe Stringer**

    -   **Andrii Nakryiko**

    -   **Brendan Gregg**

    -   **Daniel Borkmann**

    -   **Dave Thaler**

    -   **KP Singh**

-   Projects with PRs waiting: [[Pull]{.ul} [requests]{.ul} [·]{.ul}
    [cilium/ebpf.io]{.ul}
    [(github.com)]{.ul}](https://github.com/cilium/ebpf.io/pulls) (10m)

    -   [[KP]{.ul} [Singh]{.ul}](mailto:kpsingh@chromium.org)is not
        listing the ones that have been already approved

    -   [[https://github.com/ebpf-io/ebpf.io/pull/150]{.ul}](https://github.com/ebpf-io/ebpf.io/pull/150)
        (LibXDP)

        -   What section does it belong to?

            -   BPF libraries is generic BPF

            -   Andrii: Vote to stick to core loading libraries

            -   Hybrid between the two user journey based split that was
                discussed.

            -   Consensus:

                -   Category: Applications

                -   State: Emerging

    -   [[https://github.com/ebpf-io/ebpf.io/pull/140]{.ul}](https://github.com/ebpf-io/ebpf.io/pull/140)
        (hBPF)

        -   Joe: One author, follows guidelines

        -   Would benefit from advertising / awareness

        -   Can we use our technical judgement to recommend projects and
            help them gain traction

        -   Daniel: Inspiration on what one can really do with eBPF

            -   If the project goes silent, we can possibly remove it

        -   Consensus: Merge it in "Core Infrastructure (emerging)"

    -   [[https://github.com/ebpf-io/ebpf.io/pull/154]{.ul}](https://github.com/ebpf-io/ebpf.io/pull/154)
        (L3AF)

        -   David and Lorenz have approved

        -   Joe: Technical question on how are we encouraging loading /
            distribution of eBPF programs

            -   Signing

            -   Repository of eBPF programs, like a store

            -   Orchestration of loading / distribution \[L3AF is in
                this category currently.

            -   One of the concerns is whether their technical direction
                shares the same vision as the BSC, and whether their
                eBPF store diverges communities

        -   We can have leaf people here, and talk to them

        -   Consensus: Invite L3AF folks to BSC for Jan 5th before
            making a call

    -   Other PRs postponed to next meeting

-   [[KP]{.ul} [Singh]{.ul}](mailto:kpsingh@chromium.org) Proposal to
    reduce the time spent on the eBPF Website discussions

    -   Ideas, invite people and discuss the next big things we can do
        in eBPF. e.g Interfacing with the scheduler

    -   What\'s the difference in scope between ebpf office hrs vs the
        BSC meeting?

    -   Possible axes on which scopes may be defined:

        -   a\) tactical (short term) vs strategic (long term
            direction/vision)

        -   b\) Q&A vs review of new proposals

        -   c\) Linux-specific vs not, or even specific to some other
            platform like Windows, hBPF, MacOS, etc.

    -   Proposal to invite people working on long-term direction
        projects (e.g. BPF signing)

        -   Gives us an opportunity to invite experts and improve
            technical direction

    -   Early contenders for invites:

        -   Signed BPF programs

        -   L3AF

            -   They have office hours (Wed's 8am Pacific time) which
                Dave has been attending

    -   Next meeting is canceled (too close to Holidays), meet again on
        January 5

**Action Items:**

-   Dave: Invite L3AF folks to the Jan 5th BSC meeting

-   KP: Comment on PRs

-   Someone: Check with Thomas about externally published meeting notes

## Meeting \#4 - 2021-11-24

Cancelled

## Meeting \#3 - 2021-11-10

-   **Duration:**

    -   **1h**

-   **Chair:**

    -   **Joe Stringer**

-   **Participants:**

    -   **Joe Stringer**

    -   **Andrii Nakryiko**

    -   **Brendan Gregg**

    -   **Daniel Borkmann**

    -   **Dave Thaler**

    -   **KP Singh**

-   **Review process for PRs to ebpf.io (10m)**

    -   **BSC coordination of review**

        -   **Every BSC member must approve? Two members? One member?**

        -   **Rotation over BSC member to assign "owner" who is
            responsible to take the item to BSC for discussion?**

    -   **Additional community assistance
        ([[Codeowners]{.ul}](https://github.com/ebpf-io/ebpf.io/pull/148)**
        [**[PR]{.ul}**](https://github.com/ebpf-io/ebpf.io/pull/148),
        [**[previous]{.ul}** **[Cilium]{.ul}**
        **[team]{.ul}**](https://github.com/orgs/cilium/teams/ebpfio)**)**

    -   **Brendan: Session' chair's job to look through some PRs before
        each meeting and figure out how to make incremental progress on
        the PR list.**

        -   **Opinion: Minimum number of approvals + time window**

            -   **Example, if a proposal is open for 1 week with 1
                approval from BSC and it's uncontroversial, merge it.**

                -   **Uncontroversial: Just merge.**

                    -   **Examples: Link fixes, typos.**

                -   **Discussion necessary: wait for next meeting.**

                    -   **Examples: New projects**

            -   **Goal: Anyone on BSC should be able to just merge
                uncontroversial items rather than waiting for the next
                meeting.**

    -   **Today: Repository admins may "merge". BSC members in general
        are not "Admin".**

        -   **Who *should* have merge rights?**

        -   **Daniel is OK to merge for now.**

    -   **Let's follow again with Thomas on Governance page for style?
        AI: Daniel \[DONE, pinged Thomas\]**

-   **Removing projects from the website (5m)**

    -   [**[GoBPF]{.ul}**](https://github.com/ebpf-io/ebpf.io/pull/119#issuecomment-853915089)
        [**[has]{.ul}**](https://github.com/ebpf-io/ebpf.io/pull/119#issuecomment-853915089)
        [**[low]{.ul}**](https://github.com/ebpf-io/ebpf.io/pull/119#issuecomment-853915089)
        [**[activity]{.ul}**](https://github.com/ebpf-io/ebpf.io/pull/119#issuecomment-853915089)

        -   **Last commit 6 months ago.**

        -   **Meets criteria 1/2/4 for emerging, but not 3 for major
            (maintained)**

            -   **Open issues / PRs with no review for 3 months?**

                -   **Trigger? After 3 months we can review it.**

        -   **Is there an "emeritus" status?**

            -   **Prefer not, if it's not maintained we do not need to
                archive it.**

        -   **Mature project: OK to stay. Emerging -\> Stopped emerging?
            Remove from the project listing.**

        -   **Also see:
            [[https://github.com/iovisor/gobpf/issues/304]{.ul}](https://github.com/iovisor/gobpf/issues/304)**

        -   **AI: Remove from the repository (Joe) \[DONE\]**

            -   [**[https://github.com/ebpf-io/ebpf.io/pull/155]{.ul}**](https://github.com/ebpf-io/ebpf.io/pull/155)

                -   **\[Daniel: Seems after the repo transfer I cannot
                    merge yet, pinged Thomas\]**

    -   **Shall we set a periodic reminder to review these? Or rely on
        community reports?**

        -   **Joe to add 6 month cadence reminder to raise projects for
            removal**

-   **General structuring going forward for the ebpf.io projects page
    (20m)**

    -   [**[Add]{.ul}** **[Major/Emerging]{.ul}** **[labels]{.ul}**
        **[PR]{.ul}** **[per]{.ul}** **[2021-10-27]{.ul}**
        **[discussion]{.ul}**](https://github.com/ebpf-io/ebpf.io/pull/153)

        -   **AI(Daniel/Thomas): Follow up with web design agency to
            improve CSS here**

            -   **\[Daniel: pinged Thomas\]**

        -   **AI: Thomas access to analytics e.g. how many views on
            projects etc**

            -   **\[Daniel: pinged Thomas\]**

        -   **We can merge this PR and then iterate further on top,
            rebase existing project proposals.**

            -   **AI(Dave): Next steps for moving text \[DONE, PR
                \#[[156]{.ul}](https://github.com/ebpf-io/ebpf.io/pull/156)\]**

        -   **AI(Daniel) Sketch up a proposal for the web agency to
            suggest how the projects should appear visually on the
            page**

    -   **Similar examples**

        -   [**[Envoy]{.ul}**](https://www.envoyproxy.io/community)

        -   [**[CNCF]{.ul}**
            **[Landscape]{.ul}**](https://landscape.cncf.io/)

-   **Projects with PRs waiting:
    [[Pull]{.ul}](https://github.com/cilium/ebpf.io/pulls)**
    [**[requests]{.ul}** **[·]{.ul}** **[cilium/ebpf.io]{.ul}**
    **[(github.com)]{.ul}**](https://github.com/cilium/ebpf.io/pulls)
    **(25m)**

    -   **Guidelines for new users on how to get started based on
        specific use cases (Brendan)**

        -   **AI(Brendan): Make a proposal so that we can review it**

            -   **Already posted on Slack, can be shared with those not
                on Slack**

        -   **How to get started / have success with eBPF.**

    -   **Kubearmor: AI Daniel to hit merge**

        -   **\[Daniel: Seems after the repo transfer I cannot merge
            yet, pinged Thomas\]**

    -   **[[Libbpfgo]{.ul}](https://github.com/cilium/ebpf.io/pull/119):
        Need to merge \#153 above then they can rebase.**

    -   **[[Aya]{.ul}](https://github.com/ebpf-io/ebpf.io/pull/136):**

        -   **Concern about which features are supported.**

        -   **Submission on ebpf.io seems OK. Start as emerging
            category. Will need a rebase against Dave's PR. AI(Dave) let
            them know to rebase \[DONE\]**

## Meeting \#2 - 2021-10-27

-   **Duration:**

    -   **1h**

-   **Chair:**

    -   **Dave Thaler**

-   **Participants:**

    -   **Alexei Starovoitov**

    -   **Andrii Nakryiko**

    -   **Daniel Borkmann**

    -   **Dave Thaler**

    -   **Joe Stringer**

    -   **KP Singh**

    -   **Lorenz Bauer**

    -   **Thomas Graf**

-   **Meeting duration**

    -   **This meeting and future meetings will target 1h (not 1.5h)
        duration**

-   **Where do we publish meeting notes?**

    -   **There is no eBPF Foundation github repo per se**

    -   **Who owns
        [[https://github.com/ebpf]{.ul}](https://github.com/ebpf) ? Can
        we use it?**

    -   **Do we use
        [[https://github.com/cilium/ebpf.io]{.ul}](https://github.com/cilium/ebpf.io)
        for now?**

    -   **Do we create a new org like
        [[https://github.com/ebpf-foundation]{.ul}](https://github.com/ebpf-foundation)
        ?**

    -   **Do we move
        [[https://github.com/cilium/ebpf.io]{.ul}](https://github.com/cilium/ebpf.io)
        under the foundation github org?**

        -   **There was agreement to move ebpf.io under a foundation
            github org. It was observed that someone had recently
            created
            [[https://github.com/ebpf-foundation]{.ul}](https://github.com/ebpf-foundation)
            but no one on the call knew who.**

        -   **We should add LF and eBPF BSC as well as admins of the
            ebpf foundation github org.**

        -   **Right now, Isovalent pays a third party for website
            work.**

        -   **We also need to move the
            [[https://github.com/orgs/cilium/teams/ebpf-bsc]{.ul}](https://github.com/orgs/cilium/teams/ebpf-bsc)
            group to the foundation github org.**

        -   **AI(Thomas) to move the ebpf.io repository to an ebpf
            foundation github org. \[DONE\]**

        -   **Should also arrange attribution for the existing work.**

    -   **Discussion on process for commenting on meeting notes**

        -   **Okay with everyone as mentioned above in paragraph under
            header ('important' section), Thomas can then move them to
            github repo**

        -   **There will be a deadline of 1 week to post
            comments/amendments to minutes.**

-   **Technical Project stages and submission procedures (Dave Thaler)**

    -   **Is the list of Technical Projects the same as, or different
        from, the list at [[eBPF]{.ul}](https://ebpf.io/projects)**
        [**[Projects]{.ul}**
        **[Directory]{.ul}**](https://ebpf.io/projects) **today? Dave's
        reading based on our charter is that it's [different]{.ul}.**

        -   **"BSC Projects", "Technical Projects", "eBPF Projects" in
            charter, presumably same, but different from eBPF Projects
            Directory which does not require trademark transfer (if any
            exist)?**

    -   **Should we distinguish between emerging vs major? Recommended?
        No distinction?**

        -   **CNCF comparable:
            [[toc/project_proposals.adoc]{.ul}](https://github.com/cncf/toc/blob/main/process/project_proposals.adoc)**
            [**[at]{.ul}** **[main]{.ul}** **[·]{.ul}**
            **[cncf/toc]{.ul}**
            **[(github.com)]{.ul}**](https://github.com/cncf/toc/blob/main/process/project_proposals.adoc)

        -   **CCC comparable:
            [[governance/project-progression-policy.md]{.ul}](https://github.com/confidential-computing/governance/blob/master/project-progression-policy.md)**
            [**[at]{.ul}** **[master]{.ul}** **[·]{.ul}**
            **[confidential-computing/governance]{.ul}**
            **[(github.com)]{.ul}**](https://github.com/confidential-computing/governance/blob/master/project-progression-policy.md)

        -   **At least for now, we will continue the Major vs Emerging
            distinction**

    -   **How should we verify that a submission meets the
        requirements?**

        -   **Ask requesters to use the PR description for anything that
            isn't easy to look up, such as justification for "major"
            such as: is it used in production**

        -   **\# contributors can be looked up in github, but \# users
            listed in github is not a good metric**

-   **General structuring going forward for the ebpf.io projects page
    (Daniel Borkmann)**

    -   **How do we structure this in an ideal way without convoluting
        the projects page too much?**

        -   **Major vs emerging is really a separate axis from
            categories (runtimes, libraries, applications, ...).**

        -   **For a first step, we should have major vs emerging within
            each category**

        -   **Bcc should move down**

        -   **AI(Andrii): create a PR to move bcc down the page as
            appropriate**

        -   **Top section should have label of "Applications"**

        -   **AI(Dave): create a PR to add Applications label \[DONE:
            https://github.com/ebpf-io/ebpf.io/pull/153\]**

    -   **Do we split into multiple pages or keep on one page?**

        -   **Consensus is yes there are two different audiences:
            developers (bpf libs, compiler, runtimes) vs apps (cilium,
            katran).**

            -   **bpftrace/bpftools is more like sysadmin.**

            -   **Bpftrace and bcctools can be used by sysadmin, so that
                page can talk about those aspects**

        -   **It is ok to list a project in two places with different
            descriptions, if two different things are combined in the
            same repo like in the bcc case**

        -   **Having lots of descriptions can get hard to read. Maybe
            use tabs? But if only one is shown, that may give a
            preselection bias, which we want to avoid. We do want
            descriptions to call out the essential features that are
            different from the other options in the same category.**

            -   **We should ask the web content team to figure out the
                UI details, and just give high level requirements to
                them.**

        -   **Steps in order: 1) add labels, 2) add libbpfgo once PR is
            updated, 3) add web content tabs or similar once there is an
            example of both major and emerging in the same category**

        -   **AI(Dave): Create a PR to add major/emerging labels per
            category \[DONE:
            https://github.com/ebpf-io/ebpf.io/pull/153\]**

    -   

-   **Projects with PRs waiting:
    [[Pull]{.ul}](https://github.com/cilium/ebpf.io/pulls)**
    [**[requests]{.ul}** **[·]{.ul}** **[cilium/ebpf.io]{.ul}**
    **[(github.com)]{.ul}**](https://github.com/cilium/ebpf.io/pulls)

    -   **The BSC discussed the oldest two PRs that proposed project
        additions:**

        -   **[[Kubearmor]{.ul}](https://github.com/cilium/ebpf.io/pull/119):
            meets the criteria for an emerging project.**

            -   **AI(BSC members): Approve PR if looks ok**

        -   **[[Libbpfgo]{.ul}](https://github.com/cilium/ebpf.io/pull/119):
            The PR is not ready to merge as is, since the project would
            fit the "emerging" requirements, but the Go libraries
            section being modified is in the Major not Emerging section.
            The overall page needs to be updated first. Also the PR is
            missing a description of libbpfgo, which would need to be
            added.**

## Meeting \#1 - 2021-10-13

-   **Duration:**

    -   **1.5h**

-   **Chair:**

    -   **Daniel Borkmann**

-   **State:**

    -   **Notes handed over to GB chair**

-   **Participants:**

    -   **Alexei Starovoitov**

    -   **Andrii Nakryiko**

    -   **Brendan Gregg**

    -   **Daniel Borkmann**

    -   **Dave Thaler**

    -   **Joe Stringer**

    -   **KP Singh**

    -   **Lorenz Bauer**

    -   **Thomas Graf**

-   **Decide on a regular meeting schedule, e.g. could be once a month
    starting from kickoff meeting or every two weeks. (Daniel
    Borkmann)**

    -   **We decided to meet bi-weekly, on the same day and in rotating
        time zones. This means the meeting time will alternate between
        7am Seattle time and 1pm Seattle time.**

        -   **AI: Daniel to send calendar update. \[DONE\]**

-   **Chair election process and timeline (Dave Thaler)**

    -   **Our charter states: "The BSC representatives will elect a
        chair to preside over meetings, ensure minutes are taken and
        drive the BSC agenda with input from the BSC representatives."**

    -   **Chair (the default answer per charter)? Chair + vice-chair?
        Co-chairs? Kidding? (should be simple but not needed answer
        short term, longer term explanation on call, but not urgent)
        Dave is all for "Minimum Viable Governance"!**

        -   **We decided for a rotating chair to preside over the
            meeting every 2 weeks in order to balance the overhead. The
            chair will round robin alphabetically (based on first
            name).**

            -   **AI: Daniel to create a list in this doc. \[DONE\]**

        -   **The GB chair's responsibility is to publish the meeting
            notes handed over by the chair for the public and/or GB.**

            -   **The notes will be published in a Github repository.
                TBD e.g. we don't have a eBPF foundation Github org
                yet.**

        -   **The role of the BSC chair is to prepare the agenda for the
            upcoming BSC meeting, to take notes, and to have the members
            approve the notes.**

-   **eBPF Foundation recap and BSC goals (Lorenz Bauer)**

    -   **Since the foundation has been founded, 2 additional members
        joined, 4 new members are in the onboarding phase. Current
        budget is multiple hundred-thousand dollars. There are recurring
        BSC and GB meetings, each has an email list, and G drive. It's
        on the BSC to define the direction of BPF and how to use the
        foundation budget (with GB approval).**

-   **Requirements around use of eBPF bee logo (Dave Thaler)**

    -   **Is this question one for the governing board or the BSC? I
        suspect it's ultimately a board decision. (Dave Thaler)**

        -   **The official eBPF logo has been donated by Isovalent to
            the Linux Foundation (LF). During the BSC meeting, we
            discussed and elaborated on various options around logo
            usage guidelines (example:
            [[CNCF]{.ul}](https://www.cncf.io/brand-guidelines/)**
            [**[logo]{.ul}** **[usage]{.ul}**
            **[guidelines]{.ul}**](https://www.cncf.io/brand-guidelines/)
            **built upon LF brand guidelines).**

        -   **BSC decided to build upon
            [[LF]{.ul}](https://www.linuxfoundation.org/brand-guidelines/)**
            [**[brand]{.ul}**
            **[guidelines]{.ul}**](https://www.linuxfoundation.org/brand-guidelines/)
            **as well for the eBPF logo / brand.**

            -   **It is up to the eBPF Foundation to report logo abuse
                to the LF, e.g. if the composition of the eBPF logo has
                been modified in context of some commercial / non-open
                source product, vendor or event. The brand guidelines
                protect the composition of the bee logo. Technically, it
                may be considered a new logo if the eBee is taken and
                added/modified with other elements (Example: variations
                of the Golang gopher logo from Golang community).**

        -   **AI: Thomas to get back with logo variants and a set of
            assets in PNG + SVG format that we can put on the ebpf.io
            website for download as well as setting up a
            [[https://ebpf.io/brand-guidelines/]{.ul}](https://ebpf.io/brand-guidelines/)
            page based on LF brand guidelines.**

        -   **Example of LF not following LF guidelines :)
            [[https://events.linuxfoundation.org/cloud-native-ebpf-day-north-america]{.ul}](https://events.linuxfoundation.org/cloud-native-ebpf-day-north-america)
            (The eBPF bee logo has color changed, and the one used in
            posters on site had yet another color scheme)**

```{=html}
<!-- -->
```
-   **The charter mentions "Technical Projects", "eBPF Projects", and
    "BSC Projects". Is there a difference? (Dave Thaler)**

    -   **The definition of the three was not entirely clear and it was
        stated that one of the wording was used in a last minute
        amendment by LF folks.**

    -   **How can we fix the charter? Procedure: We create a redline
        version with the changes. We vote on it. It passes 70%. Thomas
        can send it to Todd (LF). LF lawyers review it. Potentially
        suggest changes. We vote on the changes. We update the
        website.**

    -   **AI: Thomas to send a charter amendment proposal that BSC can
        vote on.**

    -   **Also the question came up, can a project be in multiple
        foundations e.g. eBPF and CNCF? The answer is yes, as there is
        no requirement to transfer e.g. ownership rights.**

-   **Technical Project stages and submission procedures (Dave Thaler)**

    -   **Is the list of Technical Projects the same as, or different
        from, the list at [[eBPF]{.ul}](https://ebpf.io/projects)**
        [**[Projects]{.ul}**
        **[Directory]{.ul}**](https://ebpf.io/projects) **today? Dave's
        reading based on our charter is that it's [different]{.ul}.**

    -   **General structuring going forward for the ebpf.io projects
        page (Daniel Borkmann)**

        -   **Currently, there are** [**[5]{.ul}** **[pull]{.ul}**
            **[requests]{.ul}**](https://github.com/cilium/ebpf.io/pulls)
            **for eBPF related projects that would like to be added to
            the [[eBPF]{.ul}](https://ebpf.io/projects)**
            [**[projects]{.ul}**
            **[page]{.ul}**](https://ebpf.io/projects)**. Additionally,
            we have the terminology of "technical projects" versus "eBPF
            projects". The ebpf.io website currently uses "major
            projects" versus "emerging projects" as well as "core
            infrastructure" and "eBPF libraries". Given the pull
            requests which are to be decided, there is a bigger question
            about how the eBPF projects page should be restructured to
            better reflect the current landscape.**

            -   **The question was brought up on whether a
                category-based approach would be a better fit. The
                [[CNCF]{.ul}](https://landscape.cncf.io/)**
                **[[Landscape]{.ul}](https://landscape.cncf.io/) shows
                an example of how to categorize projects. Also, the
                question came up on the maturity of projects. For
                example, should a new eBPF library which only has seen a
                few users but is under active development be listed next
                to the existing libraries (Example Brendan brought up:
                Aya vs libbpf-rs).**

            -   **How do we determine the maturity / production
                readiness of the project for user recommendation? An
                example was brought up that we could have a "recommended
                projects" tag.**

        -   **Are there any indicators for projects that may not be
            appropriate for listing on the website?**

            -   **Context can be very important. For example, a project
                aiming to rewrite everything could be good if it is
                collaborative, or could be bad if it is aiming to fork
                and divide the community.**

            -   **Also, malware using eBPF would not be considered
                appropriate.**

        -   **We discussed the minimum bar for projects to be listed. If
            there are 5 projects that achieve the same goals and fit to
            requirements 1/2/4 (the
            [["Requirements]{.ul}](https://ebpf.io/projects)**
            [**[for]{.ul}** **[a]{.ul}** **[project]{.ul}**
            **[to]{.ul}** **[be]{.ul}**
            **[listed"]{.ul}**](https://ebpf.io/projects)**) on the
            project criteria, is that good enough to include all of
            them?**

            -   **It was suggested that a project must be actively
                maintained (e.g. fixing bugs that are reported).**

            -   **There may also be a notion of subjective element to
                admitting projects to the eBPF.io projects page, e.g.
                "the BSC reserves the right to add or remove a
                project".**

            -   **Overall some of the listed requirements need to be
                reworked and generally refined and could be more
                inclusive or better reflect structuring of the projects
                page, for example, when there are 5 libraries for the
                same language, do we list all of them and which one do
                we recommend, etc.**

        -   **In terms of the eBPF projects page we concluded for now
            that it needs a rework, but we did not conclude yet on how
            concrete next steps will look like. The discussion is
            expected to continue in the next BSC meeting(s). We agreed
            to make it a high priority item on the agenda.**

-   **The question came up during the discussion of the eBPF projects
    page with regards to who has rights to review and/or approve eBPF.io
    pull requests.**

    -   **AI: Joe and Daniel to collect all Github handles from BSC
        members and to add handles to the project. \[DONE\]**
