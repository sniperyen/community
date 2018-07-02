这是一项正在进行的工作，记录了我们到目前为止的运作方式。

# 原则

Kubernetes社区遵守以下原则：

* 开放：Kubernetes是开源的。请参阅下面的仓库准则和CLA。
* 欢迎和尊重：请参阅下面的行为守则。
* 透明和可被访问：工作和协作应该公开进行。请参阅下面的SIG治理。
* 优点：理念和贡献是根据其技术优势，与项目目标相一致的，[范围](http://kubernetes.io/docs/whatisk8s/), 和 [设计原则](contributors/design-proposals/architecture/principles.md).

# 行为守则

Kubernetes社区遵守 CNCF [行为守则](https://github.com/cncf/foundation/blob/master/code-of-conduct.md). 这里是一个摘录：

_作为该项目的贡献者和维护者，为了培养一个开放和热情的社区，我们保证尊重所有通过报告问题贡献自己力量的人，发布需求，更新文档，提交 pr 或 patch 以及其他活动._

作为Kubernetes项目的成员，您代表项目和您的贡献者。
我们非常重视我们的社区，我们希望继续培养友好和协作的贡献者和用户的环境。我们希望社区中的每个人都拥有
[积极的经验](https://www.cncf.io/blog/2016/12/14/diversity-scholarship-series-one-software-engineers-unexpected-cloudnativecon-kubecon-experience).

# 社区会员

查看 [社区会员]

# 社区团体

该项目有四种主要类型的组：

1. 特殊兴趣小组，SIG
2. 子项目
3. 工作组, WGs
4. 委员会

请注意，该项目也正在组织一个掌舵委员会，其详细信息将很快记录在案。

## 兴趣小组

The Kubernetes project is organized primarily into Special Interest
Groups, or SIGs. Each SIG is comprised of members from multiple
companies and organizations, with a common purpose of advancing the
project with respect to a specific topic, such as Networking or
Documentation. Our goal is to enable a distributed decision structure
and code ownership, as well as providing focused forums for getting
work done, making decisions, and onboarding new contributors. Every
identifiable subpart of the project (e.g., github org, repository,
subdirectory, API, test, issue, PR) is intended to be owned by some
SIG.

Areas covered by SIGs may be vertically focused on particular
components or functions, cross-cutting/horizontal, spanning many/all
functional areas of the project, or in support of the project
itself. Examples:
* Vertical: Network, Storage, Node, Scheduling, Big Data
* Horizontal: Scalability, Architecture
* Project: Testing, Release, Docs, PM, Contributor Experience

SIGs must have at least one and ideally two SIG leads at any given
time. SIG leads are intended to be organizers and facilitators,
responsible for the operation of the SIG and for communication and
coordination with the other SIGs, the Steering Committee, and the
broader community.

Each SIG must have a charter that specifies its scope (topics,
subsystems, code repos and directories), responsibilities, areas of
authority, how members and roles of authority/leadership are
selected/granted, how decisions are made, and how conflicts are
resolved. A [简单的模板] for intra-SIG governance has been
developed in order to simplify SIG creation, and additional templates
are being developed, but SIGs should be relatively free to customize
or change how they operate, within some broad guidelines and
constraints imposed by cross-SIG processes (e.g., the release process)
and assets (e.g., the kubernetes repo).

A primary reason that SIGs exist is as forums for collaboration.
Much work in a SIG should stay local within that SIG. However, SIGs
must communicate in the open, ensure other SIGs and community members
can find notes of meetings, discussions, designs, and decisions, and
periodically communicate a high-level summary of the SIG's work to the
community.

See [sig 治理] for more details about current SIG operating
mechanics, such as mailing lists, meeting times, etc.

## Subprojects

Specific work efforts within SIGs are divided into **subprojects**.
Every part of the Kubernetes code and documentation must be owned by
some subproject. Some SIGs may have a single subproject, but many SIGs
have multiple significant subprojects with distinct (though sometimes
overlapping) sets of contributors and [拥有者], who act as
subproject’s technical leaders: responsible for vision and direction
and overall design, choose/approve change proposal (KEP) approvers,
field technical escalations, etc.

Example subprojects for a few SIGs:
* SIG Network: pod networking (CNI, etc.), Service (incl. kube-proxy),
Ingress, DNS, and Network policy
* SIG Apps: workload APIs, Helm, Kompose, ...
* SIG Cluster Lifecycle: kubeadm, kops, kubespray, minikube, ...

Subprojects for each SIG are documented in [sigs.yaml](sigs.yaml).

## 工作组

We need community rallying points to facilitate discussions/work
regarding topics that are short-lived or that span multiple SIGs.
This is the purpose of Working Groups (WG). The intent is to make
Working Groups relatively easy to create and to deprecate, once
inactive.

To propose a new working group, first find a SIG to sponsor the group. 
Next, send a proposal to kubernetes-dev@googlegroups.com and also include
any potentially interested SIGs. Wait for public comment. If there's 
enough interest, a new Working Group should be formed. 

Create a new mailing list in the from of kubernetes-wg-group-name. Working 
groups typically have a Slack channel as well as regular meetings on zoom.
It's encouraged to keep a clear record of all accomplishments that's publicly
accessible.

## 委员会

某些主题（如安全性或行为守则）需要
慎重. Whereas SIGs are voluntary groups which operate in the
open and anyone can join, Committees do not have open membership and do
not always operate in the open.  The steering committee can form
committees as needed, for bounded or unbounded duration.  Membership
of a committee is decided by the steering committee.  Like a SIG, a
committee has a charter and a lead, and will report to the steering
committee periodically, and to the community as makes sense, given the
charter.

## 跨项目沟通与协调

While most work shouldn’t require expensive coordination with other
SIGs, there will be efforts (features, refactoring, etc.) that cross
SIG boundaries.  In this case, it is expected that the SIGs coordinate
with each other and come to mutually agreed solutions. In some cases,
it may make sense to form a Working Group for joint work.  Cross-SIG
coordination will naturally require more time and implies a certain
amount of overhead.  This is intentional to encourage changes to be
well encapsulated whenever possible.

On the other hand, several SIGs do have project-wide impact, for
example Release, Testing, and API Machinery. Even those that do not
may sometimes need to make changes or impose new processes or
conventions that affect other SIGs. In these cases, project-wide
communication processes will need to be followed. For example,
proposals with project-wide impact will need to be announced more
broadly, with the opportunity for members of other SIGs to provide
feedback and guidance. However, the SIG that owns the area, according
to its charter, will own the decision. In the case of extended debate
or deadlock, decisions may be escalated to the Steering Committee,
which is expected to be uncommon.

The exact processes and guidelines for such cross-project
communication have yet to be formalized, but when in doubt, use
kubernetes-dev@googlegroups.com and make an announcement at the
community meeting.

# 仓库指南

All repositories under Kubernetes github orgs, such as kubernetes and kubernetes-incubator,
should follow the procedures outlined in the [incubator document](incubator.md). All code projects
use the [Apache Licence version 2.0](LICENSE). Documentation repositories should use the
[Creative Commons License version 4.0](https://git.k8s.io/website/LICENSE).

# CLA

所有贡献者必须准守 CNCF CLA, 具体描述查看 [这里](CLA.md).

[社区会员]: /community-membership.md
[sig 治理]: /sig-governance.md
[拥有者]: community-membership.md#subproject-owner
[简单的模板]: committee-steering/governance/sig-governance-template-short.md

[![Analytics](https://kubernetes-site.appspot.com/UA-36037335-10/GitHub/governance.md?pixel)]()
