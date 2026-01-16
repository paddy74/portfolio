---
tags:
  - standards
---

# Work-Item Label Standards

This article defines a general standard for labelling work-items (issues, tasks, etc.) and pull requests. The specific value gained and labelling functions will vary depending on your work tracking and version control systems, but this guide assumes a DevOps Suite such as [GitHub](https://github.com/) or [GitLab](https://gitlab.com/). In this context, a "general standard" applies to the labels defined at top-level group, team, or organization whereas a sub-group, project, or repository often has additional layers of labelling standards.

Good labelling standards provide a consistent understanding of the definitions and purposes of different labels. They enable processes such as [change management](./change-management.md), Kanban, and [backlog refinement](./agile/index.md#backlog-refinement), enriching data used by analytics dashboards that visualize things like Sprint Burndown and [DORA metrics](https://cloud.google.com/blog/products/devops-sre/using-the-four-keys-to-measure-your-devops-performance), and help team members find, prioritize, and quickly understand their work.

:::note

These standards are not intended to be universally applicable. Different organization structures, development stacks, and objectives will influence how labels will be used and to what extent. I recommend and generally start with the below labels for [priorities](#priority), [type](#work-type-classification), and [workflow/status](#workflow--status) &mdash using the other categories on this page as examples of other useful ways to apply labels. This is demonstrated by inconsistent key/description formats despite my inclination towards consistency.

:::

## Priority

| Label | Description |
| --- | --- |
| ~priority::1-critical | Critical. We will address this as soon as possible regardless of limit on our team capacity. |
| ~priority::2-high | High. We will address this soon and will provide capacity from our team for it in the next few releases. |
| ~priority::3-medium | Medium. We want to address this but may have other higher priority items. |
| ~priority::4-low | Low. We will address this when it is convenient to do so. |
| ~priority::5-lowest | Planning. We don't have visibility of when this will be addressed. |

## Work Type Classification

These labels are based on [GitLab Handbook | Work Type Classification](https://handbook.gitlab.com/handbook/product/groups/product-analysis/engineering/metrics/#work-type-classification). Types are key in communicating progress and metrics to leadership while providing team members with a way to quickly understand the context of the work. Types can be further classified into optional sub-types, which are more flexible and expansive than the top-level types.

| Label | Description |
| --- | --- |
| ~type::bug | Issues that report undesirable or incorrect behavior. |
| ~type::feature | Any issue/MR that contains work to support the implementation of a feature and/or results in an improvement in the user experience. |
| ~type::maintenance | Upkeeping efforts and catch-up corrective improvements that are not Feature nor Bugs. |
| ~type::ignore | When using this type, the issue will be excluded from cross functional planning metrics. This is used for meta, planning, issues. |

### Sub-Type Classifications

Below are examples of labels for classifying sub-types. Work must not be labeled with a sub-type without also adding the respective top-level type.

| Label | Description |
| --- | --- |
| ~bug::performance | Performance defects or response time degradation. |
| ~bug::vulnerability | Defects related to Security Vulnerabilities. |
| ~feature::enhance | Improvements that refine an existing feature by adding additional capabilities. |
| ~maintenance::dependency | Updates to dependencies and their version upgrades. |

## Workflow / Status

Workflow labels are critical tracking the status of work. They provide information beyond a simple "Open" or "Closed" status that helps understand where exactly in the development lifecycle something is.

| Label | Description |
| --- | --- |
| ~workflow::new | This issue has not been looked at or needs additional details such as acceptance criteria, Story Points, or labeling. |
| ~workflow::backlog | This work is in the backlog and will be pulled forward when expedient. |
| ~workflow::active | This work is in progress. |
| ~workflow::review | This work is in review. |
| ~workflow::accepted | This work meets its acceptance criteria as is ready to be merged or executed. |
| ~workflow::complete | This work-item is closed as it has been reviewed, accepted, and merged or executed. |

## Role

Role labels identify specific roles that the work is most suited for. It allows developers to focus on the work within their realm of expertise &mdash or where there are opportunities to expand into another discipline.

| Label | Description |
| --- | --- |
| ~role::sre | This work is related to work performed by Site Reliability Engineers. |
| ~role::writer | This work requires a Technical Writer. |
| ~role::data:engineer | This work is intended for Data Engineers and is within that domain of expertise. |
| ~role::data:analyst | This work directly supports developing analytics dashboard; requires Data Analyst expertise. |
| ~role::data:scientist | Assignable to Data Scientists. |

## Product

Organizations and teams with multiple distinct products will benefit from labeling work based on its associated product. This is especially helpful for projects shared amongst multiple products, so that work in the shared project can be traced back to the product requesting or triggering the change.

| Label | Description |
| --- | --- |
| ~product::superthings | This work is associated with the "SuperThings" product. |
| ~product::homewebsite | This work is associated with the company's website at "www.example.com" |
| ~product::datamaker2 | This work is associated with the sequel product to "DataMakerOne". |
| ~product::costtracker | This work is associated with the software behind our internal cost tracking tool. |

## Organizational Units

Complex organizations &mdash especially those with multiple independent development teams &mdash benefit from adding labels for each respective organizational unit.

| Label           | Description                                                        |
| --------------- | ------------------------------------------------------------------ |
| ~ou::data       | Example. This work is owned by the Data group.                     |
| ~ou::rnd        | Example. This work is owned by the Research and Development group. |
| ~ou::accounting | Example. This work is owned by the Accounting group.               |

## Facet Label

Facet labels enable filtering of search results or dashboards and help surface key information about the labelled item.

| Label | Description |
| --- | --- |
| ~service-request | This work is requested _directly_ by live users or customers. |
| ~blocked | Issues with an _external_ impediment where a dependency exists outside the team and the team is unable to progress the work-item until work outside the team's control is done. |
| ~invalid | Issues that will not be addressed. |
| ~documentation | Facet label. This work is related to product documentation. |
| ~security | Facet label. This work is security related. |
| ~infrastructure | This work is related to product infrastructure. |
