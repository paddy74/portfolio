---
sidebar_label: Peer Review Process
tags:
  - example
  - agile
---

# Example Peer Review Process

This article is an example of the **Peer Review Process** section of a [Team Working Agreement](./index.md).

## Introduction

Peer review is the simple idea that code requires a second pair of eyes before it is either checked in or merged into the `main` version of the codebase. While code review adds additional time to the development process, its benefits greatly outweigh the additional effort.

## Benefits of Peer Reviews

- Peer reviews ensure that fewer mistakes and bugs are introduced to the main codebase. These mistakes and bugs would otherwise need to be identified, tracked, and fixed and could have ripple effects on other systems &mdash especially when dealing with components of the core application or system architecture.
- Peer reviews help the team share knowledge by allowing time for developers to demonstrate how they completed a problem and what thought process was used to get there. It presents an opportunity for developers who may not be as strong in one area to gain knowledge as the code changes and is discussed between parties.
- Peer reviews help the team make more accurate story point estimates. As knowledge stabilizes across the team in technical skill levels and understanding of the project's requirements it becomes easier to make story point estimates, write work-item descriptions, and define acceptance criteria.
- Peer reviews mentor developers who are new to the team. By sharing knowledge through the peer review process, newer members to the team can become more productive quicker.

## Synopsis

The team will define branch rules for all protected branches in the project's version control system which govern how changes are submitted, merged, pushed, or otherwise made to such branches according to global and branch-specific rules. These protected branches are identified as: `main`, `stage`, `test`, `develop`, and `feat/`.

Changes must never be pushed directly to a protected branch. All work should begin by creating a new branch, and changes must be introduced into protected branches exclusively through Pull Requests (PRs). Code owners must be defined, and at least one reviewer approval is required before a (PR) can be merged into a protected branch. (PRs) may be merged only by the (PR) owner or, if explicitly delegated, by another contributor to the (PR).

All changes must be tested for bugs or unexpected behavior, with new tests written as necessary to maintain required test coverage. For (PRs) that introduce new functionality, breaking changes, or are otherwise complex, a peer review meeting should be held to demonstrate and discuss the changes; otherwise, an asynchronous peer review is sufficient. All request items (RITMs) resulting from the peer review must be addressed before the (PR) is merged.

## Peer Review Instructions

### Modify Branch Policies to Enforce Code Reviews

This team uses branch policies to enforce code reviews. Through branch policies, changes can only be made to protected branches through (PRs).

(PRs) which target a `feat/` or `develop` branch use policies to enforce:

- Require at least 1 reviewer other than the (PR) creator
- Suggest that the (PR) be linked to at least 1 work-item
- Block completion while any comments are active
- Require approval by the Technical Lead

(PRs) which target the `test` or `stage` branch use policies to enforce:

- Require at least 2 reviewers other than the (PR) creator
- Suggest that the (PR) be linked to at least 1 work-item
- Block completion while any comments are active
- Require approval by a member of the architectural team

(PRs) which target the `main` branch use policies to enforce:

- Require at least 2 reviewers other than the (PR) creator
- Suggest that the (PR) be linked to at least 1 work-item
- Block completion while any comments are active
- Require approval by the Project Manager
- Require approval by the Technical Lead
- Require approval by a member of the architectural team

### Process to Make Updates to Code

Team members will use (PRs) to make changes to the code. As a developer makes changes to the codebase they will be required to make a new branch off of the applicable `feat/` or `develop` branch, make changes to the new branch, push the new branch and its changes to the remove repository, create a (PR) merging the new branch into the target branch, conduct a peer review, and only merge into the target `feat/` or `develop` branch after responding to all RITMs and being approved by assigned code owners and reviewers.

#### Submitting a (PR)

1. Ensure that Git is configured according to [the Git Version Control Standards](../../engineer/standards/git.md).
2. Clone the repository you plan on modifying
3. Checkout the `feat/` or `develop` branch, as applicable
4. Create a new branch off the `feat/` or `develop` branch, as applicable, and use a good name that complies with [the branch naming conventions](../../engineer/standards/git.md#branch-naming-conventions) (e.g. `bug#139-lost-page`).
5. Perform the work within the scope of the associated work-item or ad-hoc task. Follow the [commit message standards](../../engineer/standards/git.md#git-commit-message-standards) when making commits.
6. Test your changes locally to make sure it does what you intend it to do.
7. If appropriate, test your changes in the project's "development" environment. For shared "development" environments, first notify other team members to avoid conflicts with changes they may also be testing in the "development" environment.
8. Push your new branch to the upstream repository. Check that you are pushing changes with the correct account and your work is signed with a GPG signing key according to [the Git Version Control Standards](../../engineer/standards/git.md).
9. Navigate to the upstream repository's user interface.
10. Select the button **New (PR)**.
11. Set the appropriate source and target branches, select and fill out the right (or default) PR template. The title must follow [the (PR) conventions](../../engineer/standards/git.md#merge-request-conventions) (e.g., `[patch]: restrict lost page access to admins`).
12. Select the appropriate assignees and reviewers for the PR's peer review.
13. Link to PR to its associated work-item, if there is one.
14. Click **Create** to create the (PR).

When creating a new (PR), first rebase or merge the target branch back into your working branch. This reduces the chance of unexpected bugs or merge conflicts.

#### Peer Review Meeting

It is expected that all (PRs) have an associated peer review meeting. Peer review meetings must be attended by all members of the relevant line-of-effort and the Technical Lead.

The remainder of the team must also be invited, but their attendance is optional. Exceptions can be made for small, non-functional changes such as documentation updates or spelling corrections. These exceptions will be made most commonly for 1 Story Point work-items. These items will still require a review and testing process (if applicable) by the reviewers.

Peer reviews will be conducted within the following guidelines:

- The requester will make arrangements with reviewer(s) outside of the version control system. This meeting must be scheduled with the team's meeting tool and calendar and include the full team as an optional invite.
- Reviewers should be familiar with the technology/application to which changes are being made.
- Peer reviews should be a joint effort between the requester and the reviewer; a conversation rather than the reviewer being given code and expected to "figure it out".
- It is preferred that functional changes be demonstrated before discussing any changes to the source code.
- Code review should be conducted as frequently as necessary.
- All outstanding (PRs) will be disposed of (approved or rejected) by the end of each sprint.

After reviewing the changes that need to be made the reviewer can now choose to make comments on the (PR) if they have a concern with the changes. If any additional commits are added to the (PR) all old and new commits will need to be tested and reviewed to ensure a new bug wasn't introduced.

Once a (PR) meets all requirements the (PR) will be merged into the target branch.
