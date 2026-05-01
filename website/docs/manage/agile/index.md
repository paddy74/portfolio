---
sidebar_label: Team Working Agreement
tags:
  - example
  - agile
---

# Example Agile Team Working Agreement

This article is an example of an Agile Team Working Agreement[^1] for an DevSecOps team using lean development methodologies.[^2]

[^1]: [_Establishing an Agile Team Working Agreement_. GSA Office of the CTO](https://tech.gsa.gov/guides/agile_team_working_agreement/)

[^2]: [Wikipedia | Lean Software Development](https://en.wikipedia.org/wiki/Lean_software_development)

## Methodology

The team will follow a Scrum[^3] Agile methodology. **Sprints will be three weeks in length**, beginning on Monday and ending on Friday. Daily stand-up meetings will take place at 10:30am EST/EDT. On the first day of a Sprint, there will not be a daily stand-up and there will be a Sprint Planning meeting. On the last day of a Sprint, there will not be a daily stand-up and there will be a [Sprint Review](#sprint-review) and [Sprint Retrospective](#sprint-retrospective) meeting. On the Thursday of each week, the Scrum Master will host a [backlog refinement meeting](#backlog-refinement) with the team and Product Owner.

[^3]: Takeuchi, Hirotaka, and Ikujiro Nonaka. (1986, January 1). ["The New New Product Development Game."](https://www.hbs.edu/faculty/Pages/item.aspx?num=38542) _Harvard Business Review_ 64, no. 1 (January-February 1986).

### Meeting Etiquette

- Be on time.
- Cadence.
- Mute unless speaking.
- If stepping away, please say so in chat.

## Agile Team Roles

The team roles will be based on the [Scaled Agile Framework](https://scaledagileframework.com/agile-teams/).

## Agile Ceremonies

### Daily Stand-Up

**15 minutes**. An additional 15 minutes is reserved for parking-lot discussions.

Update the team on the status of work.

1. What did you accomplish yesterday?
2. What did you accomplish today?
3. Do you have any blockers preventing you from completing your work?

Ensure follow-up / parking-lot meetings are scheduled and held between relevant parties.

### Backlog Refinement

- Facilitator: Scrum Master
- Attendees: Scrum Master, Scrum Team, Product Owner, Client Sponsors
- Recurrence: Every Thursday
- Start Time: 1300 EST
- Duration: 1 hour

Backlog refinement aims to define the Features and User Stories for the current Program Increment and must define the User Stories proposed for the upcoming Sprint. A User Story's title, description, acceptance criteria, priority, story points, and connected work-items all must be defined during Backlog Refinement.

User Stories must be written prior to Backlog Refinement. A User Story's title, description, acceptance criteria, priority, and connected work should be defined prior to Backlog Refinement. Such properties will be reviewed and refined during Backlog Refinement.

Story Point estimates are made with Planning Poker. Team members whose skills aligns to a given User Story are required to vote and all other team members are encouraged to vote.

See the [Backlog Story Point Estimation](#backlog-story-point-estimation) section for information on the criteria for Story Point estimations.

### Sprint Review

- Facilitator: Scrum Master
- Attendees: Scrum Master, Scrum Team, Product Owner, Client Sponsors
- Recurrence: Last day of each Sprint
- Start Time: 1000 EST
- Duration: 1 hour

The Sprint Review allows the team to showcase what was accomplished and collect feedback on complete and incomplete work-items.

1. Demonstrate progress and accomplishments made during the closing Sprint. Individual demonstrations are to be conducted by the team member(s) who accomplished the work.
2. Review work-items that were completed.
3. Review work-items that were not completed. Justify why these stories were not completed and how the situation may be avoided in the future.
4. Present the Sprint Burndown and Velocity charts.
5. Collect feedback from the Product Owner and Client Sponsor

### Sprint Retrospective

- Facilitator: Scrum Master
- Attendees: Scrum Master, Scrum Team
- Recurrence: Last day of each Sprint
- Start Time: 1300 EST
- Duration: 30 minutes

The Sprint Retrospective provides the team with the opportunity to provide feedback on what went well and what can be improved on in order to create a plan for improvements to be enacted during the next Sprint.

The team will follow the 4 Ls Retrospective technique[^4].

[^4]: Gorman, Mary, and Ellen Gottesdiener. (2010, June 24). ["The 4L's: A Retrospective Technique."](https://ebgconsulting.com/blog/the-4ls-a-retrospective-technique/) _EBG Consulting_.

- **Liked**: What went well? What did team members appreciate, enjoy, or find effective? These are things that should be kept or done more in the future.
- **Learned**: What was learned? This could be technical knowledge, better communication methods, or insights into the project or process.
- **Lacked**: What made things more difficult? What is missing or needs improvement? These are gaps in how the team is working, such as missing resources, skills, or support that would have made the Sprint more successful.
- **Longed for**: What would have made things better? These are things that team members wish they'd had during the Sprint, such as better tools, clearer requirements, or more time; anything that would have made the Sprint more efficient or enjoyable.

Team members are expected, but not required, to make 2-3 contributions to the Sprint Retrospective. Retrospective items are collected anonymously. Team members are also expected, but not required, to complete a team assessment. The Scrum Master will remind the team to make these contributions each Sprint prior to the Retrospective.

1. Collection of Retrospective items.
2. Read each item out loud, by column.
3. Team members allocate 5 votes to promote items for discussion.
4. Items are discussed in order of votes.

It is the goal of each discussion item to propose a new work-item or change to team practices.

### Sprint Planning

- **Facilitator**: Scrum Master
- **Attendees**: Scrum Master, Scrum Team
- **Recurrence**: First day of each Sprint
- **Start Time**: 1000 EST
- **Duration**: 1 hour

Team members are expected to update their Sprint Capacity prior to Sprint Planning.

1. Define the Sprint Goal.
2. Determine Sprint capacity.
   - Add any days off to the Sprint Calendar.
3. Commit to User Stories.

### Technical Exchange Meeting

- **Facilitator**: Agile Project Manager
- **Attendees**: Scrum Master, Scrum Team, Product Owner, Client Sponsors
- **Recurrence**: Once per year
- **Duration**: 2-3 days

Conduct a full in-depth review of past, current, and future products developed by the team. A separate discussion will be hosted for each line-of-effort.

## Capacity and Velocity

Sprint Planning and workflow management will follow the "story point" system. In keeping with Scrum Agile methodology, capacity will be established in such a way that the pace of work remains sustainable over the long-term and allows for continuous learning.

Capacity per Sprint will be calculated by the Scrum Master during Sprint Planning according to the following formula:

- Members of the development team self-report estimates of their personal capacity to the Scrum Master during Sprint Planning.
- The Scrum Master sums self-reported individual story point capacity estimates to calculate the team's Gross Capacity for the Sprint.
- The sum of all individual capacity estimates for the development team multiplies by a factor of 0.7 to account for administration, logistics, normal friction, and continuous learning. The resulting figure is the team's Net Capacity for the Sprint.
- The resulting number will be assigned as the team's capacity for the Sprint.

The amount of work in progress is limited to two in-progress (2) backlog items per developer.

## Features

Whenever possible technical development items in the team's backlog (user stories, bugs) will be traceable to a feature specified by Product Ownership. All features will be decomposed into backlog items (user stories, bugs). The team will adapt the [Scaled Agile Framework (SAFe)](https://scaledagileframework.com/agile-teams/) definition of a feature:

> A feature is a service that fulfills a stakeholder need. Each feature includes a benefit hypothesis and acceptance criteria and is sized or split as necessary to be delivered by a single Agile Release Train (ART) in a Program Increment (PI).

Features will be prioritized preferable according to [Weighted Shortest Job First (WSJF)](https://framework.scaledagile.com/wsjf/) and the MoSCoW method by product ownership on an ongoing basis: at least every six Sprints but not more than every other Sprint. Feature value and priority will be communicated to the development team during IP Sprints and Sprint Planning as appropriate. Backlog items will be grouped according to feature.

## Backlog Items

The following work-item types will be used:

- **Epic**: A large user story, perhaps several months in size, that can span multiple Program Increments. Epics represent major strategic objectives. Epics are not considered part of Sprint commitments.
- **Feature**: A medium-sized user story representing a capability or functionality which is meaningful to the customer. Features may span multiple Sprints and comprise portions of epics but should be sized such that they can be completed within a single Program Increment. Each feature in the team's backlog should map directly to an Epic. Features are not considered part of Sprint commitments.
- **User Story**: A requirement for new functionality directly derived from or in response to engagement with external stakeholders. User stories are estimated in Sprint Planning. - Technical Debt: Items identified and logged in accordance with the team's Technical Debt Policy. Technical debt items are estimated in Sprint Planning. Technical debt items will be labeled as tech-debt in **_redacted_**.
- **Bug**: A security vulnerability or any issue with an existing system or tool which impairs functionality. Bugs are not estimated in Sprint Planning but will be used to report and track problems encountered during development and testing. A User Story must be written to address a given bug.
- **Task**: Any technical or non-technical task not otherwise defined. Tasks are generally considered so small and/or simple that they do not require estimation. A task may be used to comprise portions of user stories.
- **Issue**: Default work-item type. Any technical or non-technical task for which a User Story must be written but requires a work requirements discussion. Issues are the only work-items which may be written without consulting leadership.

### Labelling

Labels will be used to categorize and help describe, discover, filter, and manage work-items and pull requests. Labels will align with the team's [Work-Item Label Standards](../task-labels.md).

## Backlog Story Point Estimation

Story Points are used by the team to represent the estimated size, complexity, and effort needed to complete a User Story. Story Points are assigned a number from the Fibonacci scale.

The minimum size is 1 story point.

The maximum allowed size is 5 story points. However, 5 story points is highly discouraged and should be split into smaller work-items. Work-items larger than 5 story points are only allowed for items intended to be extremely general.

Members of the development team should consider the size of backlog items in their estimation. That is - even though an item may be a replication of previous work, have no external dependencies, and utilize existing highly available technology - the sheer amount of work required may justify additional story points.

In addition to the size of a story, the following criteria will automatically raise an item by one level of magnitude (e.g., 1 to 2, 2 to 3, 3 to 5, etc.). These criteria will be implicitly added by development team members during the estimation process of Sprint Planning.

- New development work.
- Replication of previously completed development work in a new environment.
- External dependencies.
- Requires significant learning (e.g., new or unfamiliar technology and/or skill transfer through collaboration).
- Requires significant collaboration between multiple team members.

Backlog items which are not completed during a Sprint and which are rolled over into a later Sprint will typically not be re-estimated. This is to make sure the team gets credit for all work completed. Backlog items may have their estimate increased if it becomes clear that the original estimate was too small. Items may also be re-estimated if they are divided into smaller work- items.

### Story Point Criteria

#### 1 - Point

The following criteria defines a one-point item:

- Something that can be completed in less than 2 hours.
- Something which has been done before and/or requires no new development work.
- An item with no external dependencies.
- An item which utilizes or deploys technology which is existing/working/highly available/accessible.

Real-world examples of one-point items include:

- Typing a set of well-worded release notes one page in length.
- Renaming a function or class or changing the directory structure of a library.
- Updating dependencies and testing for breaking changes.

#### 2 - Point

The following criteria defines a two-point item:

- Something that can be completed in less than a day.

Real-world examples of two-point items include:

- Reading the documentation for an unfamiliar library.
- A minor change to a piece of code that can be coded, tested, and deployed within a half-day.

#### 3 - Point

The following criteria defines a three-point item:

- Something that can be completed in more than a day, but less than 3 days.

Real-world examples of three-point items include:

- Designing and adding a set of new endpoints for a backend API.
- Writing infrastructure-as-code for a single new cloud resource.

#### 5 - Point

The following criteria defines a five-point item:

- Something that can be completed in less than a week, but more than two days.

Real-world examples of five-point items include:

- Refactoring a large and complex function.
- Conducting requirements investigation for a new Feature.
- Designing the REST API for a new back-end service.

## **_redacted_** Ticket Creation

All work-items - both technical and non-technical - will have a ticket created and placed on the team's **_redacted_**. Except for Issues, all new technical work-items must be approved for creation by the team's Technical Lead. Non-Technical work-items are expected to be created by or approved by the team's requirements analyst. When creating a ticket, the reporter must include the following items:

1. Work-Item Type: User Story, Bug, Task, Issue (see above).
2. Summary: Work-item title; a one sentence description.
3. Description: A detailed description of the work-item, including the definition of done. This gives the context and any needed background information needed for developers to work the item successfully.
4. Acceptance Criteria: Specific requirements (technical or not) which must be satisfied for the work-item to be considered complete. This may include documentation requirements, review requirements, etc.
5. Priority: Defaults to medium (3). See ... for further guidance.
6. Assignee: Defaults to unassigned unless otherwise directed.

When working a ticket, team members should add documentation as needed. Further, the comments/discussion section of the ticket should be used to note major milestones and challenges.

## Workflow

The team will follow a default workflow which may be supplemented for specific scopes, such as separate boards for platform development and customer service requests.

1. **New** `~workflow::new`: This issue has not been looked at or needs additional details such as acceptance criteria, Story Points, or labeling before work can start. This work-item is not ready for the backlog and is synonymous to a "draft" or "triage" state.
2. **Backlog** `~workflow::backlog`: This work is in the backlog and will be pulled forward when expedient.
3. **Active** `~workflow::active`: This work is in-progress. It is currently being worked-on and is not complete, ready for review, or blocked.
4. **Review** `~workflow::review`: The assignee for this work has determined that its acceptance criteria has been met and it is ready for [peer review](#peer-review-of-codechanges).
5. **Accepted** `~workflow::accepted`: This work has met its acceptance criteria and is ready to be merged or executed.
6. **Complete** `~workflow::complete`: This work is closed and complete. It has been reviewed, accepted, and merged or executed; no further action is needed.

## Work-Item Assignment

Work-items are assignable to any team member that has the ability and capacity to complete them. Only work-items that are well-defined can be moved to the backlog or be worked on. Poorly-defined work-items _must_ become well-defined before moving to the backlog, be assigned, or be worked-on.

## Code Movement

Wherever possible and appropriate all development items will be worked on local developer systems to avoid unnecessary cloud interfacing and costs. Only once a development item has been successfully tested on a local developer system should it be deployed to any remote environment.

- Upon code changes in the code repository's `develop` branch, changes will be deployed to the non-production "development" environment via continuous deployment processes.
- Upon code changes in the code repository's `test` branch, changes will be deployed to the non-production "testing" environment via continuous deployment processes.
- Upon code changes in the code repository's `stage` branch, changes will be deployed to the non-production "staging" environment by continuous delivery processes.
- Upon code changes in the code repository's `main` branch, changes will be deployed to the production environment by continuous delivery processes.

## Version Control

Developer notes should be written and attached to their assigned and active work-items at the end of each day regarding the progress made throughout the day on the work-item. When work is submitted for review or approval, these notes should include relevant versions of software applications, scripts, and artifacts used in the final satisfaction of the acceptance criteria.

<!-- TODO: add missing link target -->
The team's version control standards can be found at [the Git Version Control Standards](/).

## Peer Review of Code/Changes

<!-- TODO: add missing link target -->
All changes to project source code and documentation will be subject to the team's [Peer Review Process](/) policy.

## Technical Debt Policy

Technical debt will be managed in accordance with the team's [Technical Debt Policy](./tech-debt.md).

## Continuous Learning Policy

As noted above, Sprint Capacity will include allowances for continuous learning. Continuous learning activity is considered time spent acquiring new skills related to the product's development, including research required to complete assigned tasking. **20%** of Sprint Capacity will be allocated to Continuous Learning.
