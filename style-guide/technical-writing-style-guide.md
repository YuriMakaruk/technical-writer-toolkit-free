# Technical writing style guide

A concise house style for software documentation. Adopt it as is, or change any rule to match your organization and record the change in [Local decisions](#local-decisions). Where a rule is a matter of preference rather than clarity, it says so.

If you need a full reference, established public guides include the *Google developer documentation style guide* and the *Microsoft Writing Style Guide*. This guide is compatible with both on most points.

**Contents:** [Headings](#headings) · [Sentences](#sentences) · [Active and passive voice](#active-and-passive-voice) · [Imperatives](#imperatives) · [Terminology](#terminology) · [Capitalization](#capitalization) · [UI elements](#ui-elements) · [Code formatting](#code-formatting) · [Lists](#lists) · [Tables](#tables) · [Notes and warnings](#notes-and-warnings) · [Examples](#examples) · [Cross-references](#cross-references) · [Links](#links)

---

## Headings

- Use sentence case: capitalize only the first word and proper nouns. *(Preference. Title case is also common. Choose one.)*
- Start task headings with a verb in the base form: "Create a shipment". Use noun phrases for concept and reference headings: "Shipment lifecycle", "Configuration reference".
- Do not skip levels (H2 to H4). Screen readers and generated tables of contents depend on the hierarchy.
- Use one H1 per page.
- Do not end headings with punctuation, except question marks in FAQs.
- Do not put links or code formatting in headings unless the heading is the name of a code element, such as an API endpoint.

| Do | Don't |
|---|---|
| Configure a proxy | Proxy Configuration |
| Rate limits | Understanding Rate Limits |
| `POST /v1/shipments` | How the POST shipments call works |

## Sentences

- Put the most important information first in the sentence and the paragraph.
- Aim for sentences under 25 words. Split sentences that contain more than one instruction or idea.
- Keep paragraphs to 1–4 sentences.
- Put conditions before instructions, so readers know whether the instruction applies to them.
- Use present tense. Describe what the product does, not what it "will" do.
- Use "you" for the reader. Do not use "the user" when you mean the reader.
- Remove words that add no meaning: *simply, just, easily, basically, please, note that, in order to, it is important to*.
- Do not use Latin abbreviations: write "for example" instead of "e.g.", "that is" instead of "i.e.", "and so on" instead of "etc."

| Do | Don't |
|---|---|
| If you use a proxy, set `PW_PROXY_URL`. | Set `PW_PROXY_URL` if you happen to be using a proxy. |
| The agent retries failed requests. | The agent will retry failed requests. |
| To cancel a shipment, … | In order to cancel a shipment, you simply need to … |

## Active and passive voice

Use active voice by default. It names who does what, which is often the information the reader needs.

Use passive voice when:

- The actor is unknown or irrelevant: "The label is deleted after 28 days."
- The object is the focus, as in reference descriptions: "Returned if the shipment is canceled."
- Active voice would blame the reader: "The file was not found" instead of "You did not provide the file."

| Do | Don't |
|---|---|
| Parcelwise sends a webhook when the status changes. | A webhook is sent when the status is changed. |
| The API returns a `409` error. | A `409` error is returned by the API. |

## Imperatives

- Write each procedure step as an instruction that starts with a verb: "Click **Save**."
- Use one action per step. Two short actions in the same place can share a step: "Select the order, and then click **Create shipment**."
- Put the location before the action when the reader needs to move first: "In **Settings**, click **Webhooks**."
- If a step has a visible result, put it in a separate sentence after the instruction, not in the instruction.
- Do not write "You should", "You can now", or "The user must" in steps.
- Use these verbs for UI actions consistently:

| Action | Verb |
|---|---|
| Buttons, links, menu items | click (or select, if you also cover touch and keyboard) |
| Checkboxes | select, clear |
| Toggles | turn on, turn off |
| Text fields | enter |
| Lists and dropdowns | select |
| Pages and locations | go to |
| Keyboard keys | press |

*(Preference: some guides use "select" for everything to be input-neutral. Choose one approach.)*

## Terminology

- Use one term for one concept. Do not vary terms for style. If the product says "workspace", never write "project" or "space" for the same thing.
- Record every product term, its preferred form, and the forms to avoid in the [glossary](../glossary/glossary-template.md).
- Define a term on first use on each page where the reader might land directly, or link to the definition.
- Spell out an abbreviation on first use, followed by the abbreviation in parentheses: "subject matter expert (SME)". Exception: abbreviations that the audience knows better than the expansion, such as API, URL, or HTTP.
- Do not use internal code names, team names, or ticket jargon in public docs.
- Avoid idioms and culture-specific references. They are hard for non-native readers and translators.

## Capitalization

- Capitalize product names, feature names that are trademarks or branded names, and proper nouns. Write generic feature names in lowercase: "address validation", not "Address Validation", unless the product uses it as a brand.
- Match the capitalization of UI labels exactly, even if it differs from your heading style.
- Write code elements, commands, and values with their exact case, in code format: `true`, `PW_API_KEY`, `pw-agent`.
- Do not capitalize words for emphasis.
- Do not use all capitals, except for abbreviations and when quoting UI text that uses them.

## UI elements

- Format UI element names in **bold**: "Click **Create key**."
- Write the label exactly as it appears, but without trailing punctuation or ellipses ("…").
- Do not include the element type unless it helps the reader find it: "Click **Save**", not "Click the **Save** button". Include the type when two elements have similar labels, or for less obvious elements such as tabs or toggles.
- Use `>` to show a navigation path, with each part in bold: **Settings** > **Shipping** > **Address validation**.
- Do not describe the UI by position or color only ("the green button on the right"). Positions change, and the description fails for people who cannot see color.

## Code formatting

Use `code format` for anything the reader types, or that appears exactly as written in code or output:

- Commands, flags, and arguments: `pw-agent status --json`
- File names, paths, and extensions: `/etc/parcelwise/agent.yaml`, `.yaml`
- Code elements: class, function, field, and parameter names
- Values, including `true`, `null`, and string values
- Environment variables, HTTP methods with paths, status codes, and error codes

Use code blocks for:

- Anything the reader copies: commands, code, configuration.
- Output the reader compares with their own.

Rules for code blocks:

- Always specify the language for syntax highlighting: `bash`, `json`, `yaml`, `text`.
- Do not include the shell prompt (`$` or `>`) in commands that readers copy. If you must show a command and its output together, put them in separate code blocks.
- Use placeholders that cannot be mistaken for real values, and explain them: `<your-api-key>`. Use one placeholder style throughout. *(Preference: `<angle-brackets>`, `YOUR_API_KEY`, and `{curly}` are all common.)*
- Keep lines under about 80 characters, and break long commands with line continuation characters.
- Every code sample must be tested.

## Lists

- Use a **numbered list** for steps in a sequence and for ranked items. Use a **bulleted list** for everything else.
- Introduce a list with a complete sentence or a phrase that ends with a colon.
- Keep list items parallel: start each one with the same part of speech.
- Capitalize the first word of each item.
- End an item with a period if it is a complete sentence. Use no ending punctuation for fragments. Do not mix both in one list.
- Use lists for three or more items. Two items usually read better in a sentence.
- Avoid more than two levels of nesting. In procedures, use nested lists only for sub-steps or for options within a step.

## Tables

- Use tables for information that has two or more dimensions: parameters with types and descriptions, comparisons, mappings. Do not use a table for a simple list.
- Always include a header row.
- Introduce the table with a sentence that explains what it contains.
- Order rows logically (alphabetically, by frequency of use, or by workflow) and say which, if it is not obvious.
- Do not leave cells empty. Use "None", "Not applicable", or "—", and use the same one throughout.
- Keep cells short. If a cell needs more than about 3 sentences, link to a section instead.
- Do not put procedures in tables.

## Notes and warnings

Use only these four types, and use them sparingly. If every paragraph has a note, readers ignore them.

| Type | Use for | Example |
|---|---|---|
| **Note** | Information that is useful but that the reader can skip. | Sandbox keys start with `pw_test_`. |
| **Tip** | A better or faster way to do something. | To filter by several statuses, separate them with commas. |
| **Important** | Information the reader must know to succeed. | You cannot change the service after buying the label. |
| **Warning** | Risk of data loss, security problems, downtime, or charges. | Deleting a key immediately breaks every integration that uses it. |

Rules:

- Put warnings **before** the step or paragraph they apply to.
- Say what happens and how to avoid it: "Deleting the warehouse deletes all its queued orders. Export the queue first."
- Do not put essential steps inside notes.
- Do not stack admonitions. Two in a row usually means the content needs restructuring.

## Examples

- Use realistic examples. Real-looking names, addresses, IDs, and amounts help readers recognize what the values should look like.
- Use reserved domains (`example.com`, `example.org`, or the `.example` top-level domain) and reserved IP ranges (`192.0.2.0/24`, `198.51.100.0/24`, `203.0.113.0/24`) for fictional hosts. These are reserved for documentation by RFC 2606 and RFC 5737.
- Use fictional people and companies. Do not use real customer data, real credentials, or real employee names.
- Use names from different cultures, and avoid stereotypes.
- Make examples consistent: if one page uses the shipment `shp_2Xn7PqR9`, related pages should use the same one.
- Show a complete, working example before explaining variations.

## Cross-references

- Cross-reference instead of repeating. Each fact should have one source of truth.
- Tell the reader why to follow the reference: "For valid weight ranges, see *Shipment fields*."
- Put prerequisite references before the steps, and follow-up references after the result.
- Refer to sections in the same document by heading. Refer to other documents by title.
- Do not write "above" or "below". Content moves, and screen reader users may not perceive position. Link instead.

## Links

- Use link text that describes the destination. The reader should know where a link goes without reading the surrounding sentence.
- Use the target page's title, or a description of it, as the link text. Do not use "click here", "this page", "read more", or a bare URL.
- Keep link text short: usually 2–6 words.
- Do not link the same destination more than once on a page, unless the page is long.
- Avoid links in procedures, except in prerequisites and the last step. Links in the middle of a procedure take readers away from the task.
- Use relative links to pages in the same docs set, so links work in all versions and environments.
- Say when a link goes to an external site or downloads a file: "Download the OpenAPI description (YAML, 120 KB)."

| Do | Don't |
|---|---|
| For details, see **Authentication**. | For details, use "click here". |
| See the Parcelwise status page. | See https://status.parcelwise.example. |

---

## Local decisions

Record your organization's changes to this guide here, so that every writer applies the same rules.

| Topic | Decision | Date | Decided by |
|---|---|---|---|
| [Topic, for example "Heading case"] | [Decision, for example "Title case for H1 only"] | [YYYY-MM-DD] | [Name] |
