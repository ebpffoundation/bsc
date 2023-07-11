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

## Meeting #38 - 2023-06-28

- **Duration:**
- **Chair: KP Singh**
- **Participants:**
  - **Dan Brown**
  - **KP Singh**
  - **Lisa Caywood**
  - **Alexei Starovoitov**
  - **Andrii Nakryiko**
  - **Dave Thaler**
  - **Joe Stringer**
  - **Brendan Gregg**
  - **Daniel Borkmann**
- **Agenda**
  - IETF WG update (Dave?)
    - Emails went out a week ago, official announcements sent out.
    - [IETF 117 Meeting Agenda](https://datatracker.ietf.org/meeting/117/agenda)
    - WG meets regularly
      - 1300 Pacific on 24th.
      - Announce so that folks can book.
      - The week is fixed, the slots may change.
    - Alexei: Please CC BPF@IETF and BPF kernel mailing list
      - AI(Dave): Forward email
  - BPF Docs repository under eBPF will move to IETF
    - [http://github.com/ietf-wg-bpf](http://github.com/ietf-wg-bpf)  is the github organization.
  - [Windows roadmap](https://docs.google.com/presentation/d/1bsGgk_bxuhHxCxc_UXxEa62R-prAX0eNpwkT19_OeFY/edit?usp=sharing) [KP Singh/Dave]
    - Updating slides live
    - bpf / [dtrace on windows](https://github.com/microsoft/DTrace-on-Windows) overlap
    - Alexei: How do we keep parity between BPF on Linux / Windows?
      - Contributions are welcome.
      - Reactive
      - Demand enables parity (similar with ARM).
      - Runtimes that use PREVAIL often use uBPF, so uBPF feature additions result in demand for corresponding PREVAIL additions (e.g., local calls).
      - Biased opinion: Standardization.
      - KP / Dave will work on updating the slides offline.
  - [Brendan] legal update
    - Met with Intel legal and Intel open source. Intel legal will draft a proposal, "3 sentences long" for meeting preamble. Set expectations clearly around the public nature of this meeting.
    - Protect the community and ecosystem from accidental exposure to proprietary information.
  - [Brendan] Purpose of admitting projects into the foundation + expected process.
    - Example process from Kubernetes for arranging sessions with a SIG: [https://github.com/kubernetes/sig-security/issues/91](https://github.com/kubernetes/sig-security/issues/91)
  - Announcement about [IETF | IETF blog & news](https://www.ietf.org/blog/all/)
  - [Lisa] Joint Board & BSC meeting July 12th
    - Group is meeting with the board to discuss the changes to the election process with the board in 2 weeks.
    - If there are any changes that need to be made, these need to be finalized before 12th July.
    - Brendan: Cannot join, Committee as a "whole" is, why does it need to be done on the 12th and not next year.
    - Lisa: The group was supposed to be having elections

## Meeting #37 - 2023-06-14

- **Duration:**
- **Chair: Joe Stringer**
- **Participants:**
  - **Dan Brown**
  - **Daniel Havey**
  - **KP Singh**
  - **Lisa Caywood**
  - **Alexei Starovoitov**
  - **Andrii Nakryiko**
  - **Dave Thaler**
  - **Daniel Borkmann**
- **Agenda**
  - [20m] [messaging document](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdocs.google.com%2Fdocument%2Fd%2F1ws6DxSA91XvHVFhPzsf1y3645OYY3PXr1_Zc4bfd3Ko%2Fedit%3Fusp%3Dsharing&data=05%7C01%7Cdthaler%40microsoft.com%7C6834fed78eba40e1eb3508db5d36cd97%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C638206262221231034%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000%7C%7C%7C&sdata=wFc5CqBwF1LQvUPbHt6D65RQ9rGwD%2BLTjG5asxaD%2F20%3D&reserved=0) from marketing committee [Lisa/Dan]
    - Point 1 - wording is a bit loose.
      - Follow up over email
    - Point 3 - Angle from hyperscalers is tricky to back up.
      - Is it about Performance or Production Proven?
      - The latter.
      - Discussed what "production" means - includes for example millions of Android devices
    - Goal: Provide feedback by Tuesday
  - [20m] Charter amendment proposals
    - BSC membership
      - [Proposal](https://github.com/joestringer/bsc/commit/04445829620a3dc8b11c7b87e057a9b79bd465f0)
        - Nominee eligibility - initially keep it open / undefined in charter?
        - Voter eligibility - Should be specified in Charter
    - Direction of funds
      - [Proposal](https://docs.google.com/document/d/1lT4k4fHHPOeuo1hdjKB-clfHsLfGn9BtTsojcsNysd0/edit)

  - [20m] Continue discussion of BSC charter and elections process [Lisa/Joe/Dave]
    - [Nominee list brainstorm](https://docs.google.com/document/d/1RqgTjoXAPB5zQxsuVxgCy0vzWjFd_nG1BZZSwm4OJyo/edit?usp=sharing)
      - Needs a public call for participation
    - [Voters process and project list](https://docs.google.com/document/d/1PZjefD4cRWcH0xy2GxtpxEXGIYqFUbWNtiKuGdthfnU/edit?usp=drivesdk)
      - We have a list (
      - Discussion on difference between ebepf.io / ebpf.foundation.
  - Project nominations
    - _Pending IP discussion, may be further bumped to a later session:_
    - BTFHub ([https://github.com/aquasecurity/btfhub](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fgithub.com%2Faquasecurity%2Fbtfhub&data=05%7C01%7Cdthaler%40microsoft.com%7C6834fed78eba40e1eb3508db5d36cd97%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C638206262221231034%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000%7C%7C%7C&sdata=KJE1Wz1Wvi%2B8%2BHXdCE9RqZGiS2JXcSpuIT2rku1FTHU%3D&reserved=0)) submission as Technical Project
    - Libbpfgo ([https://github.com/aquasecurity/libbpfgo](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fgithub.com%2Faquasecurity%2Flibbpfgo&data=05%7C01%7Cdthaler%40microsoft.com%7C6834fed78eba40e1eb3508db5d36cd97%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C638206262221231034%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000%7C%7C%7C&sdata=2Hr%2FOOwe79VHYJo0GyRPaocqm2TpOD4FYXt591Ehbt4%3D&reserved=0)) submission as Technical Project

## Meeting #36 - 2023-05-31

- **Duration:**
- **Chair: Dave Thaler**
- **Participants:**
  - **Alexei Starovoitov**
  - **Brendan Gregg**
  - **Joe Stringer**
  - **Andrii Nakryiko**
  - **KP Singh**
  - **Daniel Borkmann**
  - **Lisa Caywood**
- **AGENDA**
  - Report on May 9 board meeting feedback on BSC report, from [minutes](https://docs.google.com/document/d/1HTDYYYbfeu-BjalMX81CPNSp_1ysnOz56pf4LAbMDYA/edit):
    - Regarding creating a security whitepaper: "Thomas suggested that Isovalent could help. Thomas added that they have hired a good security researcher analyst who has actually written the security.md for cilium and he would be happy to check if they can volunteer that person to make a first proposal. Isovalent had actually come to this conclusion that this is needed over 2 years ago, and then it failed because they didn't have anybody to actually do a first version. He also said that he is confident that the community will contribute, but the real effort lies in writing this from scratch. Lastly Thomas offered to connect the resource person to the BSC members through the mailing list. Ram added that it is an expected behavior for high-volume systems to drop packets, and having a whitepaper would probably be fine but maybe talking broadly on this through Blog is another option that we could consider. Thomas agreed with this suggestion on writing Blogs."
      - AI [Daniel/Joe]: talk to Thomas about someone to hold pen on whitepaper
    - Regarding charter amendments: "2 charter amendments in a future meeting for the Board to actually vote on: one about BSC makeup and one on the direction of funds to projects in general. Though, the direction of funds to projects in general might not require a charter update just an update to the document (project progression policy)", and action to "facilitate a joint session among the Governing Board and BSC together to essentially work out something in a more timely fashion, just to avoid a 3 month process from this point. Both Dave and Lisa agreed to this suggestion by Thomas, and Dave said that BSC may need one or two meetings, which may take a month from now, before they could participate in such a joint meeting"
      - Proposal: BSC to put together straw-man proposal by June 14 meeting, and plan to schedule joint meeting shortly thereafter for initial discussion with GB.
    - Lisa drafted the one about BSC makeup
    - Need a volunteer for funding (meeting #33)
      - [Prior discussion](https://docs.google.com/document/d/1G33tM2HyDTDG-O04k1by8M3u2pv0j0GcIM9Yo-LFM7k/edit#bookmark=id.xim3jb4mhf39)
  - IP risks [Brendan]
    - Scott Nicholas (LF Legal) has a conflict during this time, but will reach out to Intel legal to discuss Windows [roadmap](https://docs.google.com/document/d/1IbYCopXI_pyhlAQAwMDjalF1cc9k2NOfFuMzvNJItLQ/edit#heading=h.4rb6lqa4huig) [KP Singh/Dave]
    - Brendan's story: don't have private meetings with startups without a legal agreement in place
    - Brendan's story: not all startups are friendly for the eBPF Foundation's mission
    - Brendan's story: the only thing that matters is what is signed
    - Question: is a notice at start of meeting sufficient or do we need evidence of agreement (click I Agree or whatever else)?  **AI: Brendan** to check with legal
      - Anti-trust slide we also have for GB meetings, is that sufficient?
      - [https://www.linuxfoundation.org/legal/antitrust-policy](https://www.linuxfoundation.org/legal/antitrust-policy)
    - Encourage wording when discussing technical solutions on BSC meetings:
      - _In your Open Source project_, how do you do X?
    - Option: Can we evaluate projects without meetings, and only call meetings if/when necessary?
  - IETF update
    - [https://datatracker.ietf.org/doc/charter-ietf-bpf/](https://datatracker.ietf.org/doc/charter-ietf-bpf/)
    - Charter sent out for IETF-wide review, comments due by June 10
    - On agenda of 2023-06-22 IESG telechat
- Moved to following meeting June 14th:
  - BTFHub ([https://github.com/aquasecurity/btfhub](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fgithub.com%2Faquasecurity%2Fbtfhub&data=05%7C01%7Cdthaler%40microsoft.com%7C6834fed78eba40e1eb3508db5d36cd97%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C638206262221231034%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000%7C%7C%7C&sdata=KJE1Wz1Wvi%2B8%2BHXdCE9RqZGiS2JXcSpuIT2rku1FTHU%3D&reserved=0)) submission as Technical Project
  - Libbpfgo ([https://github.com/aquasecurity/libbpfgo](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fgithub.com%2Faquasecurity%2Flibbpfgo&data=05%7C01%7Cdthaler%40microsoft.com%7C6834fed78eba40e1eb3508db5d36cd97%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C638206262221231034%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000%7C%7C%7C&sdata=2Hr%2FOOwe79VHYJo0GyRPaocqm2TpOD4FYXt591Ehbt4%3D&reserved=0)) submission as Technical Project
  - [messaging document](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdocs.google.com%2Fdocument%2Fd%2F1ws6DxSA91XvHVFhPzsf1y3645OYY3PXr1_Zc4bfd3Ko%2Fedit%3Fusp%3Dsharing&data=05%7C01%7Cdthaler%40microsoft.com%7C6834fed78eba40e1eb3508db5d36cd97%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C638206262221231034%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000%7C%7C%7C&sdata=wFc5CqBwF1LQvUPbHt6D65RQ9rGwD%2BLTjG5asxaD%2F20%3D&reserved=0) from marketing committee [Lisa/Dan]


## Meeting #35 - 2023-05-17

- **Duration:**
- **Chair: Daniel Borkmann**
- **Participants:**
  - **Daniel Borkmann**
  - **Dave Thaler**
  - **Dan Brown**
  - **Joe Stringer**
  - **Alexei Starovoitov**
  - **Brendan Gregg**
  - **Andrii Nakryiko**
  - **KP Singh**
- **AGENDA**
  - Quick status webinar functionality [Dan]
    - Rough ETA for webinar functionality next month
  - Charter and elections process [Lisa/Joe/Dave]
    - Options:
      - Current categories e.g. runtime, lib, etc as we have today
      - Lisa's proposal: Dropping categories and instead:
        - Active contributors to landscape projects
          - Nr commits/PR may not say much / can be gamed
          - Issues: large projects like LLVM may just have small BPF related group
        - Brendan's suggestion: people eligible "you have demonstrated that you furthered the eBPF ecosystem"
        - Questions:
          - Should there be seat categories or just a set of unspecified seats?
          - Voting eligibility based on landscape projects.
            - Alternative: Any active members
            - Alternative: Top N active members
            - Alternative: Should each landscape project get 1 vote (Linux gets 2)?
          - Practical steps:
            - BSC compile two lists of individuals in the eBPF community
              - Nominees (eg 20-50)
              - Voters (eg 200+)
            - Before sending vote out, check with nominees if they are interested in participating.
            - Each year, new BSC reviews these lists.
            - Voters get an email for something like Condorce to rank nominees. Voting system similar to LF TAB.
          - AI(Joe): Begin assembling lists
            - (?) Call for participation
            - Nominees - start a document shared with BSC to collect names
            - Voters - Joe to write a script to pull these from landscape projects
            - Joe to send the list of landscape projects to BSC list to confirm whether we are missing any eBPF community groups
            - No particular seat categories, half/half swap (2yrs, 1yr overlap).
            - Needs charter amendment
          - Deciding split this time
            - Top 4 nominees this time get 2 year terms, next four get 1 year terms.
          - AI(Joe): Prepare an alternate wording for the charter amendment that would capture the removal of the member categories without encoding the election process in the charter.
          - Alexei: We should have a dedicated mailinglist for any voters for the BSC.
            - These members are the core folks who care about eBPF, regardless of whether they are directly on BSC or not.
            - E.g. LSF/MM/BPF, LLVM, gcc, projects, etc.
            - Needs permission from folks we add there
            - Useful also for CFPs etc
            - Dave: Don't see the need for this to be "nominees" list. For voting or generally for active BPF contributors, we need a broader list for voters.
  - [IETF BPF WG charter](https://datatracker.ietf.org/doc/charter-ietf-bpf/): anything to discuss? [Dave]
    - Already got 1 Yes vote with minor editorial feedback: [[Bpf] Warren Kumari's Yes on charter-ietf-bpf-00-03: (with COMMENT)](https://mailarchive.ietf.org/arch/msg/bpf/8EiHJ4OSjjRsR8e0pzYGrCF-DVM/)
  - BPF Conformance project submission [Dave]
    - Goals seem beneficial
    - Would it remain on Alan's github user? He's indicated that he's open to moving it into a BPF foundation / BSC organization in GitHub.
    - BSC voted to accept it as a technical project
    - Next steps
      - AI(Dave): Reach out to Alan regarding legal procedures
      - Following that, requires board approval to finalize
  - Windows roadmap [KP Singh/Dave]

## Meeting #34 - 2023-05-03

- **Duration:**
- **Chair: Brendan Gregg**
- **Participants:**
  - **Joe Stringer**
  - **Dave Thaler**
  - **Dan Brown**
  - **Lisa Caywood**
  - **Alexei Starovoitov**
  - **Andrii Nakryiko**
  - **KP Singh**
  - **Daniel Borkmann**
- **AGENDA**
  - BSC meeting zoom panelist links
    - AI: Dan Brown will check what we are supposed to use and send out more detailed instructions for next time
  - bcc security vulnerability - Brendan
    - No details reported yet, so no embargoed info
    - Brendan did a blog post about known bcc observability tool issues: DoS and TOCTOU: [https://www.brendangregg.com/blog/2023-04-28/ebpf-security-issues.html](https://www.brendangregg.com/blog/2023-04-28/ebpf-security-issues.html) KP has done a POC [https://www.youtube.com/watch?v=l8jZ-8uLdVU](https://www.youtube.com/watch?v=l8jZ-8uLdVU)
    - [https://defcon.org/html/defcon-29/dc-29-speakers.html#guo](https://defcon.org/html/defcon-29/dc-29-speakers.html#guo)
    - Apparently not a known issue
    - Discussion: could be a kernel panic (e.g., tickling an existing kprobe issue)
    - Discussion regarding security expectations for some capabilities, e.g. syscall hooks / LSM hooks and TOCTOU. ELF input to libbpf/ btf.
    - Dave: Could we have a foundation doc to summarize "eBPF and security" we can point people to. Should cover:
      - eBPF is your friend in security
      - Observability tools are not security tools (and never have been), and currently need root access anyway
      - How to configure bpf to be secure (e.g., no interpreter, no unpriv access)
    - KP: eBPF security post should explore UID 0 vs CAPs. Also note that CVEs don't mean much for us when pretty much any kernel bug could be a CVE as well.
      - CPE score is higher if a system has unprivileged eBPF
      - AI: KP to start from Brendan's blog and expand it to a draft foundation doc?
    - Cilium security doc: [https://github.com/cilium/cilium/blob/main/SECURITY.md](https://github.com/cilium/cilium/blob/main/SECURITY.md)
    - Github (in Cilium we have this enabled): [https://docs.github.com/en/code-security/getting-started/adding-a-security-policy-to-your-repository](https://docs.github.com/en/code-security/getting-started/adding-a-security-policy-to-your-repository)
    - Brendan: bcc/bpftrace can add a "security.txt" to summarise security stance and recommendations to file security bugs, and if there is a bug bounty
    - Dave: once we have projects in the foundation, should we have security response policy guidelines similar to [governance/security-response-policies.md at main · confidential-computing/governance (github.com)](https://github.com/confidential-computing/governance/blob/main/security-response-policies.md)?
      - Dave to open a PR to discuss in a future BSC meeting
    - Action items:
      - BCC README update for security policy
      - Whitepaper for security guidance for eBPF (KP to draft for BSC review)
  - LSF/MM/BPF next week!
    - Joe: can raise awareness of BSC
  - BPF governing board
    - point (2): "Voting Process: Importantly on the nominees, and who are all the voters (electorate), avoiding overlap, preferably, between the two,  etc."
    - Lisa: what about letting, say, the top 50 contributors to recognized BPF related projects vote on the new BSC seats?

## Meeting #33 - 2023-04-19

- **Duration:**
- **Chair: Andrii Nakryiko**
- **Participants:**
  - **Alexei Starovoitov**
  - **Daniel Borkmann**
  - **Brendan Gregg**
  - **Joe Stringer**
  - **KP Singh**
  - **Dan Brown**
  - **Dave Thaler**
- **AGENDA:**
  - eBPF Foundation Governing Board kindly requests BSC to resolve the following in the upcoming BSC meeting(s):
    - Initial term duration: What should be the initial term for the 8 original members (now reduced to 7), and if it is same for all the categories.
      - Straw man (Dave): Set initial 2-year terms, resolve to nominate 1 year vs. 2 year terms for upcoming election. Do election before October.
    - Voting Process: Importantly on the nominees, and who are all the voters (electorate), avoiding overlap, preferably, between the two, etc.
      - Lisa: consider letting contributors to projects participate in a condorcet vote
      - Dave: [Condorcet Internet Voting Service (civs.us)](https://civs1.civs.us/)
    - Staggered Voting: If all the members be selected in one go or will it be staggered (preferred). If it is staggered, what will be the order?, tentative dates (if possible), etc.
      - Charter says staggered. We had previously discussed splitting each category to allow continuity within a category from one election to the next.
  - From Alexei:
    - Some iovisor folks expressed several concerns (in attached pdf)
    - regarding the structure of BSC.
    - Let's discuss them tomorrow during our meeting.
    - Nature of funding mechanisms
      - BSC desire to be able to direct funds towards development of features that will benefit the eBPF community, regardless of whether the target software is a member of the eBPF foundation
        - Applies to bpftrace etc (also IOVisor)
        - Applies to LLVM, GCC
        - Applies to Linux kernel (verifier improvements, docs)
        - Faster uprobes (no existing project)
        - Security audits
        - eBPF tutorials, training material
        - etc.
      - There should clearly be some base guidelines
        - OSS
        - eBPF as a core technology
        - Statement of Work
        - etc
      - We would need proposed wording + present to board and eventually vote etc. to change the charter.
        - AI(Alexei): Initial wording proposal regarding projects vs funding independent of foundation project or not
     - Lisa: Wrt contractors for certain technical work items, this may be possible by just directly proposing to the board:
        - Cost
        - Duration
        - Expected outcome/SOW
    - Voting membership
      - Technical projects are making this complicated. One idea: Eliminate them.
    - Opening the call to the public
      - Happy to make the meetings transparent for anyone to join in listen-only mode
      - Primary concern is just moderation - Avoid derailing BSC meeting
        - Related: Early BPF summit had targeted attacks, profanity, etc.
      - We can experiment with new Zoom options to test out settings to allow this.
        - Webinar - Host + Panelists + Viewers.
        - Panelists may be invited from prior discussion with BSC (just ask)
        - AI(Dan): Set up the zoom for next meeting


## Meeting #32 - 2023-04-05

- **Duration:**
- **Chair:**
  - **KP Singh**
- **Participants:**
  - **Daniel Borkmann**
  - **Joe Stringer**
  - **Kenny Paul**
  - **Dan Brown**
  - **Brendan Gregg**
  - **Alexei Starovoitov**
  - **Andrii Nakryiko**
- **AGENDA:**
  - eBPF foundation messaging from marketing committee [Dan]
    - Generalization from the kernel to privileged system context
    - Broader message around generality and beyond kernel
  - Iovisor meeting [Kenny]
    - I/O visor can move to BPF-F after sending a formal request
      - Upcoming sub-projects should be able to apply, some logistics need to be figured out.
      - [Joe] We need to make this low overhead and low friction.
      - eBPF or I/O visor is up-to the community of the project
      - Give users an objective criteria to select their foundation.
        - Kenny: Some pros and cons.
        - Projects get legal entities?
          - Clarify if there are legal implications of project joining one foundation or the other.
      - TL; DR roadblock for I/O visor joining eBPF-F has been removed.

  - Update from IETF116 [Dave/Alexei/Daniel]
    - OASIS:
      - Main seen as putting rubber stamp, but less strong as IETF, so vendors would prefer IETF RFC instead as it has wider industry reach
    - Licensing side-meeting:
      - Dual license of the doc seems okay, no road block from IETF side. IETF legal looking into it, but for now no specific issues come to their mind.
      - We might need to put the docs into subdir with ‘note well‘ doc so contributors are aware that their patch will in the end feed into current/future RFCs
      - IETF legal will get back to us within next 2-3 weeks
    - BOF went well, generally no objections from IETF community on forming a working group for the standardization effort
      - [Slides:](https://datatracker.ietf.org/meeting/116/session/bpf/)
      - [Summary notes:](https://mailarchive.ietf.org/arch/msg/bpf/JTUytbt_kEscF0oC_P8LvRREFo0/)
    - Charter side-meeting:
      - Applying feedback from BOF and discussion on deliverables from BPF wg in particular whether charter needs to be refined or scoped down in some areas (like cross-platform map/prog types)
      - [Latest:](https://github.com/ekline/bpf/blob/main/charter-ietf-bpf.txt)
    - ^^^AI(everyone): Please look at the IETF Charter document and share your thoughts.
  - BPF Technical roadmap details have been filled out for Linux, quick walk through and we should publish it
    - [Roadmap](https://docs.google.com/document/d/1IbYCopXI_pyhlAQAwMDjalF1cc9k2NOfFuMzvNJItLQ/edit#heading=h.4rb6lqa4huig)
    - Finalize details for windows too.

## Meeting #31 - 2023-03-22

- **Duration:**
- **Chair:**
  - **Alexei Starovoitov**
- **Participants:**
  - **David Vernet**
  - **Andrii Nakryiko**
  - **Brendan Gregg**
  - **Alexei Starovoitov**
  - **Daniel Borkmann**
  - **Lisa Caywood**
  - **Dave Havey**
  - **Dan Brown**
  - **Joe Stringer**
  - **Mykola Lysenko**
  - **Manu Bretelle**
- **AGENDA:**
  - Lisa: [core messaging doc](https://docs.google.com/document/d/1ws6DxSA91XvHVFhPzsf1y3645OYY3PXr1_Zc4bfd3Ko/edit#heading=h.ymrt225km0jh)
    - Looks good
    - Next steps is marketing group to iterate to make it more concrete
    - AI(KP): Update with security enhancements based on eBPF.
    - KP: Linux-specific - Kernel modules vs. eBPF implementations. Could be blog posts. Different user journey / developer workflows with benefits when taking an eBPF path.
    - How will it be used?
      - Internal guide for how to approach content creation
    - Misconceptions
      - Security
      - Complex programs
      - Gartner: eBPF – While it is realistic for technology vendors and hyperscalers, most enterprises lack the expertise and skills necessary to use eBPF. [Blog](https://blogs.gartner.com/andrew-lerner/2021/10/11/networking-hype-cycle-2021/)
  - IETF <> [OASIS](https://en.wikipedia.org/wiki/OASIS_\(organization\)) as standardization body, pro/con
    - [OASIS-OPEN](https://www.oasis-open.org/)
    - Well-established, published standards for XML, Virt-I/O
    - Process eventually goes through ISO for recognition
    - Relatively short timelines for steps in the process
    - Can we reach out to others that previously went through this process? Get their perspective?
      - [Virt-I/O](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=virtio)
      - [Michael Tsirkin](ms@redhat.com)
      - Questions:
        - How was the process for v1.0? What about v1.1?
        - What was the feedback process like with OASIS?
    - Community aspect - who will contribute to the standard
      - How would Technical Advisory Group (TAG) work in OASIS?
    - How do new iterations of documents work?
      - Full doc or extensions/errata/etc.
  - Discuss licensing of BPF doc vs IETF licensing requirements
    - Currently GPL+BSD, question wrt IETF process
    - GPL - makes internal kernel copy clearer
    - BSD-only seems fine, but we would need to discuss with the contributors to the files.
      - Some kernel uapi headers have used single permissive license already, so there is some precedence.
    - non-BSD license is a no-go.
  - [BPF Technical Roadmap](https://docs.google.com/presentation/d/1bsGgk_bxuhHxCxc_UXxEa62R-prAX0eNpwkT19_OeFY/edit#slide=id.g14930a8517c_0_0)
    - What's the best way to publish this technical roadmap?
    - Publish to ebpf.foundation
    - KP to work with Dan Brown on this.

## Meeting #30 - 2023-03-08

- **Duration:**
- **Chair:**
  - **Joe Stringer**
- **Participants:**
  - **Dave Thaler**
  - **KP Singh**
  - **Andrii Nakryiko**
  - **Brendan Gregg**
  - **Alexei Starovoitov**
  - **Daniel Borkmann**
  - **Lisa Caywood**
- **AGENDA:**
  - Review previous action items
    - [Participate – eBPF](https://ebpf.foundation/participate/)
    - FYI - [Labs now up](https://ebpf.io/get-started/)
      - We could create more
      - We can use these for IETF hackathon
      - Question(Dave): Does Isovalent want to contribute these to the foundation?
      - FYI also for marketing committee.
      - AI(Daniel): Talk to Liz Rice about this.
  - Update from Lisa - new marketing person from LF
    - Figuring out marketing strategy etc.
  - IETF update
    - Dave: [IETF 116 Meeting Agenda](https://datatracker.ietf.org/meeting/116/agenda/)
    - 5 interesting items:
      - Hackathon (sat/sun)
      - Welcome (sun)
      - BPF session (mon)
      - Hackdemo Happy Hour	
      - Side meeting yet to be scheduled
    - Deadline for drafts 5pm PT next Monday
      - AI(Dave): Snapshots for instruction set + ELF proposals
      - AI(Everyone): Register for remote participation
        - Link: [IETF Registration](https://registration.ietf.org/116/)
  - IOVisor subprojects: Invite drafted to IOVisor board
    - [Document](https://docs.google.com/document/d/1gU3ATGrUX3w7J1FoaKClZ2IXskqe3xx1fOhj73_UK1g/edit)
    - Next step: Invite Yunsong + Fulvio onto an upcoming BSC session
      - Likely 5 April
      - Sridhar+Kenny should also be invited for LF context
      - AI(Dave): Extend an invite
  - Landscape projects, List thread from Reza Ramezanpour
    - [Related PR:](https://github.com/ebpf-io/ebpf.io-website/pull/349)
    - Last notes do not have a conclusion
    - Example (KP): Project migrating to BPF. When can it be added as emerging project?
    - Dave: Falco, Calico, even Linux fails this point:
      - The project must be using eBPF as its underlying core technology, in other words, a project would lose its purpose if the eBPF parts are removed.
    - Proposal:
      - "It must encourage the deployment/use of" BPF.
      - CCC language example: “accelerate the adoption of”
      - Two steps:
      - Action on Calico ebpf.io PR - AI(Daniel): [Update: Add project Calico to the projects page by frozenprocess · Pull Request #349 · ebpf-io/ebpf.io-website (github.com)](https://github.com/ebpf-io/ebpf.io-website/pull/349)
      - Language update to landscape requirements, on both ebpf.io and ebpf.foundation - AI(KP)
        - Ebpf.foundation doc to update: [bsc/project-progression-policy.md at master · ebpffoundation/bsc (github.com)](https://github.com/ebpffoundation/bsc/blob/master/project-progression-policy.md#iii-requirements-for-technical-projects)
        - Ebpf.io doc to update: [ebpf.io-website/faq.jsx at master · ebpf-io/ebpf.io-website (github.com)](https://github.com/ebpf-io/ebpf.io-website/blob/master/src/components/pages/project-landscape/faq/faq.jsx)
      - Guard against “eBPF washing”: Default install on common platforms deploys with BPF programs?
      - Brendan: Title at the top: "The following projects use BPF at the core of the project"
        - Potentially curated list from BSC at the eBPF foundation page
      - Brendan: ‘eBPF recommended project’
      - Lisa: Avoid product / company links. Stick to OSS projects.
      - Dave: foundation currently gives visibility to non-foundation landscape projects, at [Projects – eBPF](https://ebpf.foundation/projects/) but it’s out of date compared to ebpf.io. Merging the calico PR on ebpf.io will not add Calico to the ebpf.foundation page, notably. Need a separate PR or process to “recognize” it from the foundation.
      - Foundation page should also list ongoing engagements/projects that have BSC involvement
        - BPF standardization @ IETF
        - Technical Roadmap
        - Organization of BPF technical confs
        - …
      - Lisa: Role of the foundation here, messaging.
        - AI(Lisa): Share the brainstorm doc with the BSC list

## Meeting #29 - 2023-02-08

- **Duration:**
  - **1h**
- **Chair:**
  - **Dave Thaler**
- **Participants:**
  - **Dave Thaler**
  - **KP Singh**
  - **Andrii Nakryiko**
  - **Brendan Gregg**
  - **Lorenz Bauer**
  - **Alexei**
  - **Daniel**
- **AGENDA**
  - [Lorenz] Employed at Isovalent now
    - This means there are three BSC members, which is against our charter
    - Will come back to this if Joe joins, regarding charter/BSC election status
  - IO Visor discussion
    - Previous AI Joe: reach out Fulvio, plus invitation of both of them to BSC meeting
    - Email from Sridhar re Yunsong Lu
  - IETF prep, report on previous AIs
    - Previous AI Dave: request side-meeting
    - Previous AI Daniel: announcing to bpf@vger to Cc ietf list for doc changes related to standardization
    - Previous AI Dave: till March 13th posting snapshot of internet draft of BPF RFC
    - Status of BOF request
  - [Dave, Daniel] Landscape projects
    - How do we deal with "projects" that have an eBPF component or mode but also have non-eBPF components/modes?
    - Is the answer the same or different for ebpf.io vs ebpf.foundation (incl. BSC eligibility)?
    - Various different cases:
      - Calico
      - Falco
      - clang/LLVM
      - gcc
      - Linux
      - …
  - Continue [BPF Technical Roadmap - Google Slides](https://docs.google.com/presentation/d/1bsGgk_bxuhHxCxc_UXxEa62R-prAX0eNpwkT19_OeFY/edit#slide=id.g14930a8517c_0_0)
    - [Dave] Windows BPF roadmap discussion
  - KP: psABI = "processor specific" ABI https://refspecs.linuxfoundation.org/elf/IA64-SysV-psABI.pdf
  - Publishing BSC minutes on [bsc/minutes.md at master · ebpffoundation/bsc (github.com)
](https://github.com/ebpffoundation/bsc/blob/master/minutes.md)[IETF 116 Hackathon | IETF Community Wiki](https://wiki.ietf.org/en/meeting/116/hackathon)

## Meeting #28 - 2023-01-25

- **Duration:**
  - **1h**
- **Chair:**
  - **Daniel Borkmann**
- **Participants:**
  - **Brendan Gregg**
  - **Andrii Nakryiko**
  - **Dave Thaler**
  - **Alexei Starovoitov**
  - **Joe Stringer**
  - **Lisa Caywood**
- **AGENDA**
  - [Joe] Update on LF / iovisor \<\> eBPF foundation
    - Sridhar reached out to Yunsong to check how eBPF foundation + iovisor would work.
    - Yunsong's PoV:
      - Non-overlapping scope where eBPF foundation could subsume iovisor
      - iovisor could join eBPF foundation
      - iovisor scope:
        - Virtualized in-kernel I/O, doesn't strictly say it has to be eBPF
      - Yunsong likely at IETF
    - No reach out yet to Fulvio, discussion continues
    - **AI Joe:** reach out Fulvio, plus invitation of both of them to BSC meeting
  - [Brendan] Strategy with regards to startups trying to own an important piece of eBPF ecosystem behind closed doors and/or as patented technology
    - Defensive publication for prior art
    - Example:
      - Placing ideas into technical roadmap of BSC
      - Blog posts on ideas
    - Should we file defensive patents as a foundation?
      - Price  tag ~100k per patent
      - Foundation potentially could do that if we see fit
    - Encouraging to upstream core infra pieces into kernel, cannot live OOT
      - Example: fast uprobes
  - [Dave] update on prep for IETF and Internet-Draft submission
    - [Re: [Bpf] [Tools-discuss] reStructuredText (rst) to xml2rfc? (ietf.org)](https://mailarchive.ietf.org/arch/msg/bpf/f9L2rdNYGc-ekJL1dxA9owogFlg/)
      - Example/draft output from tool:  [https://htmlpreview.github.io/?https://raw.githubusercontent.com/ebpffoundation/ebpf-docs/pdf/draft-thaler-bpf-isa.html](https://htmlpreview.github.io/?https://raw.githubusercontent.com/ebpffoundation/ebpf-docs/pdf/draft-thaler-bpf-isa.html)
        - Auto-updated from master branch via GH action
    - BPF BOF likely to get approved, list of proposals:
      - [https://datatracker.ietf.org/meeting/important-dates/](https://datatracker.ietf.org/meeting/important-dates/)
      - BOF request expand to 3h or another side-meeting
      - Side-meeting not going into proceedings, side-meeting before the BOF scheduled
      - **AI Dave:** request side-meeting
      - [https://datatracker.ietf.org/doc/bofreq-thaler-bpf-ebpf/](https://datatracker.ietf.org/doc/bofreq-thaler-bpf-ebpf/)
      - **AI Daniel:** announcing to bpf@vger to Cc ietf list for doc changes related to standardization
      - **AI Dave:** till March 13th posting snapshot of internet draft of BPF RFC
      - BPF ELF format wip draft: [ebpf-docs-1/rst at elf · dthaler/ebpf-docs-1 (github.com)](https://github.com/dthaler/ebpf-docs-1/tree/elf/rst)
  - [AI: all] Continue to extend [BPF Technical Roadmap - Google Slides](https://docs.google.com/presentation/d/1bsGgk_bxuhHxCxc_UXxEa62R-prAX0eNpwkT19_OeFY/edit#slide=id.g14930a8517c_0_0)
    - [Dave] Windows BPF roadmap discussion
    - To be continued next meeting

## Meeting #27 - 2023-01-11

- **Duration:**
  - **1h**
- **Chair:**
  - **Brendan Gregg**
- **Participants:**
  - **Brendan Gregg**
  - **Andrii Nakryiko**
  - **Dave Thaler**
  - **Alexei Starovoitov**
  - **Daniel Borkmann**
  - **Joe Stringer**
  - **KP Singh**
- **AGENDA**
  - [IETF 116](https://www.ietf.org/how/meetings/116/) ([https://datatracker.ietf.org/doc/bofreq-thaler-bpf-ebpf/](https://datatracker.ietf.org/doc/bofreq-thaler-bpf-ebpf/))
    - Yokohama Japan, March 25-31. Should be cherry blossom season: take your camera!
    - With regards to travel, do we know which day the BOF might take place?
      - [Dave] Per [IETF 116: Important Dates](https://datatracker.ietf.org/meeting/116/important-dates/), the IESG decision whether to grant a BOF will be by Feb 17th.  A draft agenda answering the "which day" question will be available by Feb 24th, and the agenda will be final by March 3.
    - Process for Visa invitations: [IETF | Visa Application Process](https://www.ietf.org/how/meetings/116/116-visa-application-process/)
    - Any other plans @ IETF outside BOF?
      - [Dave] Likely will be used in various [hackathon](https://wiki.ietf.org/en/meeting/116/hackathon) projects
  - Misc bits [Daniel]:
    - LSF/MM/BPF CFP is out ([https://lore.kernel.org/bpf/Y7hDVliKq+PzY1yY@localhost.localdomain/](https://lore.kernel.org/bpf/Y7hDVliKq+PzY1yY@localhost.localdomain/))
      - Vancouver, May 8-10
    - FOSDEM kernel devroom schedule ([https://fosdem.org/2023/schedule/track/kernel/](https://fosdem.org/2023/schedule/track/kernel/))
      - Brussels Feb 4,5
    - [BPF Conference spreadsheet](https://docs.google.com/spreadsheets/d/1aLBiGI2-xRQ6AtWwiFK59brjt52oQVeRt5cgqf14Yx4/edit#gid=1036541245&fvid=143074800)
    - Adding events to the foundation website for upcoming conferences
      - Cloud native security con [bpf talks](https://events.linuxfoundation.org/cloudnativesecuritycon-north-america/program/schedule/) (search bpf)
      - AI(Daniel): Bill should reach out to Sridhar to arrange
  - SREcon, Singapore [Brendan]
    - KP may know people; Alexei
  - BPF naming: BPF as a superset
    - [https://ebpf.io/what-is-ebpf#what-do-ebpf-and-bpf-stand-for](https://ebpf.io/what-is-ebpf#what-do-ebpf-and-bpf-stand-for)
  - BPF on systemd; can systemd manage lifecycle of BPF everything? [Alexei]
    - What about people using k8 to manage everything? [Joe]
    - Currently L3AFd does try to do this for BPF [Dave]; L3AFd is cross-platform
      - Walmart is using it now.
      - Discussion on how L3AFd works - API-based configuration, etc. Give it a URL + commands to execute the user+bpf kernel progs
  - Intel joining eBPF foundation: waiting on LF
  - Fedora frame pointers approved and planned for a release
    - Brendan to do blog post on stack walking and BPF
    - (lookup sframe stuff)
    - [https://fosdem.org/2023/schedule/event/walking\_stack\_without\_frame\_pointers/](https://fosdem.org/2023/schedule/event/walking_stack_without_frame_pointers/)
  - Continue [BPF Technical Roadmap - Google Slides](https://docs.google.com/presentation/d/1bsGgk_bxuhHxCxc_UXxEa62R-prAX0eNpwkT19_OeFY/edit#slide=id.g14930a8517c_0_0): Windows portion [Dave]

## Meeting #26 - 2022-12-14

- **Duration:**
  - **1h**
- **Chair:**
  - **Andrii Nakryiko**
- **Participants:**
  - **Andrii Nakryiko**
  - **Brendan Gregg**
  - **Daniel Borkmann**
  - **Dave Thaler**
  - **Joe Stringer**
  - **Lorenz Bauer**
  - **KP Singh**
- **AGENDA**
  - IOVisor follow ups
    - Joe will ping Kenny, no updates otherwise
    - We need IOVisor projects to better align with BSC charter
  - Faster uprobes (Brendan)
    - The goal is to avoid mode switch overhead caused by normal uprobes (uprobes are many times slower than kprobes to trigger)
      - Andrii: a good chunk of overhead is when there is no NOP that the uprobe code can patch out. If NOP is present ~3x faster.
    - There are new "zero instrumentation APM" companies in the market
      - Based on uprobes, slows down application
      - Slower than Open Telemetry
      - Dave: Should we invite OTel people to BSC meetings?
      - Brendan: OTel already puts hooks into code, could use those for USDT
        - [https://sched.co/1Auyh](https://sched.co/1Auyh)
        - [https://www.youtube.com/watch?v=0D4GTdv7QQA](https://www.youtube.com/watch?v=0D4GTdv7QQA)
      - A lot of the industry outside of SF doesn't have the ability to change source, so uprobe based instrumentation is the only things that works
      - Brendan: imagine a "OTel using eBPF project", possible to do and would get a lot of attention
    - This needs user-space BPF engine, and somehow figure out user-kernel BPF interactions
    - KP: teach kernel to JIT BPF program into privileged user-space memory page within process' memory space. Fall back to syscall-like interface if BPF program needs to interact with kernel state (BPF maps, BPF helpers, etc)
    - Is this a possible outreachy / intern project?
      - See [Outreachy | Mentor FOSS interns - Outreachy](https://www.outreachy.org/mentor/) and [Mentor FAQ - Outreachy](https://www.outreachy.org/mentor/mentor-faq/) for mentorship requirements
      - Might have to extend BPF foundation policy to allow this
  - Andrii: Fedora has rejected enabling frame pointers, but might get a second shot at this
    - [https://pagure.io/fesco/issue/2817](https://pagure.io/fesco/issue/2817)
    - [https://pagure.io/fesco/issue/2917#comment-832331](https://pagure.io/fesco/issue/2917#comment-832331)
    - Andrii: Maybe we should push Canonical for this as well?
      - KP: Kees might help
  - [Dave] BPF vs eBPF terminology
    - Lots of discussion, but leaning towards using eBPF in eBPF foundation-derived documentation, but mention that BPF is perfectly valid name as well
    - BPF is often used as a category / broad term, but this means something different to BSD people
  - [Dave] community topics for meetings (my action item) and Foundation info on the BSC
    - [https://ebpf.foundation/participate/](https://ebpf.foundation/participate/) - moved to next meeting
  - [Dave] BPF technical roadmap (Windows portion) - moved to next meeting
  - Next meeting date?
    - 2023-01-11

## Meeting #25 - 2022-11-16

- **Duration:**
  - **1h**
- **Chair:**
  - **Joe Stringer**
- **Participants:**
  - **Joe Stringer**
  - **Alexei Starovoitov**
  - **Dave Thaler**
  - **Daniel Borkmann**
  - **KP Singh**
  - **Lisa Caywood**
  - **Mykola Lysenko**
  - **Brendan Gregg**
  - [**Andrii Nakryiko**](mailto:andrii.nakryiko@gmail.com)
- **AGENDA:**
  - IOVisor project invitations
    - [Joining the eBPF Foundation - IOVisor budget steering committee](https://docs.google.com/document/d/1CgVATbTGbvnPebZ9YD39qVjaVGN9UixGMKZIq-Ltw0A/edit?usp=sharing)
    - [Joining the eBPF Foundation - Projects](https://docs.google.com/document/d/1Xhfrdlqi0xKcGN5Oz_1ReiKoGnlCh6IdvbK9tPhLFy0/edit?usp=sharing)
    - Next steps:
      - Get OK from BSC on templates
      - For the IOVisor budget steering board, reach out to Kenny Paul to initiate the reach-out
      - BCC, BPFTrace, Kubectl trace and Ply, uBPF:
        - At this point, the effort to include these projects individually in the eBPF foundation does not outweigh the process.
        - It seems like a more promising path to just follow up directly with the IOVisor budget steering board and follow up on alignment/merging on bulk for all projects.
    - AI (Joe): Follow up with Kenny for the first template. Hold back on reaching out to individual projects, pending progress directly with the IOVisor budget steering board.
  - IETF discussion
    - KP, Alexei, Dave attended the side-meeting at IETF last week
    - Dave summary:
      - Well attended, a recording was made and there are two sets of notes. Dave to follow up on sharing these with BSC.
      - No interest in non-IETF RFC
      - ISO not discounted
      - Several interested in standardizing in IETF
      - IETF hackathon separately also had various eBPF hack projects
        - [IETF-Hackathon/ietf115-project-presentations: Project results presentations at end of Hackathon (github.com)](https://github.com/IETF-Hackathon/ietf115-project-presentations/) has all the presentations, DT tto figure out which ones had eBPF in them
        - Here's one: [ietf115-project-presentations/hackathon-presentation-pdmeh.pdf at main · IETF-Hackathon/ietf115-project-presentations (github.com)](https://github.com/IETF-Hackathon/ietf115-project-presentations/blob/main/hackathon-presentation-pdmeh.pdf)
        - Here's another: [https://github.com/IETF-Hackathon/ietf115-project-presentations/blob/main/IETF%20115%20Hackathon-BMWG-Container%20Benchmarking.pdf](https://github.com/IETF-Hackathon/ietf115-project-presentations/blob/main/IETF%20115%20Hackathon-BMWG-Container%20Benchmarking.pdf)
        - SRv6 hackathon presentation does NOT mention eBPF so don't know whether they used eBPF or not: [ietf115-project-presentations/ietf-115-hackathon-srv6-dataplane-visibility.pdf at main · IETF-Hackathon/ietf115-project-presentations (github.com)](https://github.com/IETF-Hackathon/ietf115-project-presentations/blob/main/ietf-115-hackathon-srv6-dataplane-visibility.pdf)
      - From hallway immediately afterwards, suggestion / request to create a bpf@ietf.org email address which also forwards to [bpf@vger.kernel.org](mailto:bpf@vger.kernel.org) list
      - Range of proposals, ISA is the most concrete. Not enough time to discuss standardization of other aspects (map types etc.)
    - Q: How hardware industry intends to use eBPF.
      - KP: With NVME there are papers with concrete proposals
      - Potential benefit of ISA standardization outside kernel to expand usage, in domains where we may not have previously considered
    - Alexei: Suggestion - Begin following the IETF procedure but using rST
      - Dave: By the time something becomes an RFC, it is typically defined in XML. That would likely be the target format preferred by IETF. We could use a rst2xml converter to get it in the right format.
    - Mykola: How would we version RFCs over time (particularly after published)? Consider that the ISA may be further expanded.
      - Dave: Couple of options. Brand new RFC, or new extension RFCs. In the initial RFC, specify that the set of opcodes may be expanded in future RFCs. If there are no breaking changes, just create a new "delta" document for the new bits.
      - Can also opt to reserve some portion of the opcodes to avoid standardization for those ranges. Those reserved set are commonly also managed by IANA for allocation in other RFCs.
      - Errata is also possible for minor amendments.
    - Alexei: We still have the option to choose, but given the range of use cases brought up in the IETF session it seems like it is worth seriously considering
      - Routers, edge, wifi, SRv6, NVME
    - Dave:
      - Possible next steps: New mailing list @ IETF
      - Arrange a BoF at the next IETF (March, Yokohama JP)
        - [IETF | IETF 116](https://www.ietf.org/how/meetings/116/)
      - Based on activity on the ML, we could get a slot for a BoF and/or WG. BoF is typically a first step.
      - AI (Dave): Reach out to IETF folks to set up ML
      - AI (Dave): get on the proposed BOF list for IETF 116
        - [BOF Requests (ietf.org)](https://datatracker.ietf.org/doc/bof-requests)
  - KP:
    - [https://www.usenix.org/conference/osdi22/presentation/zhong](https://www.usenix.org/conference/osdi22/presentation/zhong)
    - Alexei: Not NVMe related, but like XDP for storage
      - Acceleration of B-Tree walks etc.
    - Christoph's use case:
      - Programmable RAID / load balancing
  - KP:
    - [BPF Technical Roadmap](https://docs.google.com/document/d/1IbYCopXI_pyhlAQAwMDjalF1cc9k2NOfFuMzvNJItLQ/edit#heading=h.s9q5yjnxn0e5)
      - Can everyone check they have access to this?

## Meeting #24 - 2022-11-02

- **Duration:**
  - **1h**
- **Chair:**
  - **Alexei Starovoitov**
- **Participants:**
  - **Andrii Nakriyko**
  - **Daniel Borkmann**
  - **Joe Stringer**
  - **Lisa Caywood**
- **AGENDA:**
  - **Conference sheet from Lisa:**
    - [https://docs.google.com/spreadsheets/d/1aLBiGI2-xRQ6AtWwiFK59brjt52oQVeRt5cgqf14Yx4/edit#gid=0](https://docs.google.com/spreadsheets/d/1aLBiGI2-xRQ6AtWwiFK59brjt52oQVeRt5cgqf14Yx4/edit#gid=0)
    - Rough estimate around sponsorship opportunities
    - Waiting on list from Brendan to further complete conferences
  - [https://lists.ebpf.foundation/g/bsc/topics](https://lists.ebpf.foundation/g/bsc/topics)

## Meeting #23 - 2022-10-19

- **Duration:**
  - **1h**
- **Chair:**
  - **Lorenz Bauer**
- **Participants:**
  - **Alexei Starovoitov**
  - **Andrii Nakriyiko**
  - **Dave Thaler**
  - **Daniel Borkmann**
  - **Joe Stringer**
  - **Brendan Gregg**
  - **Lisa Caywood**
  - **KP Singh**
- **AGENDA:**
  - Review Action Items
    - Alexei discussion with Christoph Hellwig
      - Hardware vendors (?) would like standardization
      - Amazon, Intel proposal not viable
      - No IETF is not a deal breaker, but preference from Christoph
    - eBPF/IETF discussion call scheduled for [8am Pacific 10/21](https://www.worldtimebuddy.com/?qm=1&lid=8,2643743,2643743&h=8&date=2022-10-21&sln=8-9&hf=0)†
      - Alexei and Dave will attend
  - [Joe, Dave] Report on discussion with Kenny Paul about iovisor foundation
    - [Joining the eBPF Foundation - Google Docs](https://docs.google.com/document/d/1CgVATbTGbvnPebZ9YD39qVjaVGN9UixGMKZIq-Ltw0A/edit)
    - Dave: merge iovisor with eBPF foundation might take longer, offer individual projects to migrate
      - Iovisor has money they can't spend
      - Lisa: bureaucratic process, doable but requires timely action
        - Not much interaction between iovisor technical board and LF
      - Joe: has a list of the current technical board members of iovisor.
        - Alexei Starovoitov (Meta)
        - Fulvio Risso (Politecnico di Torino)
        - Yunsong Lu (Huawei)
        - cf. Fri, Oct 7 mail to BSC from Joe with notes from discussion with LF
    - Migrating a project that is already under LF just requires an application to eBPF foundation
    - Lisa: how would we migrate projects? How many can we migrate?
      - Transfer of ownership insider LF
      - We might have to budget funds for this, maybe we can use iovisor funds?
  - [Lorenz] What's happening to the eBPF trademark?
    - Application is happening
  - [Dave] Use of eBPF logo for landscape projects
    - Bill Mulligan [asks](https://github.com/ebpf-io/ebpf.io-website/pull/278#issuecomment-1269518791): "Since there is currently no logo, would you mind adding just the eBPF one for now?"
  - [Dave] ebpf-docs repo created under github ebpffoundation org.  Booked Oct. 27 office hours slot.
  - [Daniel] Applied for FOSDEM'23 for eBPF [devroom](https://submission.fosdem.org/submission/devroom) track (Quentin, Florent, Michal, Daniel)
    - Single day, should know whether it's accepted by end of October
    - Maybe use foundation resources to publicize the CFP?
    - Lisa: started a list of foundation relevant events
      - Funnel this back into website / social media
    - Brendan: has a long list, going to filter that down

## Meeting #22 - 2022-10-05

- **Duration:**
  - **1h**
- **Chair:**
  - **KP Singh**
- **Participants:**
  - **Alexei Starovoitov**
  - **Brendan Gregg**
  - **Daniel Borkmann**
  - **Dave Thaler**
  - [**Joe Stringer**](mailto:joe@isovalent.com)
  - **Andrii Nakryiko**
- **AGENDA:**
  - Standardization
    - Can we standardize eBPF in [IETF](https://www.ietf.org/)?
      - Lars, chair of IETF, was open to it.
      - Lars is creating a conference call to discuss?
    - Would eBPF people participate in IETF?
    - Is it in scope for IETF?
    - KP: What are the benefits of standardization in IETF? [Not a lawyer disclaimers from all folks]:
      - Not very clear yet.
      - Dave in IETF for a long time.
      - Alexei: Had attended one IETF meeting
        - A lot of discussion about copyright, licensing, trademarks etc.
        - BPF ISA is not copy-righteable
      - IETF does not require IP assignment
        - But it requires disclosure
      - By submitting one, grants permission to IETF to create derivative works.
        - IETF can, legally, change the standard without eBPF foundation consensus.
        - Google created some RFC, IETF created a derivative.
      - Ratification to ISO for standardization
    - Alexei: Linux foundation has some way to make sub foundations to make standards
      - LF won't help us
      - Check with Christoph, if an RFC number is sufficient, this is lighter than becoming an official IETF standard / document.
    - Daniel: What does it mean to have a RFC number?
    - Brendan: What about POSIX?
      - Dave has been involved with POSIX
      - POSIX is published by 3 ISO, IEEE, the Open Group.
        - 3 need to ratify a standard
        - Likely a time intensive process.
        - See [Austin Group - Wikipedia](https://en.wikipedia.org/wiki/Austin_Group) for more details on how the 3 orgs together make up the "Austin Group" for POSIX
        - In ISO, the C group is dormant and got merged into the C++ group at present, where Dave lurks on the mailing list
        - Mailing list is not just open to any subscriber, you have to get an invite
    - Alexei: Where is C++ standard happening?
      - ISO
      - List is locked
    - Alexei: Where is Rust doing its standard work?
      - Andrii: There does not appear to be a standard
    - Andrii:
      - Java standards: [https://docs.oracle.com/javase/specs/](https://docs.oracle.com/javase/specs/) Oracle publishes them itself
    - NVME: [NVM Express – scalable, efficient, and industry standard](https://nvmexpress.org/), specs are free/public apparently
    - Alexei: A ratification helps hardware vendors have more comfort implementing w.r.t stability, legal etc.
      - Lisa: We do have access to LF legal for a consultation and they can guide us.
    - Check with Christoph about the requirements of the nvme standard to take [] reference for eBPF (eBPF doc, independent-steam RFC, IETF RFC, ISO), take least effort to unblock Christoph.
      - Alexei to check with Christoph in person next week.
  - Dave: Feedback on recruit project contributions process
    - uBPF maintainers under iovisor to submit their project
    - uBPF is writing a compliance test suite based on the ISA doc, possibly, in a way to make it generically pluggable.
      - PR in the uBPF repo.
    - This is from Quentin: [https://github.com/ebpffoundation/ebpf-docs/tree/main/tools/ebpf-check](https://github.com/ebpffoundation/ebpf-docs/tree/main/tools/ebpf-check), compliance check for an ELF file.
    - Consensus: Encourage to contribute to foundation
  - Dave (with help from others) is doing a lot of standard cleanup work.
    - Alexei: needs reviews from other people.
  - Donald proposed help with documents:
    - Propose inviting Donald to BSC meeting, OH is a possibility, not works for all BSC folks though.
  - Daniel: BPF track at FOSDEM conference
    - [FOSDEM 2023 - Home](https://fosdem.org/2023/)
    - KP: Possibly also a keynote speaker
    - Who is the eBPF community manager?
      - Lisa: Marketing committee. Bill is mostly managing it
      - Consensus: List of conferences we should be engaged with
      - Probably a Wiki, your favorite spreadsheet platform
  - More conferences:
    - Scale20x
    - SRE Con
    - FOSS.in (India)
    - [Schedule | Linux Foundation Events](https://events.linuxfoundation.org/open-source-summit-europe/program/schedule/) is scheduled for Open Source SUmmit Europe (co-located with LPC) and had ebpf talks, just search for ebpf on that page

## Meeting #21 - 2022-09-21

- **Duration:**
  - **1h**
- **Chair:**
  - **Joe Stringer**
- **Participants:**
  - **Alexei Starovoitov**
  - **Brendan Gregg**
  - **Daniel Borkmann**
  - **Dave Thaler**
  - **KP Singh**
  - **Andrii Nakryiko**
- **AGENDA:**
  - (10m) Documenting prog types and map types
    - [Issue on ebpf.io issues](https://github.com/ebpf-io/ebpf.io-website/issues/259)
    - Email from BSC list, [ebpf.io issue](https://github.com/ebpf-io/ebpf.io-website/issues/259)
    - Let's direct people to submit patches to the upstream kernel tree to improve this documentation
    - Long-term, cross-platform docs on ebpf.foundation. Dave Thaler is already beginning work in this direction.
  - (40m) Roadmap
    - [BPF Technical Roadmap - Google Slides](https://docs.google.com/presentation/d/1bsGgk_bxuhHxCxc_UXxEa62R-prAX0eNpwkT19_OeFY/edit#slide=id.g13ceb4fbe3c_0_0)
    - Verification
      - Extension: Observing verifier decisions. Relevant to signing
    - CI
      - Discussion around arm64 cross-arch testing. Progress being made.
      - BSC should engage with s390, ppc64, risc-v, mips maintainers to get missing features like trampolines, atomics etc.
    - More notes added as comments on the roadmap slides
    - Continue the rest of the roadmap discussion next meeting
  - (10m) Election
    - Were any candidates identified during LPC discussion?
      - None in particular
    - Key question: Do we have the BSC makeup that we want?
      - Other OSes (BSD, Apple, Amazon)
      - AI(Dave): Reach out to Apple folks
    - Proposal: Delay election until IOVisor -\> BPF Foundation transition occurs
      - Who owns next steps here?
      - AI(Joe): Reach out to Sridhar on template for eligible projects to ask whether they would be interested to join BPF Foundation.
  - IETF BPF Standardization
    - May be difficult based on scope of BPF (not a protocol)

## Meeting #20 - 2022-09-07

- **Duration:**
  - **1h**
- **Chair:**
  - **Dave Thaler**
- **Participants:**
  - **Alexei Starovoitov**
  - **Andrii Nakryiko**
  - **Joe Stringer**
  - **Brendan Gregg**
  - **Daniel Borkmann**
  - **Lorenz Bauer**
- **AGENDA:**
  - KP: Roadmap [slides](https://docs.google.com/presentation/d/1bsGgk_bxuhHxCxc_UXxEa62R-prAX0eNpwkT19_OeFY/edit#slide=id.g14930a8517c_0_9) some slides have been added). Folks please add slides
    - KP might not be able to make it to this instance
  - Lisa Caywood walked us through her email about ebpf.foundation/projects and the BSC discussed her questions
    - Keep landscape projects off foundation projects page
    - Could link from BSC membership page to projects that are represented, e.g., anchor at ebpf.io/projects
    - Daniel suggested we include efforts like BPF standardization
    - Also add documentation
      - Best practices for distributions
      - ?
    - ACTION (?): create a list with relevant links (+blurb?)
      - Below could be under menu item "Initiatives" or "Featured Work" and highlight ongoing efforts, e.g. similar design as project 'boxes'
        - Brendan: BPF guidelines
        - Dave: standardization
        - KP: BPF roadmap
        - Daniel: ecosystem report
        - Daniel: community events
          - Events we co-org, sponsor and plan to increase user base
          - (but isn't that marketing committee, on a different page?)
  - Minutes
    - 1 week to revise private notes in this document
    - 1 week after meeting, GB chair publishes to [https://github.com/ebpffoundation/bsc](https://github.com/ebpffoundation/bsc)
      - GB chair or BSC chair?
      - Should be LF PM?
  - Public meeting references
    - Typically the Weds biweekly meetings are open to BSC and invitees only (subject to charter)
    - Typically the thurs BPF office hours is completely open with topics proposed ahead of time on a first come, first serve basis. BSC members attend this regularly. Canceled if there is no agenda. We should advertise this more widely.
    - BSC ML: bsc@lists.ebpf.foundation
  - Joe reported on projects and BSC membership in preparation for nominations
    - Two-week period to poll for candidates
    - Goal for candidate pool next BSC meeting, using LPC to recruit/scout out possible candidates

## Meeting #19 - 2022-08-24

- **Duration:**
  - **1h**
- **Chair:**
  - **Daniel Borkmann**
- **Participants:**
  - **Alexei Starovoitov**
  - **Dave Thaler**
  - **Brendan Gregg**
  - **KP Singh**
  - **Joe Stringer**
- **AGENDA:**
  - Misc bits:
    - GB sum up relevant to BSC [Dave]

      - Lisa now voted as vice chair
      - Budget discussion

        - Marketing + BSC
        - GB + BSC
          - Unclear whether budget split or common
      - Project adoption process for GB vote
        - Small change from Scott, ratified
          - We can now start getting projects in such as iovisor , eBPF for Windows
        - Example bcc
          - Reaching out to maintainers
          - Given already under iovisor (LF), logos etc already donated
          - Instructions on what to do: [bsc/project-progression-policy.md at master · ebpffoundation/bsc (github.com)](https://github.com/ebpffoundation/bsc/blob/master/project-progression-policy.md)
          - Fill out template, send to BSC, vote, good to migrate

            - Submission template (as linked from instructions above): [https://github.com/ebpffoundation/bsc/blob/master/project-submission-template.md](https://github.com/ebpffoundation/bsc/blob/master/project-submission-template.md)
          - Charter going into project's repo
            - Charter template (as linked from instructions above): [https://github.com/ebpffoundation/bsc/blob/master/Technical%20Charter%20(custom%2Bdata)%20--%20LF%20Projects%2C%20LLC%204-10-2019%20FINAL.docx](https://github.com/ebpffoundation/bsc/blob/master/Technical%20Charter%20(custom%2Bdata)%20--%20LF%20Projects%2C%20LLC%204-10-2019%20FINAL.docx)
          - [Governance - IO Visor Project](https://www.iovisor.org/about/governance)
    - Sponsoring updates [Daniel]
      - LPC 2022 (10k live stream sponsor -\> [done & listed](https://lpc.events/))
      - eBPF day 2022 (done, foundation is listed as livestream sponsor at [Cloud Native eBPF Day North America | Linux Foundation Events](https://events.linuxfoundation.org/cloud-native-ebpf-day-north-america/), 7.5k)
  - Review goals and ongoing efforts from BSC side [all]
    - [BPF guidelines](https://tinyurl.com/bpfguidelines2022) doc
      - Brendan to finish up reviewing the doc, then bring it to BSC for subsequent review.
        - Also working on BPF debugging guidelines, which could be a separate doc or included in above
    - [BPF roadmap](https://tinyurl.com/bpfroadmap2022) doc
      - KP: needs top
      - Use next meeting to go over the doc in detail
      - Goals also around presenting e.g. at LPC / elsewhere

- Shared / honest roadmap across companies to publish.

- xyz handled by company abc
- Adding priorities, difficulties

  - Example priority queue, scheduler.. 3 implementations each
  - Don't want important building blocks "owned" by startups and not widely available as OSS
- Other points not assigned so we can find interested folks in community
- Platform specific roadmap vs cross-platform roadmap structure
- Slidedeck & we add own agenda e.g. related to companies

- BPF standardization effort
- BPF ecosystem report (collab with marketing team)
- Technical Projects:

  - eBPF for Windows
  - tbd: iovisor migration
- BPF community events
  - 4 recurring ongoing conferences for BPF

    - LPC, LSF/MM/BPF, eBPF day, eBPF summit
  - Sponsoring recommendations to GB
    - Currently above 4 approved
    - More tbd
  - Event wishlist for next year:
    - An eBPF track/day at [https://indiafoss.net/](https://indiafoss.net/)
    - Potentially eBPF track for FOSDEM
    - LinuxCon Japan
      - [Open Source Summit Japan | Linux Foundation Events](https://events.linuxfoundation.org/open-source-summit-japan/)
    - KubeConAsia (eBPF day?)
    - Target crowd:
      - User-focussed people, less developer focussed
- Communication around BPF
  - "BPF is unsafe"
    - Analysis around BPF bugs/exploits from past CVEs and relation around distributions to clear off FUD
      - [Example](https://bugs.chromium.org/p/chromium/issues/detail?id=1320051): ChromsOS bug where they disabled lockdown and attacker used bpf\_write\_user helper
      - Best practices document around reasonable sec posture
      - BPF guidelines
    - Doc around security use cases that can be solved ("BPF is great for sec" writeup)
    - Post on ebpf.foundation website? User story
    - AI starting Google doc
  - "limited because not Turing complete"
    - Examples vs. service mesh [[0]](https://www.youtube.com/watch?v=heDVglDRDNw)[[1]](https://www.tetrate.io/blog/ebpf-and-sidecars-getting-the-most-performance-and-resiliency-out-of-the-service-mesh/), call w/ analysts, vs. WASM [[2]](https://www.infoq.com/news/2022/01/ebpf-wasm-service-mesh/)

- Other items?

  - Deprecation process of iovisor & migration of GH repositories? [Dave/Brendan/others?]

    - Anything to update from LF side?
    - What concrete steps are needed?

      - Covered above already
  - [https://github.com/ebpffoundation/bsc/pull/6](https://github.com/ebpffoundation/bsc/pull/6) (project nominations 2022) [Joe]
    - Stalled on [https://github.com/ebpffoundation/bsc/pull/6#discussion\_r931438187](https://github.com/ebpffoundation/bsc/pull/6#discussion_r931438187) ?
    - TBD for next week:
      - Rework PR to update to current list
      - Nominations

## Meeting #18 - 2022-08-10

- **Duration:**
  - **1h**
- **Chair:**
  - **Brendan Gregg**
- **Participants:**
  - **Alexei Starovoitov**
  - **Dave Thaler**
  - **KP Singh**
  - **Lisa Caywood**
  - **Daniel Borkmann**
  - **Joe Stringer**
  - **Andrii Nakryiko**
- **AGENDA:**
  - Daniel:
    - BSC recommendations for sponsorship help for BPF conferences, e.g.

      - eBPF day (co-located w/ KubeCon -\> October this year)
      - Linux Plumbers conf

        - Foundation could offer LPC passes for people in need
      - eBPF summit
      - Have $10k unratified in budget for events. Not enough for KubeCon general sponsorship.
        - Cloud Native eBPF day "gold" sponsorship is 9k; Dave: why not that? **BSC says yes**.
      - [https://events.linuxfoundation.org/wp-content/uploads/2022/08/sponsor-cncf-2022-08.10.22.pdf](https://events.linuxfoundation.org/wp-content/uploads/2022/08/sponsor-cncf-2022-08.10.22.pdf)
      - [https://events.linuxfoundation.org/wp-content/uploads/2022/08/sponsor-plumberscon22-080322.pdf](https://events.linuxfoundation.org/wp-content/uploads/2022/08/sponsor-plumberscon22-080322.pdf) anu
      - OneSummit (networking conf) has an eBPF submission (Dave).
      - Priority: ensure LPC and LSF/MM/BPF conf go ahead
      - [KP]: WIshlist for next year:
        - An eBPF track/day at [https://indiafoss.net/](https://indiafoss.net/)
    - ebpf.io now has Communities menu entry for SO, Reddit & Slack
      - AI: Daniel: update links to add more SO tags
      - [https://stackoverflow.com/questions/tagged/ebpf](https://stackoverflow.com/questions/tagged/ebpf)
      - [https://www.reddit.com/r/eBPF/](https://www.reddit.com/r/eBPF/)
      - Note that ebpf.io is a community site; BSC is making recommendations (Dave)
      - ebpf.io and ebpf.foundation seems duplicative and confusing (Lisa)
        - eBPF marketing team should look into this: Lisa, Bill, etc.
        - What if other sites pop up as eBPF, do we have any influence? (KP) If they use the eBPF logo, and if LF owns it, then yes (Lisa).
    - Update from Lorenz around SO collectives: tl;dr still too small at this point
    - Foundation doc around state of eBPF landscape to highlight community growth, production users & their use cases, etc (potentially sth for q1/2023)
      - E.g., similar to conference flyers
  - Dave:
    - [Copy in the requirements for being a Landscape Project by dthaler · Pull Request #9 · ebpffoundation/bsc (github.com)](https://github.com/ebpffoundation/bsc/pull/9) -- **BSC voted yes**
    - Emails from Sridhar to BSC
      - [eBPF-BSC] Feedback from LF-Legal on Approved Charter Changes.
      - [eBPF-BSC] Request to change the BSC Bi-Weekly Meeting times
      - [eBPF-BSC] Request for Feedback
        - [LF Networking Launches Open Source Project Anuket (opensourceforu.com)](https://www.opensourceforu.com/2021/01/lf-networking-launches-open-source-project-anuket/)
      - BSC members not on [eBPF-BSC] mailing list should join (Brendan)

## Meeting #17 - 2022-07-27

- **Duration:**
  - **1h**
- **Chair:**
  - **Andrii Nakryiko**
- **Participants:**
  - **KP Singh**
  - **Daniel Borkmann**
  - **Dave Thaler**
  - **Joe Stringer**
  - **Lisa Caywood**
  - **Brendan Gregg**
- **AGENDA:**
  - Lisa Caywood on Charter changes
    - [https://github.com/ebpf-io/ebpf.io/pull/172](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fgithub.com%2Febpf-io%2Febpf.io%2Fpull%2F172&data=05%7C01%7Cdthaler%40microsoft.com%7C84f7267afece4a4e2d9808da693d9018%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637938010396171822%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000%7C%7C%7C&sdata=dd5%2BuV4SgTd1CnN2wniL8c8U2cmqkyRMu1HVm5tJ1GU%3D&reserved=0)

      - BSC voted YES on April 20
      - Board voted YES on July 21
    - [https://github.com/ebpf-io/ebpf.io/pull/176](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fgithub.com%2Febpf-io%2Febpf.io%2Fpull%2F176&data=05%7C01%7Cdthaler%40microsoft.com%7C84f7267afece4a4e2d9808da693d9018%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637938010396171822%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000%7C%7C%7C&sdata=2fq16qdBBWgVjSPJvCbP%2FNXDOsD9z4vzfe5nF3vvrcA%3D&reserved=0)
      - BSC discussed in April and had no objections, just a question about exit process.  No comparable found for a foundation with an exit process, so propose treating that as separate issue
      - Board voted YES on July 21
      - Goal: Ratify YES vote (without closing discussion on exit process)
      - BSC ratified this on July 27th
    - [https://github.com/ebpf-io/ebpf.io/pull/175](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fgithub.com%2Febpf-io%2Febpf.io%2Fpull%2F175&data=05%7C01%7Cdthaler%40microsoft.com%7C84f7267afece4a4e2d9808da693d9018%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637938010396171822%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000%7C%7C%7C&sdata=0PWxVshWXYKDgzDxDEf6NEsZwd1O088ZbS3JhJbvWq0%3D&reserved=0)
      - Board voted YES on July 21
      - This is now up for BSC vote to complete the amendment
      - BSC voted in favor on July 27th
  - Dave Thaler also merged in
    - [https://github.com/ebpffoundation/bsc/pull/7](https://github.com/ebpffoundation/bsc/pull/7)
    - [https://github.com/ebpffoundation/bsc/pull/8](https://github.com/ebpffoundation/bsc/pull/8)
  - Sridhar's (remaining) board meeting updates?
    - Budget is in the process of being approved by the board
    - Marketing Committee is currently, per Sridhar: "We have a Marketing Committee (Lisa Caywood, Daniel Havey and Bill Mulligan) "  additional nominations welcome
    - Infrastructure cost estimate?
      - CI/CD currently covered by Meta
      - Documentation
      - These are not currently technical projects.
  - ONE summit submissions for BPF (networking conference in Seattle Nov.)
    - CFP end of this week.
    - [ONE Summit | Linux Foundation Events](https://events.linuxfoundation.org/one-summit-north-america/?hss_channel=tw-721094774)
  - eBPF day co-located at KubeCon (CFP open, too)
  - Stack Overflow Collectives: in progress, SO has been made aware

## Meeting #16 - 2022-07-13

- **Duration:**
  - **1h**
- **Chair:**
  - **Alexei Starovoitov**
- **Participants:**
  - **Lorenz Bauer**
  - **KP Singh**
  - **Brendan Gregg**
  - **Dave Thaler**
  - **Joe Stringer**
  - **Andrii Nakryiko**
  - **Daniel Borkmann**
- **AGENDA:**
  - Lisa Caywood will join on July 27th (we need to notify her if meeting is canceled)
  - Follow up to "foster eBPF community" discussion from last time
  - BSC re-election nominations
    - [https://github.com/ebpffoundation/bsc/pull/6](https://github.com/ebpffoundation/bsc/pull/6)
    - [https://github.com/ebpffoundation/ebpf.foundation/pull/4](https://github.com/ebpffoundation/ebpf.foundation/pull/4)
    - [https://github.com/ebpf-io/ebpf.io-website/pull/175](https://github.com/ebpf-io/ebpf.io-website/pull/175)
  - [Dave] ebpf.io vs ebpf.foundation website – done?
    - Lorenz: governance, what is ebpf, and docs like ISA, not other things on ebpf.foundation. Also Technical Projects once we get that going.
    - KP: BSC can periodically review project landscape but not be authoritative on the content for it, so ok to keep landscape projects on ebpf.io
    - Lorenz: ok for ebpf.io to have all ebpf related confs, and foundation only have things that foundation has an official role in
  - Ebpf summit, cloud native ebpf day, LPC ebpf track, lsf/mm/bpf are pre-authorized to use bee logo
  - Should we remove projects discussions from High-Pri items above? yes
  - [Lorenz]: Slack is not viable, messages disappearing and not publicly searchable
    - Should it be deprecated?
    - [https://stackoverflow.com/questions/tagged/ebpf+or+bpf](https://stackoverflow.com/questions/tagged/ebpf+or+bpf)
    - [https://www.reddit.com/r/eBPF/](https://www.reddit.com/r/eBPF/)
    - [KP] Why not [https://stackoverflow.com/questions/tagged/go?tab=Newest](https://stackoverflow.com/questions/tagged/go?tab=Newest)

      - See also [https://stackoverflow.com/collectives/go](https://stackoverflow.com/collectives/go)
    - [Andrii] BPF is a lot more things than just the BPF tag
      - C++, libraries, kernel
    - [Lorenz]: Figure out what is necessary to get a collective on SO
    - Requirements mentioned: web searchable, threaded, supports Q&A, can subscribe to new Q's or A's, not be specific to a single repo, not be specific to a single programming language (like go)
      - Non-requirement (but maybe nice to have): free
    - What to do next?
      - We need a collective: [https://stackoverflow.com/collectives](https://stackoverflow.com/collectives)

        - Tags like ebpf, bpf, xdp-bpf, bcc-bpf, libbpf, bpftrace, bpftool, etc
      - Slack archive? Steering to people to SO instead.
        - [http://bash.org/?244321](http://bash.org/?244321)

## Meeting #15 - 2022-06-01

- **Duration:**
  - **1h**
- **Chair:**
  - **Lorenz Bauer**
- **Participants:**
  - **KP Singhstack**
  - **Brendan Gregg**
  - **Dave Thaler**
  - **Joe Stringer**
  - **Andrii Nakryiko**
- **AGENDA:**
  - Discuss AI since last meeting (5 min)
    - Alexei is the next rotating chair for
    - AI Lorenz: ask Thomas about /bsc permissions again
  - Discussion with LF / Lisa Caywood didn't take place since we didn't communicate the invitation clearly enough, need to reschedule.
  - Where do we want to foster the eBPF community? (Lorenz Bauer) (10 min)
    - Current state: knowledge is locked in cilium Slack
    - We need at least the following from the main community hub:

      - Public archive
      - Easily searchable
      - Accessible from countries with strong censorship, e.g. China
      - Ability to export the data
      - Ability to moderate the community (assumption: CoC applies)
      - Accessible from companies, e.g. Meta (?)
      - Access via web interface, native app for iOS / android?
      - A way to get notified of new questions (mail?)
      - Threaded conversations
      - Social features: mark as answered, upvotes
      - Good integration with GitHub, other issue trackers
      - "Neutral ground": primary affiliation should be the foundation so that competitors can use the same community
      - More?
    - Options
      - Github Discussions
      - Discourse
      - Slack (default)
      - Email list
      - Stack overflow

        - [https://area51.stackexchange.com/](https://area51.stackexchange.com/)
      - Reddit
    - Proposal: Lorenz takes an action item to compare available platforms and make a recommendation.
      - [Question from Daniel] Could we have various options e.g. slack, stack overflow, reddit, email list and link them as "community resources" under ebpf.io? I'd assume there are already subcommunities for all of them, example:
        - Existing slack w/ ~10k users
        - [https://stackoverflow.com/questions/tagged/ebpf](https://stackoverflow.com/questions/tagged/ebpf)
        - [https://www.reddit.com/r/eBPF/](https://www.reddit.com/r/eBPF/)
        - [https://www.spinics.net/lists/xdp-newbies/](https://www.spinics.net/lists/xdp-newbies/) but we could also create a new list for ebpf itself (& searchable via lore)
        - Maybe just a matter of "official blessing" to link to them from ebpf.io?
  - Can we create a separate budget for eBPF related projects that are hard to get done otherwise? (Lorenz / Joe)
    - Examples
      - Documenting eBPF map semantics for cross platform compat, eBPF for Windows (Joe Stringer)
      - Allow Technical Projects to fund individuals for tasks
    - Prior art
      - Outreachy ([Outreachy | Internships Supporting Diversity in Tech - Outreachy](https://www.outreachy.org/)) interns paid for work
      - Hire LF to do XYZ
  - Discussed election schedule / process PRs from Joe
    - [https://github.com/ebpffoundation/bsc/pull/5](https://github.com/ebpffoundation/bsc/pull/5) is accepted an merged
    - [https://github.com/ebpffoundation/bsc/pull/6](https://github.com/ebpffoundation/bsc/pull/6) needs decision re charter changes, coordination with LF

## Meeting #14 - 2022-05-18

- **Duration:**
  - **1h**
- **Chair:**
  - **KP Singh**
- **Participants:**
  - **Alexei Starovoitov**
  - **Brendan Gregg**
  - **Dave Thaler**
  - **Joe Stringer**
  - **Andrii Nakryiko**
  - **Daniel Borkmann**
  - **Joe Stringer**
- **AGENDA:**
  - Discuss the High priority AIs
    - Dave: bsc github ACL issues, Dave could add any reviewers, but was able to "@" people in comments.
    - Strawman project proposal template form discussion (Example: eBPF for Windows)

      - Does every project need to have a charter?
      - LF: This is a template that can be changed any way that the project wants
      - KP: The template should explicitly mention that "it's flexible"
      - Security checklists from OpenSSF
      - Coverity for OSS: [https://scan.coverity.com/](https://scan.coverity.com/)
      - Review of the PDF form

        - KP: Does it need to be a delta highlighted
        - Dave: recommended
      - Costs
        - Github CI/CD resources (currently in freebie quota)
        - Code coverage licenses
      - Is the process approved? Discuss concerns, vote
        - Daniel: What happens if a process is not done by a single foundation / company?
          - Do the contributors have a vote?
        - Dave: There is a precedent, but not sure how it worked..
        - There were no changes to the form needed, but took longer as it was the first one. LF now has experience, so should hopefully.
        - A signatory was needed.
        - Positive vote for the process
  - Debrief from LSF/MM/BPF (limited time)
    - BPF Standardization
    - Christoph Hellewig indicated that they're willing to contribute.
  - Daniel: At KubeCon
    - Lot's of traction about eBPF
  - Cloud Native eBPF Day youtube playlist: [https://youtube.com/playlist?list=PLj6h78yzYM2PzqjM3DTYjiVZ42wXDp0Qg](https://youtube.com/playlist?list=PLj6h78yzYM2PzqjM3DTYjiVZ42wXDp0Qg)

## Meeting #13 - 2022-04-20

- **Duration:**
  - **1h**
- **Chair:**
  - **Joe Stringer**
- **Participants:**
  - **Alexei Starovoitov**
  - **Brendan Gregg**
  - **Dave Thaler**
  - **Joe Stringer**
  - **Andrii Nakryiko**
  - **Daniel Borkmann**
  - **KP Singh**
  - **Lorenz Bauer**
- **AGENDA:**
- (5m) Review action items
  - Charter amendment
    - Technical project criteria, current WIP proposal (Dave):

      - Criteria 1: Trademark transfer
      - Criteria 2: BPF Foundation is primary governance structure
- (5m) [Charter wording amendment](https://github.com/ebpf-io/ebpf.io/pull/172)
  - [Approved](https://github.com/ebpf-io/ebpf.io/pull/172#issuecomment-1104419435)
- (15m) Decide on re-election schedule with appropriate offsets to avoid replacement of the entire committee at once. Needs resolution by Q2 2022. (Governing board ask)
  - The [charter](https://ebpf.io/charter) has three election cases for the BSC:
  - 1) Chair, elected from BSC members.  BSC already decided to rotate every two weeks, so this one is done.
  - 2) eBPF Runtime Representative, from active contributors to the runtime.
  - 3) Additional Project Representatives, from active contributors to additional important projects
  - (Dave): Note (4bi) - For continuity at least half of these should stay the same at any point in time
    - The rest of the categories do not have this constraint
      -
  - Process:
    - Need the outline of how to do the election
      - Project nomination?
      - AI(Joe): Figure out the projects
    - Need to figure out how to stagger (who to re-elect at 1y mark)
      - Volunteers from BSC
    - Need to set a date (proposal: October 2022)
  - Original list from August 2021:
    - Two representatives (the "Kernel Representatives") from the group of eBPF Linux kernel maintainers
    - - Daniel Borkmann, Isovalent, eBPF Maintainer
    - - Alexei Starovoitov, Facebook, eBPF Maintainer
        -
    - One representative (each a "eBPF Runtime Representative") for each additional open-source eBPF runtime implementation.
    - - Dave Thaler, Microsoft, eBPF Runtime for Windows
        -
    - Up to two representatives ("Additional Project Representatives") from additional open source projects that are important to the eBPF ecosystem, as determined by the BSC.
    - - Lorenz Bauer, Cloudflare, eBPF Go library & long-time eBPF contributor
    - - KP Singh, Google, eBPF LSM
        -
    - Up to three representatives with maintainer status ("Maintainer
    - Representatives") of major eBPF Foundation projects as approved by the BSC.
    - - Brendan Gregg, Netflix, bcc/bpftrace
    - - Andrii Nakryiko, Facebook, Katran
    - - Joe Stringer, Isovalent, Cilium Maintainer
  - Timeline:
    - Members elected: October
    - Election: Mid sept at latest
    - Projects to elect members from: August
- (30m) Discuss [eBPF Technical Roadmap](https://docs.google.com/document/d/1-zyHDLg5NTlKX6oPgyupvJRIn5pK40-x8-hoE3xPQu4/edit) proposals
  - Expanded the list, included a few additional ideas here
  - More may come up during LSF/MM/BPF
- (5m) Next meeting: 18 May (Avoid overlap with LSF/MM/BPF)

## Meeting #12 - 2022-04-06

- **Duration:**
  - **1h**
- **Chair:**
  - **Alexei Starovoitov**
- **Participants:**
  - **Brendan Gregg**
  - **Andrii Nakryiko**
  - **Dave Thaler**
  - **Daniel Borkmann**
- **AGENDA:**
- ebpf.io / bpf.io - AI Daniel: Move domains to a BSC owned entity so the domains stay in ownership of the eBPF community represented by BSC. Solely BSC is admin & owner. BSC is good with this.
- Discussion / update around iovisor transferral
- AI all: Review and extend [KP's doc](https://docs.google.com/document/d/1-zyHDLg5NTlKX6oPgyupvJRIn5pK40-x8-hoE3xPQu4/edit) for next time with roadmap items
  - For next meeting we'll go over them and discuss
- AI Daniel: Create a [brand@ebpf.io](mailto:brand@ebpf.io) (list with: 1 legal, 1 marketing person on it)
  - Check with Bill on status of brand guidelines so we can push PR further
- BSC agreed to use eBee logo for cloud native eBPF day as well as LSF/MM/BPF conference

## Meeting #11 - 2022-03-23

- **Duration:**
  - **1h**
- **Chair:**
  - **Dave Thaler**
- **Participants:**
  - **Brendan Gregg**
  - **Andrii Nakryiko**
  - **Dave Thaler**
  - **Alexei Starovoitov**
  - **Joe Stringer**
  - **KP Singh**
- **AGENDA:**
- Review open AI's
- Takeaways from Governing Board meeting
  - ebpf.io vs ebpf.foundation website
  - Fixing posted charter
  - Proposal to create a marketing committee to manage website, event logistics, press releases (subcommittee tasked with creating actual proposal: Thomas, Lisa, Stephen, Dave)
  - Open question about slack channel vs Cilium
  - Investigating level of LF PM support, leaning towards "Extended Support (level 3)"
- [Dave] Plan for next open meeting, should we have another discussion of signed programs at an earlier time slot?
  - 9am Pacific Thursdays is bpf office hours, could use that slot for open meetings
  - Currently under "kernel" section but could be moved up on project page to be more general.   Keep rule to cancel if no agenda proposal.
  - **AI (KP):** investigate creating an app script
  - **AI (Dave):** PR to update socializing wider than "kernel"
  - KP discussing signing programs with various folks
  - **AI (KP):** pick a week for signed program discussion
- [Alexei] Times for future BSC meetings
  - Lorenz missed so should we use a different time that is more convenient for Brendan?  Back to 1pm Pacific / 7am Australia / 10pm Switz (April 27th)... why do we have a 3 week gap?
  - **AI (Daniel):** update invite, meet April 6 and 20 (etc) at 1pm Pacific, with 1 hr duration [DONE]
- [Dave] [Charter](https://ebpf.io/charter/) says that by default "One representative of any Member may observe meetings of the BSC" but the BSC can change that at any time.
  - Discussion: Don't change, don't proactively invite, but allow requests if they come
- [Dave] Review of updated [https://github.com/ebpf-io/bsc/pull/1](https://github.com/ebpf-io/bsc/pull/1)
  - Proposed sequencing:
    - Review proposal
    - Get ebpf for windows example case
    - Approve proposal
    - Go through acceptance process for ebpf for windows
- Discussion of project scoping
  - Dave's high level strawman from last meeting: a project must be able to argue how it _encourages/fosters the deployment and use of eBPF_, not just (e.g.) allow using eBPF as an option
  - **AI (Dave):** get ebpf for windows to fill out forms
  - **AI (All):** Review the PR
  - CLA/DCO required?
  - IP declarations?
    - Is there potential for intellectual property or patent problems to arise from participation in eBPF foundation?
    - Legal questions, leave to legal review of project submission, not BSC scope.
  - All BSC to review PR to approve this process
    - Hold back on approval until first project works through the process.
    - eBPF for Windows can be guinea pig
  - **AI (KP):** create a skeleton doc for categories/roadmap of projects

## Meeting #10 - 2022-03-09

- **Duration:**
  - **1h**
- **Chair:**
  - **Daniel Borkmann**
- **Participants:**
  - **Andrii**
  - **Alexei**
  - **Dave**
  - **Daniel**
  - **Joe**
  - **Brendan**
- AI: Ask from LF
  - Offer an open BSC meeting slot. For example once a month.
  - Cadence could be once every 4 weeks
  - How to propose items for discussion
    - For example, BPF office hours
  - Invitation from BSC side
  - AI: doc for topics & contact points to BPF foundation website
- [Dave] How to best track AI's – follow-up to review above list w/ current state
- [Dave] eBPF Foundation projects (as opposed to "landscape") - follow up from 2021-10-13 meeting
  - Review of [https://github.com/ebpf-io/bsc/pull/1](https://github.com/ebpf-io/bsc/pull/1)
  - General feedback to be lightweight (minimum viable governance), maybe just have one stage for now, not distinguish between levels
  - KP AI: technical project can ask BSC for an invite
  - KP how do we define an overall mission for technical steering committee
    - BSC meeting to chart out goals
  - E.g. encourage deployment of OSS eBPF as technology
  - Technical vs landscape projects
- BPF + integrity subsystem
  - [https://lore.kernel.org/bpf/20220302111404.193900-1-roberto.sassu@huawei.com/](https://lore.kernel.org/bpf/20220302111404.193900-1-roberto.sassu@huawei.com/)
  - [https://docs.google.com/document/d/1tcoIAZhdBMHg5usuMopMJczYqLgEMiifyHwoXPz4Cp8/edit](https://docs.google.com/document/d/1tcoIAZhdBMHg5usuMopMJczYqLgEMiifyHwoXPz4Cp8/edit)
  - Potentially we meet with Mimi at LSF/MM/BPF to discuss next steps

## Meeting #9 - 2022-02-23

- **Duration:**
  - **1h**
- **Chair:**
  - **Brendan Gregg**
- **Participants:**
  - **Andrii Nakryiko**
  - **Brendan Gregg**
  - **Dave Thaler**
  - **KP Singh**
  - **Joe Stringer**
  - **Alexei Starovoitov**
  - [**Lorenz Bauer**](mailto:lmb@cloudflare.com)
- LSFMMBPF
  - Beautiful Palm Springs, CA
  - Do your proposal
- Lorenz will have a new job
  - Discuss BSC when he starts; Lorenz will give up spot if that makes sense
  - Will keep working on BPF
- How to track pending AIs [Dave]
  - Could put them at the top of this doc, or annotate this doc
  - Could add them to github repo
  - We will add tick boxes to top of document
  - KP will figure out how best to do this and tell us
- eBPF foundation projects [Dave]
  - Examples from other projects of governance
  - Example projects:
    - eBPF for Windows
    - Prevail verifier
    - L3AF
  - Is the goal to acquire projects for eBPF (and sponsorship money)? [Joe]
  - Can a project be short-lived? (e.g., make an API improvement) [Joe]
    - Yes, examples with other projects do this
  - Can be academic projects, corporate projects [Dave]
  - We should read through the three options above and have a meaningful discussion [Alexei]
    - LF CCC [governance/project-progression-policy.md at main · confidential-computing/governance (github.com)](https://github.com/confidential-computing/governance/blob/main/project-progression-policy.md)
    - LF Networking [LFN Project Lifecycle (Updated) - LF Networking - LF Networking Confluence](https://wiki.lfnetworking.org/pages/viewpage.action?pageId=62490363)
    - CNCF process [toc/project\_proposals.adoc at main · cncf/toc (github.com)](https://github.com/cncf/toc/blob/main/process/project_proposals.adoc) benefits [https://www.cncf.io/services-for-projects/](https://www.cncf.io/services-for-projects/)
  - eBPF foundation charter is to have projects! [Dave]
  - Note that LF CCC has a statement to say that projects have to promote the use of eBPF [Dave]
  - Can we include old projects like bpftrace? [Brendan]
    - After selecting governance, we then can look at existing/future projects
  - Getting funding for CI would be a benefit [Lorenz]
  - LF tooling: [https://lfx.linuxfoundation.org/](https://lfx.linuxfoundation.org/)
  - Can propose projects that further eBPF that haven't been started yet; we lay out technical direction of where eBPF should go  [KP]
  - To endorse a project, we would need to believe in its technical vision and how it benefits the eBPF ecosystem. [Alexei]
    - Be LF-like: if it promotes eBPF, it's good
  - CCC Project Contribution Agreement: [https://lists.confidentialcomputing.io/g/main/files/TAC/Project%20Submissions/LF%20Projects%20--%20Form%20of%20Trademark%20and%20Account%20Assignment.docx](https://lists.confidentialcomputing.io/g/main/files/TAC/Project%20Submissions/LF%20Projects%20--%20Form%20of%20Trademark%20and%20Account%20Assignment.docx)

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
