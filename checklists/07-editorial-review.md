# Editorial review checklist

**Use when:** doing a language and consistency pass after technical review. Do this pass last, because technical changes introduce new errors. Rules referenced here are in the [style guide](../style-guide/technical-writing-style-guide.md).

## First pass: read as the reader

- [ ] The first paragraph says what the page is about and who it is for.
- [ ] The page type is clear, and the page does only that job (concept, task, or reference).
- [ ] Each heading describes the content below it. Reading only the headings gives a correct outline.
- [ ] Nothing important is only in a screenshot, table note, or footnote.

## Sentences

- [ ] Most sentences are under 25 words. Longer sentences contain no more than one idea.
- [ ] Instructions use the imperative ("Click **Save**"), not "You should click" or "The user clicks".
- [ ] Active voice is used unless the actor is unknown or unimportant.
- [ ] No filler: "simply", "just", "easily", "please note that", "in order to", "it is important to".
- [ ] No promises about the future ("will soon support") unless approved.
- [ ] Conditions come before instructions ("If X, do Y").

## Terminology and names

- [ ] Product, feature, and UI names match the [glossary](../glossary/glossary-template.md) and the product.
- [ ] One term is used for each concept. No synonyms for variety.
- [ ] Abbreviations are spelled out on first use, unless the audience knows them better as abbreviations (API, URL).

## Formatting

- [ ] Headings use the same case style throughout.
- [ ] UI elements are in bold. Code, commands, file names, and values are in code format.
- [ ] Numbered lists are used only for sequences. Bulleted lists are used for everything else.
- [ ] List items are parallel: all start with the same part of speech and use the same punctuation.
- [ ] Tables have headers, and every cell has content (use "None" or "—" consistently).
- [ ] Notes and warnings use the defined types only, and there are no more than two per screen.

## Links and references

- [ ] Every link works and goes to the most specific relevant page or section.
- [ ] Link text describes the destination. No "click here" or bare URLs in body text.
- [ ] Cross-references to UI locations use the format **Menu** > **Item**.

## Mechanics

- [ ] Spelling and grammar checked with a tool, and the results reviewed by a person.
- [ ] Numbers, units, dates, and times use one format throughout.
- [ ] Placeholder text, comments to reviewers, and TODOs are removed.
