# Documentation planning checklist

**Use when:** starting documentation for a new product, a major release, or a large feature. Complete it before you write. The output goes into the [documentation plan](../planning/documentation-plan.md).

## Scope

- [ ] I can state in one sentence what the documentation must enable readers to do.
- [ ] The list of features, changes, or components in scope comes from a source of truth (roadmap, epic, PRD), and I have linked it.
- [ ] Out-of-scope items are written down and agreed with the product manager.
- [ ] I know whether this is new content, an update to existing content, or both, and I have listed the existing pages affected.

## Audience

- [ ] Primary and secondary audiences are named by role (for example "platform engineer"), not "users".
- [ ] For each audience, I know their goal, prior knowledge, and where they will look for help.
- [ ] I have talked to at least one person who represents the audience, or to support or sales staff who talk to them.

## Content

- [ ] Each deliverable has a type (tutorial, how-to, concept, reference, release notes) and an owner.
- [ ] I have checked support tickets, forum posts, and search logs for questions this release should answer.
- [ ] I know which content is generated (API reference, CLI help) and who maintains the generator.
- [ ] Screenshots, diagrams, and videos are listed separately, because they take longer to produce and to update.
- [ ] Localization needs are known: languages, deadlines, and whether the translation vendor needs a string freeze.

## People and access

- [ ] Each deliverable has a named subject matter expert (SME) who has agreed to review.
- [ ] Review time is booked in the SMEs' sprint or calendar, not assumed.
- [ ] I have access to a working build, test environment, or sandbox account.
- [ ] I have access to the design files, specs, and issue tracker.

## Schedule

- [ ] Documentation milestones are tied to engineering milestones (feature complete, code freeze, release), not only to dates.
- [ ] The plan includes time for review rounds, fixes, and publishing — usually at least 30% of the writing time.
- [ ] There is a date after which only critical changes to the product are allowed to change the docs.
- [ ] The release manager knows that documentation is part of the release criteria.

## Risks

- [ ] Features that are likely to change or slip are marked, and I have a fallback (for example, publishing the page later).
- [ ] Dependencies on other teams are written down with owners and dates.
