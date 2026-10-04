# Documentation plan template

A one-page agreement between the writer, the product manager, and engineering about what documentation will be delivered, by whom, and when. Complete the [planning checklist](../checklists/01-documentation-planning.md) first, then fill in this plan. Share it for sign-off before you start writing.

---

## Template

```markdown
# Documentation plan: [Project, release, or feature]

| | |
|---|---|
| **Owner** | [Writer name] |
| **Product manager** | [Name] |
| **Engineering contact** | [Name] |
| **Release** | [Version or name], planned for [YYYY-MM-DD] |
| **Status** | [Draft/Approved/In progress/Done] |
| **Last updated** | [YYYY-MM-DD] |

## Goal

After this release, [audience] can [what they can do] by using the documentation.

## Scope

**In scope:**

- [Feature or change, with link to epic or spec]

**Out of scope:**

- [Item, and the reason or where it is covered]

## Audience

[Primary audience and their goal. Link to the audience analysis if there is one.]

## Deliverables

| # | Deliverable | Type | New or update | Owner | SME reviewer | Due | Status |
|---|---|---|---|---|---|---|---|
| 1 | [Page title] | [How-to/Concept/Reference/Tutorial/Release notes] | [New/Update] | [Name] | [Name] | [Date] | [Not started] |

## Milestones

| Milestone | Engineering date | Docs deliverable | Docs date |
|---|---|---|---|
| Feature complete | [Date] | First drafts ready for technical review | [Date] |
| Code freeze | [Date] | Technical review complete | [Date] |
| Release candidate | [Date] | Editorial review complete, docs staged | [Date] |
| Release | [Date] | Docs published | [Date] |

## Dependencies and risks

| Dependency or risk | Impact | Mitigation | Owner |
|---|---|---|---|
| [Description] | [What happens to the docs] | [Plan] | [Name] |

## Sign-off

| Name | Role | Date |
|---|---|---|
| [Name] | Product manager | [Date] |
| [Name] | Engineering lead | [Date] |
```

---

## Example: deliverables and milestones

> The following excerpt uses the fictional Parcelwise platform.

**Goal:** After the 4.2 release, warehouse IT administrators can connect the Sync Agent to a MySQL database without contacting support.

| # | Deliverable | Type | New or update | Owner | SME reviewer | Due | Status |
|---|---|---|---|---|---|---|---|
| 1 | Configure the database connection | How-to | Update | Priya N. | Tomás R. | 2026-02-20 | In review |
| 2 | Configuration reference: `database.*` | Reference | Update | Priya N. | Tomás R. | 2026-02-20 | Drafting |
| 3 | Install Parcelwise Sync Agent: requirements | Reference | Update | Priya N. | Tomás R. | 2026-02-13 | Done |
| 4 | Troubleshoot MySQL connections | Troubleshooting | New | Priya N. | Support: Lena K. | 2026-02-27 | Not started |
| 5 | 4.2.0 release notes | Release notes | New | Priya N. | Release manager | 2026-03-06 | Not started |

| Milestone | Engineering date | Docs deliverable | Docs date |
|---|---|---|---|
| Feature complete | 2026-02-11 | First drafts ready for technical review | 2026-02-20 |
| Code freeze | 2026-02-25 | Technical review complete | 2026-02-27 |
| Release candidate | 2026-03-03 | Editorial review complete, docs staged | 2026-03-06 |
| Release | 2026-03-10 | Docs published | 2026-03-10 |
